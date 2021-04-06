---
layout: page
title: Introduction to Data Analysis with Python 
description: PART 0 Python Basics
img: /assets/img/teachings/intro_to_d_a/markus-spiske-FXFz-sW0uwo-unsplash.jpg
importance: 2
---

Cover photo by <a href="https://unsplash.com/@markusspiske?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Markus Spiske</a> on <a href="https://unsplash.com/collections/2488721/data-science?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>


# Podstawy Pythona {#podstawy}
1. [Podstawowe typy danych i zmienne, podstawowe struktury danych](#typy)
2. [Podstawowe operacje](#operacje)
3. [Warunek if](#if)
4. [Pętla for](#for)
5. [Funkcje](#funkcje)
6. [Importowanie modułów](#import)
7. [Rekomendowane strony](#rekomendacje)

## 1. [Podstawowe typy danych i zmienne, podstawowe struktury danych](#podstawy) {#typy}
Znak równości 
> =

używany jest do przypisania wartości do zmiennej. Zmienna znajduje się po lewej stronie znaku równości, wartość po prawej stronie. 

Przykład
> liczba = 5

Jako iż Python jest językiem z typowaniem dynamicznym, nie musimy określać typu danych jaki przechowuje dana zmienna jak to się odbywa w językach z typowaniem statycznym.

Ten sam przykład w języku z typowaniem statycznym
> int liczba = 5

Zmienne są ważnym elementem wszystkich programów, przypisuje się do nich dane, modyfikuje je, wykonuje się na nich operacje etc.

Wszystkie zmienne mają swój zasięg, w ramach tego zasięgu są "widoczne", możemy się do nich odwołać i je modyfikować. Zmienne tworzone np. w funkcjach, warunkach czy pętlach nie są widoczne poza ich zakresem.

Ważne jest żeby nazywać zmienne unikatowo, żeby ich przypadkowo nie nadpisać, zaś sama nazwa powinna informować za co dokładniej odpowiada dana zmienna.

**Zmiena musi być zainicjalizowana, nie można tworzyć niezainicjalizowanej zmiennej**


```python
liczba = 5
print(liczba)
#nadpisanie liczby
liczba = 3
print(liczba)
```

    5
    3
    

Jeżeli chcemy zachować poprzednią wartość możemy na przykład utworzyć nową zmienną i dalsze operacje wykonywać na niej


```python
pierwsza_liczba = 5
print(pierwsza_liczba)
#przypisanie wartosci pierwszej liczby do nowej zmiennej
druga_liczba = pierwsza_liczba
print(druga_liczba)
#modyfikacja drugiej zmiennej
druga_liczba = 3
print(pierwsza_liczba)
print(druga_liczba)
```

    5
    5
    5
    3
    

Tabela przedstawiająca podstawowe typy danych:

Typ danych | Nazwa
--- | ---
Typ całkowity | int
Typ zmiennoprzecinkowy | float
Typ zespolony | complex
Typ tekstowy | str
Typ logiczny | bool

By sprawdzić typ zmiennej należy wpisać komende
>type(x)

gdzie x to nasza zmienna



```python
print(type(5))
print(type(5.0))
print(type(5 + 0j))
print(type("5"))
print(type(True))
```

    <class 'int'>
    <class 'float'>
    <class 'complex'>
    <class 'str'>
    <class 'bool'>
    

Żeby zmienić typ zmiennej należy określić na jaki typ zmiennej chcemy go zmienić.


```python
napis = "5"

print("Rzutowanie na liczbę całkowitą:")
liczba_calkowita = int(napis)
print(liczba_calkowita)
print(type(liczba_calkowita))

print("\nRzutowanie na liczbę zmiennoprzecinkową:")
liczba_zmiennoprzecinkowa = float(napis)
print(liczba_zmiennoprzecinkowa)
print(type(liczba_zmiennoprzecinkowa))

print("\nRzutowanie na liczbę zespoloną")
liczba_zespolona = complex(napis)
print(liczba_zespolona)
print(type(liczba_zespolona))

print("\nRzutowanie na wartość logiczną")
wartosc_logiczna = bool(napis)
print(wartosc_logiczna)
print(type(wartosc_logiczna))
#Rzutowanie na wartość logiczną zwróci True, jeżeli dana wartość nie jest pusta, nie jest None 
```

    Rzutowanie na liczbę całkowitą:
    5
    <class 'int'>
    
    Rzutowanie na liczbę zmiennoprzecinkową:
    5.0
    <class 'float'>
    
    Rzutowanie na liczbę zespoloną
    (5+0j)
    <class 'complex'>
    
    Rzutowanie na wartość logiczną
    True
    <class 'bool'>
    

Zadanie, które z poniższych wartości zwróci True, a które zwrócą False?


```python
true_or_false = [None for x in range(8)] # deklaracja listy, narazie się tym nie przejmujemy
true_or_false[0] = "false"
true_or_false[1] = "False"
true_or_false[2] = False
true_or_false[3] = 0
true_or_false[4] = None #w Pythonie zamiast null używa się None
true_or_false[5] = "" #deklaracja pustego napisu
true_or_false[6] = [] #deklaracja pustej listy
true_or_false[7] = -1

for i in range(8):
  print(bool(true_or_false[i]))

```

    True
    True
    False
    False
    False
    False
    False
    True
    

### Podstawowe struktury danych

#### Listy

Listy to najbardziej uniwersalne struktury danych w Pythonie. 

Definiuje się je w **kwadratowych nawiasach**, zaś **wartości rozdziela się przecinkami**. Listy mogą przechowywać w sobie przedmioty różnego typu, ale często przechowuje się tylko jednego typu. 

```python
empty_list = [] #pusta lista
int_list = [1, 2, 3] #lista liczb całkowitych
str_list = ["1", "2", "3"] #lista napisów
```

Listy oraz napisy moga być indeksowane (indeksowanie zaczynamy od 0)
```python
list[index]
```
Indeksowanie może przyjmować wartości ujemne (wtedy odczytujemy wartości z końca).

Możemy odwołać się do przedziału z listy przy pomocy zapisu
```python
list[początek:koniec]
```

Funkcja 
```python
len(lista)
```
zwraca długość listy


```python
lista = [1, 2, 3, 4, 5]
print(lista)
print(lista[0])
print(lista[4]) #Podanie 5 wyrzuci wyjątek przekroczenia zakresu listy!!!
print(lista[-1]) #Ostatnia wartość z listy
print(lista[0:3]) #Koniec jest przedziałem otwartym, nie uwzględniamy go
print(lista[:]) #Wyświetli cały zakres
print(len(lista)) #Długość listy
print(lista[0:len(lista)]) #Wyświetli cały zakres
print(lista[::-1]) #Wyświetli odwróconą listę

```

    [1, 2, 3, 4, 5]
    1
    5
    5
    [1, 2, 3]
    [1, 2, 3, 4, 5]
    5
    [1, 2, 3, 4, 5]
    [5, 4, 3, 2, 1]
    

Analogiczne zachowanie w przypadku napisu


```python
napis = "Hello"
print(napis)
print(napis[0])
print(napis[4]) #Podanie 5 wyrzuci wyjątek przekroczenia zakresu listy!!!
print(napis[-1]) #Ostatnia wartość z listy
print(napis[0:3]) #Koniec jest przedziałem otwartym, nie uwzględniamy go
print(napis[:]) #Wyświetli cały zakres
print(len(napis)) #Długość listy
print(napis[0:len(napis)]) #Wyświetli cały zakres
print(napis[::-1]) #Wyświetli odwróconą listę
```

    Hello
    H
    o
    o
    Hel
    Hello
    5
    Hello
    olleH
    

Funkcja 
```python
lista.append(obiekt)
```
dodaje obiekt do listy

Funckja
```python
del lista[indeks]
```
usuwa obiekt z podanego indeksu z listu


```python
lista = []
print(lista)
lista.append(1)
lista.append(2)
lista.append(3)
print(lista)
del lista[2]
print(lista)
```

    []
    [1, 2, 3]
    [1, 2]
    

### Krotki
Innym typem struktury danych jest krotka (tuple), która w przeciwieństwie do listy jest niemodyfikowalna, nie można zmodyfikować wartości w niej przechowywanych.

Definiuje się ją poprzez wartości rozdzielone przecinkami

```python
krotka = przedmiot1, przedmiot2, przedmiot3
```

Bardzo często stosuje się operacje odwrotną, gdy na przykład jakaś funkcja zwraca wiele wyników, a my chcemy przypisać je do pojedynczych zmiennych

```python
zmienna1, zmienna2 = funkcja_zwracająca_dwa_wyniki()
```


```python
krotka = 1, 2, 3
print(krotka)
print(krotka[0])
```

    (1, 2, 3)
    1
    


```python
krotka[0] = 3 #Błąd, krotka jest niemodyfikowalna
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-13-8458fb98f811> in <module>()
    ----> 1 krotka[0] = 3 #Błąd, krotka jest niemodyfikowalna
    

    TypeError: 'tuple' object does not support item assignment


### Zbiory
Zbiór to nieuporządkowana kolekcja bez duplikatów. Przy dodawaniu elementu, sprawdzane więc jest czy przypadkiem nie istnieje już w zbiorze. Zbiory można sumować, znajdować ich część wspólną oraz obliczać różnicę.
Zbiory defniuje się przy pomocy słowa kluczowego
```python
set(zbior_obiektów)
```
bądź przy pomocy nawiasów
>{ }


```python
koszyk_Nowaka = {'jablko', 'pomarancz', 'jablko', 'gruszka', 'pomarancz', 'banan'}
koszyk_Kowalskiego = {'jablko', 'winogrona', 'banan'}

print(koszyk_Nowaka) #usunięto duplikaty
print(koszyk_Nowaka | koszyk_Kowalskiego) #suma zbiorów
print(koszyk_Nowaka & koszyk_Kowalskiego) #część wspólna zbiorów
print(koszyk_Nowaka ^ koszyk_Kowalskiego) #obiekty znajdujące się w jednym zbiorze ale nie w obu
print(koszyk_Nowaka - koszyk_Kowalskiego) #obiekty znajdujące się w zbiorze Nowaka ale nie ma ich u Kowalskiego
```

    {'banan', 'pomarancz', 'jablko', 'gruszka'}
    {'pomarancz', 'banan', 'jablko', 'gruszka', 'winogrona'}
    {'banan', 'jablko'}
    {'pomarancz', 'gruszka', 'winogrona'}
    {'pomarancz', 'gruszka'}
    

### Słowniki
Słownik to zbiór par typu 
>klucz: wartość
z zaznaczeniem, że wartości kluczy są unikatowe.

Głównymi operacjami na słowniku jest odczytywanie wartości poprzez podanie klucza.


```python
samochod =	{
  "marka": "Ford",
  "model": "Mustang",
  "rok_produkcji": 1964
}
```


```python
print(samochod)
```

    {'marka': 'Ford', 'model': 'Mustang', 'rok_produkcji': 1964}
    


```python
print(samochod['model']) #odczytanie konkretnej wartości poprzez podanie klucza
```

    Mustang
    


```python
samochod['model'] = "Mustang II" #modyfikacja wartości
print(samochod)
```

    {'marka': 'Ford', 'model': 'Mustang II', 'rok_produkcji': 1964}
    


```python
samochod['cena'] = 10000 #dodanie nowego klucza wraz z wartością
```


```python
print(samochod)
```

    {'marka': 'Ford', 'model': 'Mustang II', 'rok_produkcji': 1964, 'cena': 10000}
    

#### Więcej informacji o strukturach danych:
> [https://docs.python.org/3/tutorial/datastructures.html](https://docs.python.org/3/tutorial/datastructures.html)

## [2. Podstawowe operacje](#podstawy) {#operacje}
Poniżej lista kilku podstawowych operacji, które przydadzą nam się potem

* Dodawanie


```python
print(5 + 3)
print(5.0 + 3.0)
print((5.0 + 0j) + (3.0 + 2j)) #Liczby zespolone należy otoczyć nawiasem
print("Hello " + "world") #Łączenie napisów

```

    8
    8.0
    (8+2j)
    Hello world
    

* Odejmowanie


```python
print(5 - 3)
print(5.0 - 3.0)
print((5.0 + 0j) - (3.0 + 2j))
```

    2
    2.0
    (2-2j)
    

* Mnożenie


```python
print(5 * 3)
print(5.0 * 3.0)
print((5.0 + 0j) * (3.0 + 2j))
print("Hello " * 3 ) #Powtarzanie napisu
```

    15
    15.0
    (15+10j)
    Hello Hello Hello 
    

* Dzielenie



```python
print(5 / 3) #Dzielenie zwraca wynik zmiennoprzecinkowy
print(5.0 / 3.0)
print((5.0 + 0j) / (3.0 + 2j))
```

    1.6666666666666667
    1.6666666666666667
    (1.153846153846154-0.7692307692307692j)
    

* Dzielenie bez reszty


```python
print(5 // 3)
print(5.0 // 3.0)
```

    1
    1.0
    

* Reszta z dzielenia (modulo)


```python
print(5 % 3)
print(5.0 % 3.0)
```

    2
    2.0
    

* Potęgowanie


```python
print(5 ** 3)
print(5.0 ** 3.0)
print((5.0 + 0j) ** (3.0 + 2j))
```

    125
    125.0
    (-124.62689272475588-9.650782857996035j)
    

## [3. Warunek if](#podstawy) {#if}

Do tworzenia warunków stosuje się klauzulę if. Ważne w zapisie jest to by po warunku postawić znak 
>:

Zaś warunek musi być wcięty 4 spacjami (z reguły odpowiada to dla 1 przycisku tab, dla skonfigurowanego IDE). Gdy wychodzimy z warunku, usuwamy wcięcie.

Następny sprawdzany warunek będzie nazywał się elif (w skrócie od else if). 
Zaś, jeżeli wszystkie warunki nie zostały spełnione program wejdzie do struktury else o ile taka została zdefiniowana

```python
if warunek:
  wykonaj_te_operacje_jezeli_spelniony_warunek
elif inny_warunek:
  pass #pass oznacza pustą operację, która nic nie robi
else:
  w_pozostalych_przypadkach_zrob_to
```

**Warunek if i elif są wykluczające się (jeżeli nasze zapytanie spełnia oba warunki, to wejdzie do pierwszego z nich). Jeżeli chcemy tego uniknąć musimy używać szeregu ifów.**

### Operacje przyrównania

```python
 > - większe
 >= - większe równe
 == - równe
 <= - mniejsze równe
 < - mniejsze
 != - nierówne
```


```python
#zadeklarujmy liczbę
liczba = 10
```


```python
if liczba > 0:
  print("Liczba dodatnia")
elif liczba == 0:
  print ("Liczba jest zerem")
else:
  print("Liczba ujemna")
```

    Liczba dodatnia
    

Warunki możemy łączyć przy pomocy słów
> and

oraz
> or

W przypadku pierwszego oba warunki muszą być spełnione by program wszedł do wnętrza if'a. W przypadku drugiego co najmniej jeden z nich musi być spełniony


```python
liczba = 6
if (liczba % 2 == 0) and (liczba % 3 == 0):
  print("Liczba jest podzielna przez 2 i przez 3")

if (liczba > 0) or (liczba < 0):
  print("Liczba jest albo dodatnia, albo ujemna ¯\_(ツ)_/¯")
```

    Liczba jest podzielna przez 2 i przez 3
    Liczba jest albo dodatnia, albo ujemna ¯\_(ツ)_/¯
    

### Sprawdzanie czy dana rzecz znajduje się w przedziale, strukturze

Bardzo przydatną umiejętnością jest możliwość określenia czy coś znajduje się w zdefiniowanym przedziale, strukturze, która nas interesuje.

Wykorzystamy do tego słowo kluczowe
> in


```python
correct_answers = [4, 5, 6]
users_answer = int(input("Podaj wynik: "))
if users_answer in correct_answers:
  print("Prawidłowa odpowiedź")
else:
  print("Nieprawidłowa odpowiedź")


```

    Podaj wynik: 12
    Nieprawidłowa odpowiedź
    

## [4. Pętla for](#podstawy) {#for}

Jedną z charakterystycznych rzeczy w Pythonie jest sposób w jaki sposób działa w nim pętla for. W większości języków pętla ta wygląda następująco:
```
for(inicjalizacja, warunek końca pętli, operacje wykonane po każdej iteracji)
```

Na przykład:

```
for(int i = 0; i<10; i++)
{
  [...]
}
```

W przypadku języka Python pętla for wygląda następująco
``` python
for zmienne in obiekt_na_ktorym_iterujemy:
```

Na przykład:


```python
lista = [1, 2, 3, 4, 5, 6, 7, 8]
for element in lista:
  print(element)
```

    1
    2
    3
    4
    5
    6
    7
    8
    

Do iterowania po sekwencji liczb służy funkcja range
```python
range(poczatek, koniec, krok)
```
gdzie:
* poczatek - początkowa wartość sekwencji (opcjonalna, domyślnie przyjmuje 0)
* koniec - końcowa wartość sekwencji (zakres otwarty, czyli range(7) dotrze do 6
* krok - o ile ma być większa/mniejsza następna liczba w sekwencji (opcjonalna, domyślnie 1)


```python
for i in range(3):
  print(i)
```

    0
    1
    2
    


```python
for j in range(0,3):
  print(j)
```

    0
    1
    2
    


```python
for k in range(0,3,1):
  print(k)
```

    0
    1
    2
    

Często iterując po jakimś obiekcie nadal chcemy mieć informacje o numerze iteracji. Do zliczania wykorzystywana jest metoda 
>enumerate

która opakujemy obiekt iterowany

Przykład:


```python
shopping_list = ["jablka", "pomarancze", "gruszki", "winogrona"]
for counter, element in enumerate(shopping_list):
  print(str(counter + 1)+" element: " + element)
```

    1 element: jablka
    2 element: pomarancze
    3 element: gruszki
    4 element: winogrona
    

Do pętli często wykorzystywane są dwa sformułowania
> break

oraz
>continue

Pierwsze powoduje całkowite wyjście z pętli, drugie zaś pomija dalszą część kodu w danej iteracji

Przykład:



```python
result = 0
for i in range(8):
  if i == 6:
    break
  if i%2 == 0:
    continue
  result += 1 # skrócony zapis result = result + 1
print(result)
```

    3
    

## [5. Funkcje](#podstawy) {#funkcje}

Często zdarza się, że jakąś czynność wykonujemy wielokrotnie, w takim celu możemy daną funkcjonalność zapisać jako funkcję.

Funkcje **def**iniuje się następująco:

```python
def nazwa_funkcji(parametry):
  operacje wykonywane w ramach funkcji
  return wynik funkcji # funkcja może nic nie zwracać, być bez returna
```

Zaś wywołanie odbywa się przez podanie nazwy funkcji, oraz wszystkich wymaganych parametrów
```python
nazwa_funkcji(parametry)
```

Definiując funkcje możemy ustawić parametrom wartości domyślne, które o ile użytkownik nie poda własnych będa używane

```python
def nazwa_funkcji(parametr1 = wartosc):
  [...]
```

Przy wywoływaniu funkcji parametry podajemy w takiej samej kolejności jak zostały zdefiniowane, jeżeli tak nie chcemy to możemy podawać nazwę parametru i jaką wartość mu przekazujemy

```python
# definicja
def nazwa_funkcji(parametr1, parametr2):
  [...]
# wywołanie
nazwa_funkcji(wartość dla parametr1, wartość dla parametr2)
#alternatywne wywołanie, tutaj kolejność nie ma znaczenia
nazwa_funkcji(parametr2=wartosc2, parametr1=wartosc1)
```

Przykład:


```python
def dodawanie(a, b):
  print("a: " + str(a))
  print("b: " + str(b))
  return a+b

print("Pierwsza wersja:")
print(dodawanie(2,3))
print("\nDruga wersja:")
print(dodawanie(b=3, a=2))
```

    Pierwsza wersja:
    a: 2
    b: 3
    5
    
    Druga wersja:
    a: 2
    b: 3
    5
    

## [6. Importowanie modułów](#podstawy) {#import}

W ramach warsztatów poznamy kilka bibliotek do Pythona. 
Część z nich jest już wbudowana i nie musimy ich instalować. W przypadku pozostałych będziemy musieli je pobrać.

Jeżeli korzystamy z Google Colab ten problem nas nie dotyczy (po prostu importujemy biblioteki).

W przypadku IDE jak PyCharm, może ono samo pobrać potrzebne biblioteki (poinformuje o braku biblioteki i zaproponuje jej zainstalowanie).

W pozostałych przypadkach musimy poradzić sobie sami.
Jednym z rozwiązań jest pip, manager pakietów dedykowany dla Pythona, zainstalowany wraz z Pythonem.

W pierwszym kroku musimy go na wszelki wypadek zaktualizować. Otwieramy konsole i wpisujemy:

1. Na systemach z rodziny Linux i MacOS:
```
pip install -U pip
```

2. Na systemach z rodziny Windows
```
python -m pip install -U pip
```

Następnie należy wejść na [stronę z pakietami Pythona](https://pypi.org), znaleźć interesującą nas bibliotekę i postępować zgodnie z instrukcjami

Na przykład:

Chcemy pobrać bibliotekę numpy.

1. Wchodzimy na powyższą stronę
2. W wyszukiwarce wpisujemy "numpy" naciskamy enter
3. Wchodzimy w interesujące nas wyszukanie
4. Na górze strony napisana jest komenda jaką należy wpisać w terminalu by zainstalować daną bibliotekę. Tutaj będzie to
```pip install numpy```
5. Możemy zaimportować bibliotekę do naszego programu


#### Importowanie bibliotek

By zaimportować bibliotekę należy użyć słowa kluczowego 
> import

Jeżeli do biblioteki chcemy odwoływać się w inny sposób niż jest nazwana możemy użyć słowa 

> as 

a nastepnie nadać własną nazwę.

Jeżeli interesuje nas tylko pewna funkcjonalność z biblioteki (nie chcemy importować całej) używamy składni

```python
from nazwa_biblioteki import co_chcemy_zimportować as nasza_nazwa
```

Przykład:


```python
import numpy as np

np.__version__ # sprawdzenie wersji pakietu
# np.version.version
```




    '1.18.5'



## [7. Rekomendowane strony](#podstawy) {#rekomendacje}

Celem tych warsztatów jest tylko pobieżne wprowadzenie do języka Python. Jeżeli chcesz zgłębić swoją wiedzę Internet oferuje wiele kursów, blogów, które mogą Ci pomóc w twojej drodze.

Poniżej zamieszczam listę linków, które wydają mi się być przydatnymi źródłami informacji
> 
  * [W3Schools](https://www.w3schools.com/python/)
  * [Docs](https://docs.python.org/3/tutorial/)
  * [(PL) Learn Python](https://www.learnpython.org/pl/) 
  * [(PL) Python 101](https://python101.readthedocs.io/pl/latest/)
  * [(PL)Django Girls](https://tutorial.djangogirls.org/pl/python_introduction/) 