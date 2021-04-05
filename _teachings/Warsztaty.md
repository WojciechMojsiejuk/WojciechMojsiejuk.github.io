---
layout: page
title: Introduction to Data Analysis with Python II
description: a project with a background image
img: /assets/img/teachings/intro_to_d_a/markus-spiske-FXFz-sW0uwo-unsplash.jpg
importance: 1
---


# Przygotowanie środowiska pracy
0. Podstawowe informacje
1. Instalacja
2. IDE
3. Jupyter notebook & Google Colab
4. Hello world

## 0. Podstawowe informacje
Python jest *interpretowanym*, *wieloparadygmatowym* językiem wysokiego poziomu do zastosowań ogólnych z *dynamicznym* i *silnym* typowaniem danych. 

* Interpretowany - skrypt programu **nie musi być** wcześniej **kompilowany**, podczas uruchamiania jest na bieżąco interpretowany przez wbudowany interpreter

* Wieloparadygmatowy - nie ma jednego podejścia (paradygmatu) w jakim należy używać tego języka, można pisać m.in. **obiektowo** jak i **strukturalnie** (na tych warsztatach skupimy się na tym ostatnim)

* Typowanie dynamiczne - przypisanie typu danych do wartości przechowywanych w zmiennych odbywa się w trakcie działania programu

* Typowanie silne - nie można wymusić dla jednego typu danych by automatycznie zachował się jako drugi typ danych (musimy dokonać konwersji typów o ile jest to możliwe)

Obecnie nadal istnieją dwie wersje Pythona (Python 2 oraz Python 3) różniące się, nie w pełni kompatybilne, lecz od 2020 roku **Python 2** przestał otrzymywać wspieranie. **Obecny kod powinien być więc pisany tylko i wyłącznie w wersji 3!**

 Istnieje wiele źródeł informacji pisanych w Pythonie 2, można je wykorzystywać mając świadomość, że część rzeczy może być inaczej realizowana w Pythonie 3, na przykład podejście do funkcji **print**.

## 1. Instalacja
W celu pobrania Pythona należy wejść na 
[oficjalną stronę dystrybutora](https://www.python.org/downloads/) i postępować z instrukcjami zgodnymi z systemem operacyjnym na którym pracujemy.

####Dodatkowe informacje przydatne do instalacji:
(PL)
https://tutorial.djangogirls.org/pl/installation/

#### Windows:
https://docs.python.org/3/using/windows.html

https://www.guru99.com/how-to-install-python.html


#### Linux:
https://tecadmin.net/install-python-3-8-ubuntu/

``` apt-get install python```

#### MacOS:
```brew install python```

## 2. IDE 
>IDE (*ang. integrated development environment*; *pol. zintegrowane środowisko programistyczne)* - zbiór narzędzi do tworzenia oprogramowania

Pomimo iż nic nie stoi na przeszkodzie, żebyśmy pisali programy w konsoli terminalu, dla ułatwienia naszej pracy możemy skorzystać z przeróżnych programów mających na celu ułatwienie nam pracy.

Ze swojej strony jako IDE mogę polecić [PyCharm](https://www.jetbrains.com/pycharm/) oferujące darmową wersję **Community** oraz płatną wersję **Professional**, która jest dostępna **za darmo dla wszystkich studentów naszej uczelni** (muszą oni wyrobić mail uczelniany, informacja sprawdzona dla 2019 roku).

Jest to dość potężne oprogramowanie, którego wszystkich dobrodziejstw nie wykorzystamy, lecz posiada bardzo dobry system podpowiedzi, który może być przydatny na początkowym etapie nauki tego języka.

## 3. Jupyter notebook & Google Colab

### Jupyter notebook 

Jupyter notebook to technologia która umożliwia nam tworzenie interaktywnych dokumentów w których możemy zagnieżdżać fragmenty kodu oraz je uruchamiać. Idealne rozwiązanie do wizualizacji danych, demonstracji kodu etc. 

To co właśnie czytasz to dokument utworzony w tej technologii!

Więcej informacji na ten temat możesz znaleźć m.in. [na stronie twórców](https://jupyter.org). Osobiście polecam instalacje tej technologii w ramach pakietu [Anaconda](https://www.anaconda.com/distribution/) zawierającej wszelkie potrzebne biblioteki jeżeli chcemy zacząć naszą przygodę z analizą danych w Pythonie.

### Google Colab

Google Colab jest rozwiązaniem Google które dostarcza i obsługuje środowisko Jupyter notebook. Dzięki temu nie musimy nic pobierać, instalować. Mamy gotowe środowisko do pracy :)

####Przydatne informacje:

* [Wprowadzenie do Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb)

* [(PL) Konfiguracja Google Colab - połączenie z GitHubem, zmiana runtime'u, ładowanie danych z Google Drive ](https://bulldogjob.pl/news/738-google-colab-pythonowy-obszar-roboczy-w-chmurze)

* [Tutorial Google Colab ze strony, którą bardzo wszystkim polecam](https://towardsdatascience.com/getting-started-with-google-colab-f2fff97f594c)

## 4. Hello world

Jeżeli udało nam się prawidłowo zainstalować i skonfigurować środowisko pracy należy napisać pierwszy program. W tym celu w utworzonym pliku o rozszerzeniu *.py (nie dotyczy to rozwiązania Jupyter) wklejamy poniższą linię:


```python
print("Hello world")
```

    Hello world
    

A następnie zapisujemy plik i uruchamiamy go przez nasze IDE, lub w konsoli otwartej w folderze gdzie znajduje się nasz zapisany plik (przykładowo *main.py*)

``` python main.py ```

lub

``` python3 main.py ```

Jeżeli wszystko poszło dobrze, to właśnie udało Ci się napisać pierwszy program w Pythonie :D


#Podstawy Pythona
0. Podstawowe typy danych i zmienne, podstawowe struktury danych
1. Podstawowe operacje
2. Warunek if
3. Pętla for
4. Funkcje
5. Importowanie modułów
6. Rekomendowane strony

## 0. Podstawowe typy danych i zmienne, podstawowe struktury danych
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
    

###Podstawowe struktury danych

####Listy

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
    

###Krotki
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
    

####Więcej informacji o strukturach danych:
https://docs.python.org/3/tutorial/datastructures.html

## 1. Podstawowe operacje
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
    

## 2. Warunek if

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

###Operacje przyrównania

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
    

###Sprawdzanie czy dana rzecz znajduje się w przedziale, strukturze

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
    

## 3. Pętla for

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
    

## 4. Funkcje

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
    

## 5. Importowanie modułów

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



## 6. Rekomendowane strony

Celem tych warsztatów jest tylko pobieżne wprowadzenie do języka Python. Jeżeli chcesz zgłębić swoją wiedzę Internet oferuje wiele kursów, blogów, które mogą Ci pomóc w twojej drodze.

Poniżej zamieszczam listę linków, które wydają mi się być przydatnymi źródłami informacji

* https://www.w3schools.com/python/
* https://docs.python.org/3/tutorial/
* (PL) https://www.learnpython.org/pl/
* (PL) https://python101.readthedocs.io/pl/latest/
* (PL) https://tutorial.djangogirls.org/pl/python_introduction/



#Podstawy analizy danych
0. Numpy
1. Matplotlib
2. Pandas
3. Math & Scipy
4. ~OpenCV~
5. ~Tensorflow & Scikit-learn~



#0. Numpy
---------

0. Podstawowe informacje
1. Ndarray
2. Podstawowe operacje na tablicach wielowymiarowych
3. Algebra liniowa


## 0. Podstawowe informacje

**NumPy** to skrót od *Numerical Python*, jest to podstawowa biblioteka do obliczeń liczbowych w Pythonie. Większość bibliotek zorientowanych naukowo silnie współpracuje z obiektami tablicowymi Numpy dlatego opanowanie podstaw tej biblioteki jest esencjonalnie związane z dalszą podróżą w analizę danych. Częściowo napisana w C/C++ umożliwia szybkie operacje na danych. Operacje pakietu Numpy mogą w złożony sposób przetwarzać całe tablice bez wykorzystywania pętli.

Przydatne linki:

* https://numpy.org

* https://numpy.org/doc/1.17/user/quickstart.html

* https://docs.scipy.org/doc/numpy/user/index.html

* https://docs.scipy.org/doc/numpy-1.13.0/reference/routines.html


* https://towardsdatascience.com/the-easiest-python-numpy-tutorial-ever-5c206c809a0d


Porównanie wydajności:



```python
import numpy as np
numpy_array = np.arange(1000000)
python_list = list(range(1000000))

%time for _ in range(10): npa_2 = numpy_array * 2
```

    CPU times: user 13 ms, sys: 4 ms, total: 17 ms
    Wall time: 21.3 ms
    


```python
%time for _ in range(10): pl_2 = [x * 2 for x in python_list]
```

    CPU times: user 612 ms, sys: 160 ms, total: 773 ms
    Wall time: 776 ms
    

## 1. Ndarray

**Ndarray** - ***n*** ***d*** *immensional* ***array*** (*pol. tablica n-wymiarowa*)

Jest podstawowym obiektem biblioteki Numpy. Jest to kontener przeznaczony do przechowywania dużych zbiorów danych.

**Syntax:**
``` python
class numpy.ndarray(shape, dtype, ...)
```
>**shape** - wymiary utworzonej tablicy

>**dtype** - typ danych przechowywanych w tablicy (cała tablica przechowuje tylko jeden)

Tablice n-wymiarowe można tworzyć z wcześniej utworzonych list lub krotek pythonowych przy pomocy polecenia 

```python
np.array()
```

Przykład:



```python
import numpy as np

lista = [1, 2, 3, 4]
nd_arr = np.array(lista)
print(nd_arr)
print(type(nd_arr)) # typ 
print(nd_arr.shape) # wymiary
print(nd_arr.dtype) # typ danych przechowywanych
```

    [1 2 3 4]
    <class 'numpy.ndarray'>
    (4,)
    int64
    


```python
nd_arr_2 = np.ndarray(lista)
print(nd_arr_2)
print(type(nd_arr_2)) # typ 
print(nd_arr_2.shape) # wymiary
print(nd_arr_2.dtype) # typ danych przechowywanych
```

    [[[[1.601345e-316 5.075659e-317 7.213358e-322           nan]
       [0.000000e+000 0.000000e+000 0.000000e+000 0.000000e+000]
       [0.000000e+000 0.000000e+000 0.000000e+000 0.000000e+000]]
    
      [[0.000000e+000 0.000000e+000 0.000000e+000 0.000000e+000]
       [0.000000e+000 0.000000e+000 0.000000e+000 0.000000e+000]
       [0.000000e+000 0.000000e+000 0.000000e+000 0.000000e+000]]]]
    <class 'numpy.ndarray'>
    (1, 2, 3, 4)
    float64
    

Zwróćmy uwagę na wymiary (1, 2, 3, 4)

* 1 klamra zawierająca 2 klamry,

* zawierajace 3 klamry,

* zawierajace 4 wartości losowe.

Nasz parametr listy został zinterpretowany jako shape !!!


```python

nd_arr_3 = np.ndarray(shape=(4,1), dtype=int)
print(nd_arr_3)
print(type(nd_arr_3)) # typ 
print(nd_arr_3.shape) # wymiary
print(nd_arr_3.dtype) # typ danych przechowywanych
```

    [[4607182418800017408]
     [4607182418800017408]
     [4607182418800017408]
     [                  0]]
    <class 'numpy.ndarray'>
    (4, 1)
    int64
    

By lepiej zrozumieć kształt n-wymiarowych tablic, przestudiujmy poniższe zdjęcie:


```python
import matplotlib.pyplot as plt
import cv2
from google.colab import drive
from google.colab.patches import cv2_imshow
drive.mount('/content/drive')
image = cv2.imread('/content/drive/My Drive/Warsztaty/axes.png')
cv2_imshow(image)
```

    Mounted at /content/drive
    


![png](output_88_1.png)


**Wymiary** w ndarray nazywane są **axes** (*l. poj.* axis). 

Jakie wymiary będą miały poniższe przykłady?



```python
import numpy as np
ex_1 = np.array([[ 1., 0., 0.],[ 0., 1., 2.]])
ex_2 = np.array([[1, 1]])
ex_3 = np.array([[]])
ex_4 = np.array([1, 2, 3])
ex_5 = np.array([])
ex_6 = np.array([[ 0,  1,  2,  3,  4],
       [ 5,  6,  7,  8,  9],
       [10, 11, 12, 13, 14]])

print(ex_1.shape)
print(ex_2.shape)
print(ex_3.shape)
print(ex_4.shape)
print(ex_5.shape)
print(ex_6.shape)
```

    (2, 3)
    (1, 2)
    (1, 0)
    (3,)
    (0,)
    (3, 5)
    

###Dodatkowe parametry:
>ndim - zwraca liczbę *axes*, wymiarów

>size - zwraca liczbę elementów w tablicy

Przykład:


```python
nd_arr = np.array([[ 0,  1,  2,  3,  4],
                   [ 5,  6,  7,  8,  9],
                   [10, 11, 12, 13, 14]])
print(nd_arr.shape)
print(nd_arr.ndim)
print(nd_arr.size)
```

    (3, 5)
    2
    15
    

## 2. Podstawowe operacje na tablicach wielowymiarowych

### Operacje arytmetyczne
Operacje arytmetyczne są zawsze wykonywane *elementwise* (na poszczególnych elementach)



```python
'''
Przykład wykorzystany w książce Uczenie maszynowe z użyciem Scikit-Learn i TensorFlow Helion 2018
'''
import numpy as np
import matplotlib.pyplot as plt # biblioteka wykorzystywana do tworzenia wykresów, więcej powiemy o niej później

u = np.array([5, 2])
v = np.array([1, 6])

''' 
Funkcja odpowiadająca za narysowanie strzałki wskazującej pozycję wektora od początku
Domyślnie początek jest ustawiony na koordynaty (0, 0)
'''
def rysuj_wektor(wektor, poczatek=[0, 0], **options): 
    return plt.arrow(poczatek[0], poczatek[1], wektor[0], wektor[1],
              head_width=0.3, head_length=0.4, length_includes_head=True,
              **options)

```


```python
rysuj_wektor(u, color="r")
rysuj_wektor(v, color="b")
plt.axis([0, 6, 0, 7])
plt.grid()
plt.text(2.5, 1.2, "u", color="r", fontsize=18)
plt.text(0.3, 3.5, "v", color="b", fontsize=18)
plt.show()

```


![png](output_96_0.png)


####Dodawanie

$c_{ij} = a_{ij} + b_{ij}$

>$A_{m,n} + B_{m,n} =\begin{pmatrix}
  a_{1,1} & \cdots & a_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  a_{m,1} & \cdots & a_{m,n}
 \end{pmatrix}
+
 \begin{pmatrix}
  b_{1,1}  & \cdots & b_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  b_{m,1} & \cdots & b_{m,n}
 \end{pmatrix}
 =
 \begin{pmatrix}
  a_{1,1} + b_{1,1}  & \cdots & a_{1,n} + b_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  a_{m,1} + b_{m,1} & \cdots & a_{m, n} + b_{m,n}
 \end{pmatrix}
 $

 Przykłady:


```python
rysuj_wektor(u, color="r")
rysuj_wektor(v, color="b")
rysuj_wektor(v, poczatek=u, color="b", linestyle="dotted")
rysuj_wektor(u, poczatek=v, color="r", linestyle="dotted")
rysuj_wektor(u+v, color="g")
plt.axis([0, 7, 0, 9])
plt.text(2.5, 1.2, "u", color="r", fontsize=18)
plt.text(0.3, 3.5, "v", color="b", fontsize=18)
plt.text(2.4, 2.5, "u+v", color="g", fontsize=18)
plt.grid()
plt.show()
```


![png](output_98_0.png)



```python

a = np.array( [20,30,40,50] )
b = np.array( [0, 1, 2, 3,] )
c = a + b
print(c)
```

    [20 31 42 53]
    


```python
a = np.array( [[5,10],[-3, 0]])
b = np.array( [[7, 2], [2, 3,]] )
c = a + b
print(c)
```

    [[12 12]
     [-1  3]]
    

####Odejmowanie

$c_{ij} = a_{ij} - b_{ij}$

>$A_{m,n} - B_{m,n} =\begin{pmatrix}
  a_{1,1} & \cdots & a_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  a_{m,1} & \cdots & a_{m,n}
 \end{pmatrix}
-
 \begin{pmatrix}
  b_{1,1}  & \cdots & b_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  b_{m,1} & \cdots & b_{m,n}
 \end{pmatrix}
 =
 \begin{pmatrix}
  a_{1,1} - b_{1,1}  & \cdots & a_{1,n} - b_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  a_{m,1} - b_{m,1} & \cdots & a_{m, n} - b_{m,n}
 \end{pmatrix}
 $

 Przykłady:


```python
a = np.array( [20,30,40,50] )
b = np.array( [0, 1, 2, 3,] )
c = a - b
print(c)
```

    [20 29 38 47]
    


```python
a = np.array( [[5,10],[-3, 0]])
b = np.array( [[7, 2], [2, 3,]] )
c = a - b
print(c)
```

    [[-2  8]
     [-5 -3]]
    

####Mnożenie przez skalar

$c_{ij} = a_{ij} \cdot r $

>$(rA_{m,n})=r\cdot\begin{pmatrix}
  a_{1,1} & \cdots & a_{1,n} \\
  \vdots  & \ddots & \vdots  \\
  a_{m,1} & \cdots & a_{m,n}
 \end{pmatrix}
 =
 \begin{pmatrix}
  r\cdot a_{1,1} & \cdots & r\cdot a_{1,n}\\
  \vdots  & \ddots & \vdots  \\
  r\cdot a_{m,1} & \cdots & r\cdot a_{m, n}
 \end{pmatrix}
 $

 Przykłady:


```python
a = np.array( [20,30,40,50] )
r = 10
c = a*r
print(c)
```

    [200 300 400 500]
    


```python
a = np.array( [[1, 2, 3],[4, 5, 6]] )
r = 0.25
c = a*r
print(c)
```

    [[0.25 0.5  0.75]
     [1.   1.25 1.5 ]]
    


```python
a = np.array( [[10, 20],[30, 40]] )
r = 10
c = a/r # dzielenie macierzy = mnożenie przez odwrotność
print(c)
```

    [[1. 2.]
     [3. 4.]]
    

####Mnożenie tablic
Trzeba szczególnie uważać na mnożenie tablic między sobą.

Domyślna operacja 
> *

Zwróci nam następujące wartości

$c_{ij} = a_{ij} \cdot b_{ij} $

Przykład:


```python
a = np.array( [20,30,40,50] )
b = np.array( [0, 1, 2, 3] )
c = a * b
print(c)
```

    [  0  30  80 150]
    

Gdy interesuje nas mnożenie Cauchy'ego zdefiniowane w następujący sposób:


$c_{i,j}=\sum_{r=1}^m a_{i,r}b_{r,i}$

Musimy użyć funkcji
```python
np.matmul(pierwsza_macierz, druga_macierz)
```
bądź operatora
> @

Działanie to zdefiniowane jest wyłącznie dla macierzy, z których pierwsza ma tyle kolumn, co druga wierszy. 

Przykład:


```python
a = np.array( [[1,2],[3,0]] )
b = np.array( [[0, 1], [2, 3]] )
c = a @ b
print(c)
c = np.matmul(a,b)
print(c)
```

    [[4 7]
     [0 3]]
    [[4 7]
     [0 3]]
    


```python
a = np.array( [[1,2]] )
b = np.array( [[0, 1], [2, 3]] )
c = b@a
print(c)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-109-9cab40bd7661> in <module>()
          1 a = np.array( [[1,2]] )
          2 b = np.array( [[0, 1], [2, 3]] )
    ----> 3 c = b@a
          4 print(c)
    

    ValueError: matmul: Input operand 1 has a mismatch in its core dimension 0, with gufunc signature (n?,k),(k,m?)->(n?,m?) (size 1 is different from 2)


### **Nakładanie funkcji na tablice**

Numpy umożliwia nakładanie funkcji na każdy element tablicy

Przykład


```python
a = np.array( [0, 1, 2, 3] )
b = a**2 # potęgowanie
print(b)
```

    [0 1 4 9]
    


```python
a = np.array( [0, np.pi/2, np.pi, 3/2*np.pi] )
b = np.round(np.sin(a)) # wyliczanie sinusa i zaokrągranie wartości
print(b)
```

    [ 0.  1.  0. -1.]
    


```python
import numpy as np
a = np.array( [20,30,40,50] )
print(a.max()) # znajduje maksymalną wartość
print(a.min()) # znajduje minimalną wartość
print(a.sum()) # sumuje wartości
print(a.prod()) # zwraca iloczyn
print(a.mean()) # zwraca średnią
print(a.std()) # zwraca odchylenie standardowe
print(a.var()) # zwraca wariancję
```

    50
    20
    140
    1200000
    35.0
    11.180339887498949
    125.0
    

W przypadku tablicy wielowymiarowej często trzeba określić względem jakiego wymiaru operacje mają się wykonywać


```python
b = np.array([[ 0,  1,  2,  3],
              [ 4,  5,  6,  7],
              [ 8,  9, 10, 11]])

print(b.sum(axis=0))
print(b.sum(axis=1))
```

    [12 15 18 21]
    [ 6 22 38]
    

Więcej funkcji można znaleźć [tutaj](https://docs.scipy.org/doc/numpy-1.13.0/reference/routines.math.html)

## Funkcje tworzące tablice

Numpy umożliwia wiele możliwości tworzenia tablic wypełnionymi konkretnymi danymi

Funkcja
>zeros 

tworzy tablice pełną zer.

Funkcja
>ones

tworzy tablicę pełną jedynek.

Funkcja
>empty 

tworzy tablicę której zainicjalizowana wartość jest losowa, zależna od tego co jest przechowywane w pamięci.

Wymiary tablicy muszą być podawane w nawiasach!

```python
np.zeros((wymiar1, wymiar2), dtype=typ)
```

Domyślnie dtype wszystkich tych funkcji jest floatem (liczby zmiennoprzecinkowe), ale można go zdefiniować oraz podać ilość obiektów w jednej komórce.

Przykład:


```python
np.zeros( (3,4) )
```




    array([[0., 0., 0., 0.],
           [0., 0., 0., 0.],
           [0., 0., 0., 0.]])




```python
np.ones( (3,4), dtype=int)
```




    array([[1, 1, 1, 1],
           [1, 1, 1, 1],
           [1, 1, 1, 1]])




```python
np.empty( (3,4) )
```




    array([[5.97074934e-316, 0.00000000e+000, 4.11556683e-321,
            1.59254195e-316],
           [6.92303567e-310, 6.92303567e-310, 6.92303567e-310,
            6.92303567e-310],
           [0.00000000e+000, 2.96439388e-323, 2.12199579e-314,
            6.92303731e-310]])




```python
a = np.zeros( (1,2), dtype=(int,2))
print(a) # w każdej komórce przechowywane są dwa obiekty typu int
print(a.shape) # zwróćmy uwagę na wymiary!
```

    [[[0 0]
      [0 0]]]
    (1, 2, 2)
    

Jeżeli chcemy zainicjować tablice wartościami z pewnego przedziału możemy wykorzystać funkcję
>arange

będącą funkcją zbliżoną do funkcji range w Pythonie

```python
np.arange(od, do, krok)
```
Przykład:


```python
print(np.arange( 10, 30, 5 ))
print(np.arange(6))
```

    [10 15 20 25]
    [0 1 2 3 4 5]
    

Bądź funkcję
>linspace

która zwraca n liczb z pewnego przedziału z równym odstępem (w tym przypadku początek jak i koniec są domknięte)

```python
np.linspace(od, do, ile_liczb)
```
Przykład:



```python
np.linspace( 0, 2, 9 )
```




    array([0.  , 0.25, 0.5 , 0.75, 1.  , 1.25, 1.5 , 1.75, 2.  ])



Jeżeli chcemy uzupełnić tablicę wartościami pseudolosowymi zastosujemy funkcję random 
```python
np.random.random((wymiar1, wymiar2))
```
zwracającą wartości z przedziału 0 - 1
Przykład:


```python
np.random.random((2,3))
```




    array([[0.72096784, 0.15166739, 0.62780155],
           [0.14470733, 0.5110661 , 0.3135805 ]])



## Funkcje modyfikujące wymiary tablicy

Inną, dość częstą operacją jaką będziemy stosować na naszej tablicy to zmiana jej wymiarów.

Do zmiany wymiarów tablicy wykorzystywana jest funkcja 
>reshape

która jako parametr otrzymuje nowe wymiary tablicy

```python
n_wym_tablica.reshape(nowe_wymiary)
```

Przykład:



```python
a = np.arange(12)
print(a)
print(a.shape)
a = a.reshape(3,4)
print(a)
print(a.shape)
```

    [ 0  1  2  3  4  5  6  7  8  9 10 11]
    (12,)
    [[ 0  1  2  3]
     [ 4  5  6  7]
     [ 8  9 10 11]]
    (3, 4)
    

Do spłaszczenia tablicy do jednego wymiaru służy funkcja
>ravel
```python
np.ravel(tablica_do_spłaszczenia)
```
Przykład:


```python
print(a)
print(a.shape)
print(np.ravel(a))
print(np.ravel(a).shape)
```

    [[ 0  1  2  3]
     [ 4  5  6  7]
     [ 8  9 10 11]]
    (3, 4)
    [ 0  1  2  3  4  5  6  7  8  9 10 11]
    (12,)
    

Bardzo często przy pracy na macierzach interesuje nas transpozycja macierzy.

Do dokonania transpozycji służy funkcja
>transpose

albo parametr
>T

Przykład:


```python
a = np.arange(15).reshape(3,5)
print(a)
print(a.shape)
print(a.T)
print(a.T.shape)
b = a.transpose()
print(b)
print(b.shape)
```

    [[ 0  1  2  3  4]
     [ 5  6  7  8  9]
     [10 11 12 13 14]]
    (3, 5)
    [[ 0  5 10]
     [ 1  6 11]
     [ 2  7 12]
     [ 3  8 13]
     [ 4  9 14]]
    (5, 3)
    [[ 0  5 10]
     [ 1  6 11]
     [ 2  7 12]
     [ 3  8 13]
     [ 4  9 14]]
    (5, 3)
    

## 3. Algebra liniowa



Pakiet numpy posiada całkiem zaawansowaną część poświęconą algebrze liniowej.

Wprawa w tej dziedzinie (chociażby na poziomie podstawowym) jest konieczna w analizie danych. Wiele operacji, algorytmów wykonywanych jest na macierzach w celu przyspieszenia czasu wykonywania.

Rozpiskę wszystkich funkcji oferowanych przez numpy dotyczących algebry liniowej można znaleźć [tutaj](https://docs.scipy.org/doc/numpy/reference/routines.linalg.html)



### Norma
Norma wektora $\textbf{u}$, zapisywana jako $\left \Vert \textbf{u} \right \|$, stanowi miarę długośc (tzn. modułu) wektora $\textbf{u}$. Istnieje wiele różnych norm, najczęściej jednak stosowaną jest norma euklidesowa, definiowana jako:

$\left \Vert \textbf{u} \right \| = \sqrt{\sum_{i}{\textbf{u}_i}^2}$


```python
def norma_wektora(wektor): # własnoręcznie napisana funkcja do wyliczania normy
    return sum([element**2 for element in wektor])**0.5
```


```python
u = np.array([3, 4])

print(norma_wektora(u))
```

    5.0
    

Możemy też wykorzystać do tego problemu bibliotekę Numpy, a dokładniej metodę

```python
numpy.linalg.norm(wektor)
```


```python
import numpy.linalg as LA
LA.norm(u)
```




    5.0



**Wektor znormalizowany** wektora niezerowego $\textbf{u}$, zapisywany jako $\hat{\textbf{u}}$, jest wektorem jednostkowym skierowanym w tę samą stronę, co wektor $\textbf{u}$. Jest on równy:
> $\hat{\textbf{u}} = \dfrac{\textbf{u}}{\left \Vert \textbf{u} \right \|}$


```python
plt.gca().add_artist(plt.Circle((0,0),1,color='c'))
plt.plot(0, 0, "ko")
rysuj_wektor(u / LA.norm(u), color="k")
rysuj_wektor(u, color="b", linestyle=":")
plt.text(0.3, 0, "$\hat{u}$", color="k", fontsize=18)
plt.text(1.5, 1.7, "$u$", color="b", fontsize=18)
plt.axis([0, 7, 0, 5])
plt.grid()
plt.show()
```


![png](output_145_0.png)


### Iloczyn skalarny
(*ang. dot product*) definiujemy w następujący sposób:

>$\textbf{u} \cdot \textbf{v} = \left \Vert \textbf{u} \right \| \times \left \Vert \textbf{v} \right \| \times cos(\theta)$

gdzie:

* $\theta$ - kąt pomiędzy wektorami $\textbf{u}$ i $\textbf{v}$.

Możemy obliczyć go przy pomocy poniższego polecenia
```python
np.dot(wektor1, wektor2)
```



```python
u = np.array([2, 0])
v = np.array([4, 0])

rysuj_wektor(u, color="k")
rysuj_wektor(v, color="b", linestyle=":")
rysuj_wektor([np.dot(u,v),0], color="r")
plt.text(0.3, 0.1, "$u$", color="k", fontsize=18)
plt.text(2.5, 0.1, "$v$", color="b", fontsize=18)
plt.text(4.5, 0.1, "$u \cdot v$", color="r", fontsize=18)
plt.axis([0, 8, -2, 2])
plt.grid()
plt.show()
```


![png](output_147_0.png)



```python
print(np.dot(u,v))
```

    8
    

### Rzutowanie punktu na oś
Iloczyn skalarny jest również używany do rzutowania punktów na oś. Rzutowanie wektora $\textbf{v}$ na oś $\textbf{u}$ jest przeprowadzane za pomocą następującego równania:

$\textbf{proj}_{\textbf{u}}{\textbf{v}} = \dfrac{\textbf{u} \cdot \textbf{v}}{\left \Vert \textbf{u} \right \| ^2} \times \textbf{u}$

Co jest równoważne wzorowi:

$\textbf{proj}_{\textbf{u}}{\textbf{v}} = (\textbf{v} \cdot \hat{\textbf{u}}) \times \hat{\textbf{u}}$


```python
u = np.array([7, 0])
v = np.array([3, 4])

u_normalized = u / LA.norm(u)
proj = np.dot(v, u_normalized) * u_normalized

rysuj_wektor(u, color="r")
rysuj_wektor(v, color="b")

rysuj_wektor(proj, color="k", linestyle=":")
plt.plot(proj[0], proj[1], "ko")

plt.plot([proj[0], v[0]], [proj[1], v[1]], "b:")

plt.text(1, 0.2, "$rzut_u v$", color="k", fontsize=18)
plt.text(1.5,2.5, "$v$", color="b", fontsize=18)
plt.text(5, 0.2, "$u$", color="r", fontsize=18)

plt.axis([0, 8, -0.5, 4.5])
plt.grid()
plt.show()
```


![png](output_150_0.png)


### Obliczanie kąta pomiędzy wektorami
Jednym z wielu zastosowań iloczynu skalarnego jest obliczanie kąta pomiędzy dwoma niezerowymi wektorami. Za pomocą definicji iloczynu skalarnego możemy wyznaczyć następujący wzór:

$\theta = \arccos{\left ( \dfrac{\textbf{u} \cdot \textbf{v}}{\left \Vert \textbf{u} \right \| \times \left \Vert \textbf{v} \right \|} \right ) }$

Jeśli $\textbf{u} \cdot \textbf{v} = 0$, to $\theta = \dfrac{π}{2}$. Innymi słowy, jeśli iloczyn skalarny dwóch niezerowych wektorów jest równy 0, to znaczy, że są one prostopadłe względem siebie.

Skorzystajmy z tego wzoru do obliczenia kąta pomiędzy wektorami $\textbf{u}$ i $\textbf{v}$ (w radianach):


```python
def kat_wektora(u, v):
    cos_theta = np.dot(u,v) / (LA.norm(u) * LA.norm(v))
    return np.arccos(np.clip(cos_theta, -1, 1))

u = np.array([2, 5])
v = np.array([3, 1])

theta = kat_wektora(u, v)
print("Kąt =", theta, "radianów")
print("      =", theta * 180 / np.pi, "stopni")
```

    Kąt = 0.8685393952858896 radianów
          = 49.76364169072618 stopni
    

### Macierze

####Macierz diagonalna
**Macierz diagonalną**, na przykład:

\begin{bmatrix}
  4 & 0 & 0 \\
  0 & 5 & 0 \\
  0 & 0 & 6
\end{bmatrix}

możemy stworzyć za pomocą funkcji:
```python
np.diag(lista elementów mających pojawić się na głównej przekątnej)
```


```python
print(np.diag(np.array([1,2,3])))
```

    [[1 0 0]
     [0 2 0]
     [0 0 3]]
    

Jeśli zaś przekażemy macierz do funkcji diag, zostaną wypisane elementy znajdujące się w głównej przekątnej:


```python
D = np.array([
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
    ])
np.diag(D)
```




    array([1, 5, 9])



####Macierz jednostkowa
Macierz jednostkową (tożsamościową) o rozmiarze n definiujemy w następujący sposób.

```python
np.eye(n)
```

\begin{bmatrix}
  1 & 0 & 0 \\
  0 & 1 & 0 \\
  0 & 0 & 1
\end{bmatrix}


```python
print(np.eye(3))
```

    [[1. 0. 0.]
     [0. 1. 0.]
     [0. 0. 1.]]
    

#### Macierz transponowana
Transpozycją macierzy $M$ nazywamy macierz zapisywaną jako $M^T$, w której $i^{ty}$ rząd jest równy $i^{tej}$ kolumnie macierzy $M$:

$ A^T =
\begin{bmatrix}
  10 & 20 & 30 \\
  40 & 50 & 60
\end{bmatrix}^T =
\begin{bmatrix}
  10 & 40 \\
  20 & 50 \\
  30 & 60
\end{bmatrix}$

Innymi słowy ($A^T)_{i,j}$ = $A_{j,i}$

Oczywiście, jeśli macierz $M$ ma rozmiar $m \times n$, to jej transpozycja $M^T$ przyjmuje postać $n \times m$.

Macierz transponowaną za pomocą atrybutu T
```python
macierz.T
```
bądź funkcji 
```python
np.transpose(macierz)
```
która dodatkowo potrafi określić względem jakich osi ma zostać wykonana permutacja macierzy


```python
A = np.array([[10, 20, 30],[40, 50, 60]])

print('='*20)
print('atrybut T')
print('='*20)
print(A)
print('-'*20)
print(A.T)
print('-'*20)
print(A.T.T)
print('='*20)
print('funkcja transpose()')
print('='*20)
print(A)
print('-'*20)
print(np.transpose(A))
print('-'*20)
print(np.transpose(np.transpose(A)))
print('-'*20)

```

    ====================
    atrybut T
    ====================
    [[10 20 30]
     [40 50 60]]
    --------------------
    [[10 40]
     [20 50]
     [30 60]]
    --------------------
    [[10 20 30]
     [40 50 60]]
    ====================
    funkcja transpose()
    ====================
    [[10 20 30]
     [40 50 60]]
    --------------------
    [[10 40]
     [20 50]
     [30 60]]
    --------------------
    [[10 20 30]
     [40 50 60]]
    --------------------
    

#### Graficzne przedstawianie macierzy
Wektory mogą być reprezentowane jako punkty lub strzałki w N-wymiarowej przestrzeni. Jeżeli uznamy macierze za listy wektorów, to jej wykresem jest określona liczba punktów lub strzałek. Stwórzmy, na przykład, macierz $P$ o rozmiarze $2 \times 4$ i wygenerujmy jej wykres w postaci punktów:




```python
import matplotlib.pyplot as plt

P = np.array([
        [3.0, 4.0, 1.0, 4.6],
        [0.2, 3.5, 2.0, 0.5]
    ])
x_coords_P, y_coords_P = P
plt.scatter(x_coords_P, y_coords_P)
plt.axis([0, 5, 0, 4])
plt.show()
```


![png](output_162_0.png)


#### Zastosowania geometryczne operacji macierzowych
Dodawanie wektorów skutkuje procesem translacji geometrycznej, mnożenie wektorów przez skalar zmnienia skalę (powiększa lub pomniejsza, gdzie środek stanowi początek układu współrzędnych), natomiast iloczyn wektorowy skutkuje rzutowaniem wektora na inny wektor, co powoduje przeskalowanie i pomiar wynikowej współrzędnej.

Również operacje macierzowe mają bardzo użyteczne zastosowania geometryczne.

####Dodawanie macierzy


```python
from matplotlib.patches import Polygon

H = np.array([
        [ 0.5, -0.2, 0.2, -0.1],
        [ 0.4,  0.4, 1.5, 0.6]
    ])
P_moved = P + H

plt.gca().add_artist(Polygon(P.T, alpha=0.2))
plt.gca().add_artist(Polygon(P_moved.T, alpha=0.3, color="r"))
for vector, origin in zip(H.T, P.T):
    rysuj_wektor(vector, poczatek=origin)

plt.text(2.2, 1.8, "$P$", color="b", fontsize=18)
plt.text(2.0, 3.2, "$P+H$", color="r", fontsize=18)
plt.text(2.5, 0.5, "$H_{*,1}$", color="k", fontsize=18)
plt.text(4.1, 3.5, "$H_{*,2}$", color="k", fontsize=18)
plt.text(0.4, 2.6, "$H_{*,3}$", color="k", fontsize=18)
plt.text(4.4, 0.2, "$H_{*,4}$", color="k", fontsize=18)

plt.axis([0, 5, 0, 4])
plt.grid()
plt.show()
```


![png](output_165_0.png)


Dodanie macierzy wypełnionej identycznymi wektorami skutkuje prostą translacją geometryczną


```python
H2 = np.array([
        [-0.5, -0.5, -0.5, -0.5],
        [ 0.4,  0.4,  0.4,  0.4]
    ])
P_translated = P + H2

plt.gca().add_artist(Polygon(P.T, alpha=0.2))
plt.gca().add_artist(Polygon(P_translated.T, alpha=0.3, color="r"))
for vector, origin in zip(H2.T, P.T):
    rysuj_wektor(vector, poczatek=origin)

plt.axis([0, 5, 0, 4])
plt.grid()
plt.show()
```


![png](output_167_0.png)


####Mnożenie przez skalar


```python
def rysuj_translacje(P_przed, P_po, tekst_przed, tekst_po, axis = [0, 5, 0, 4], arrows=False):
    if arrows:
        for wektor_przed, wektor_po in zip(P_przed.T, P_po.T):
            rysuj_wektor(wektor_przed, color="blue", linestyle="--")
            rysuj_wektor(wektor_po, color="red", linestyle="-")
    plt.gca().add_artist(Polygon(P_przed.T, alpha=0.2))
    plt.gca().add_artist(Polygon(P_po.T, alpha=0.3, color="r"))
    plt.text(P_przed[0].mean(), P_przed[1].mean(), tekst_przed, fontsize=18, color="blue")
    plt.text(P_po[0].mean(), P_po[1].mean(), tekst_po, fontsize=18, color="red")
    plt.axis(axis)
    plt.grid()

P_przeskalowane = 0.60 * P
rysuj_translacje(P, P_przeskalowane, "$P$", "$0.6 P$", arrows=True)
plt.show()
```


![png](output_169_0.png)


#### Przekształcenia liniowe
W bardziej ogólnym ujęciu każde przekształcenie liniowe $f$ odwzorowujące n-wymiarowe wektory na m-wymiarowe wektory możemy przedstawiać za pomocą macierzy. Załóżmy, na przykład, że mamy do czynienia z trójwymiarowym wektorem $\textbf{u}$:

$\textbf{u} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$

a przekształcenie $f$ definiujemy jako:

$f(\textbf{u}) = \begin{pmatrix}
ax + by + cz \\
dx + ey + fz
\end{pmatrix}$

Transformacja ta odwzorowuje trójwymiarowe wektory do postaci dwuwymiarowej w sposób liniowy (tzn. otrzymywane współrzędne stanowią jedynie sumy iloczynów pierwotnych koordynatów). Możemy zapisać to przekształcenie jako macierz $F$:

$F = \begin{bmatrix}
a & b & c \\
d & e & f
\end{bmatrix}$

Teraz w celu obliczenia $f(\textbf{u})$ wystarczy przeprowadzić mnożenie macierzowe:

$f(\textbf{u}) = F \textbf{u}$

Jeśli mamy macierz $G = \begin{bmatrix}\textbf{u}_1 & \textbf{u}_2 & \cdots & \textbf{u}_q \end{bmatrix}$, gdzie każdy element $\textbf{u}_i$ stanowi trójwymiarowy wektor kolumnowy, to operacja $FG$ spowoduje liniowe przekształcenie wszystkich wektorów  $\textbf{u}_i$ w sposób zdefiniowany w macierzy $F$:

$FG = \begin{bmatrix}f(\textbf{u}_1) & f(\textbf{u}_2) & \cdots & f(\textbf{u}_q) \end{bmatrix}$

Podsumowując, macierz znajdująca się po lewej stronie iloczynu wektorowego określa stosowane przekształcenie liniowe wobec wektorów znajdujących się po prawej stronie.

##### Przykład

Zdefiniujmy macierz, która będzie reprezentowana przez kwadrat jednostkowy


```python
kwadrat = np.array([
        [0, 0, 1, 1],
        [0, 1, 1, 0]
    ])

plt.gca().add_artist(Polygon(kwadrat.T, alpha=0.2))
plt.axis([0, 2, 0, 2])
plt.show()
```


![png](output_172_0.png)


##### Mnożenie przez macierz jednostkową
nie zmienia właściwości macierzy

$\begin{bmatrix}
  1 & 0 \\
  0 & 1
\end{bmatrix}
\cdot
\begin{bmatrix}
  0 & 0 & 1 & 1\\
  0 & 1 & 1 & 0
\end{bmatrix}
=\begin{bmatrix}
  0 & 0 & 1 & 1\\
  0 & 1 & 1 & 0
\end{bmatrix}$



```python
macierz_jednostkowa = np.eye(2)
plt.gca().add_artist(Polygon(np.dot(macierz_jednostkowa, kwadrat).T, alpha=0.2))
plt.axis([0, 2, 0, 2])
plt.show()
```


![png](output_174_0.png)


##### Skalowanie

$\begin{bmatrix}
  szerokość & 0 \\
  0 & wysokość
\end{bmatrix}$





```python
szerokość = 2
wysokość = 2
skalowanie = np.array([[szerokość, 0],[0, wysokość]])

plt.gca().add_artist(Polygon(np.dot(skalowanie, kwadrat).T, alpha=0.2))
plt.axis([0, 2, 0, 2])
plt.show()
```


![png](output_176_0.png)


##### Rotacja

$\begin{bmatrix}
  \cos{\phi} & \sin{\phi} \\
  -\sin{\phi} & \cos{\phi}
\end{bmatrix}$

gdzie

* $\phi$ - kąt o jaki chcemy obrócić macierz względem osi OY





```python
rotacja = np.array([[np.cos(np.pi/6), np.sin(np.pi/6)],[-1*np.sin(np.pi/6), np.cos(np.pi/6)]])

plt.gca().add_artist(Polygon(np.dot(rotacja, kwadrat).T, alpha=0.2))
plt.axis([0, 2, -0.5, 2])
plt.show()
```


![png](output_178_0.png)


#####Powinowactwo osiowe

Względem osi X

$\begin{bmatrix}
  1 & \tan{\phi} \\
  0 & 1
\end{bmatrix}$

Względem osi Y

$\begin{bmatrix}
  1 & 0 \\
  \tan{\psi} & 1
\end{bmatrix}$

gdzie

* $\phi$ - kąt o jaki przesunięty zostanie część macierzy względem osi OY
* $\psi$ - kąt o jaki przesunięty zostanie część macierzy względem osi OX


```python
powinowactwo_x = np.array([[1, np.tan(np.pi/6)],[0, 1]])

plt.gca().add_artist(Polygon(np.dot(powinowactwo_x, kwadrat).T, alpha=0.2))
plt.axis([0, 2, 0, 2])
plt.show()
```


![png](output_180_0.png)



```python
powinowactwo_y = np.array([[1, 0],[np.tan(np.pi/6), 1]])

plt.gca().add_artist(Polygon(np.dot(powinowactwo_y, kwadrat).T, alpha=0.2))
plt.axis([0, 1.5, 0, 2])
plt.show()
```


![png](output_181_0.png)


##### Odbicie

Względem początku

$\begin{bmatrix}
  -1 & 0 \\
  0 & -1
\end{bmatrix}$

Względem osi X

$\begin{bmatrix}
  1 & 0 \\
  0 & -1
\end{bmatrix}$

Względem osi Y

$\begin{bmatrix}
  -1 & 0 \\
  0 & 1
\end{bmatrix}$


```python
odbicie_x = np.array([[1, 0],[0, -1]])

plt.gca().add_artist(Polygon(np.dot(odbicie_x, kwadrat).T, alpha=0.2))
plt.axis([-1, 1, -1, 1])
plt.show()
```


![png](output_183_0.png)



```python
odbicie_y = np.array([[-1, 0],[0, 1]])

plt.gca().add_artist(Polygon(np.dot(odbicie_y, kwadrat).T, alpha=0.2))
plt.axis([-1, 1, -1, 1])
plt.show()
```


![png](output_184_0.png)



```python
odbicie_pocz = np.array([[-1, 0],[0, -1]])

plt.gca().add_artist(Polygon(np.dot(odbicie_pocz, kwadrat).T, alpha=0.2))
plt.axis([-1, 1, -1, 1])
plt.show()
```


![png](output_185_0.png)


#### Macierz odwrotna
Macierz może reprezentować dowolne przekształcenie liniowe, może więc pojawić się w naszych głowach pytanie: czy istnieje macierz transformacji odwracająca efekt danej macierzy transformacji $F$? 

Odpowiedź brzmi: tak... czasami! Jeśli taka macierz istnieje, jest ona nazywana **macierzą odwrotną** i zapisujemy ją jako $F^{-1}$.

By ją wyliczyć możemy skorzystać z funkcji

```python
numpy.linalg.inv(macierz_kwadratowa)
```

Jeżeli podana macierz jest nie prawidłowa, bądź nie istnieje macierz odwrotna do podanej zostanie wyrzucony wyjątek
>LinAlgError


```python
import numpy.linalg as LA

wynik_przeksztalcenia = np.dot(odbicie_pocz, kwadrat)

try:
  macierz_odwrotna = LA.inv(odbicie_pocz)
  plt.gca().add_artist(Polygon(np.dot(macierz_odwrotna, wynik_przeksztalcenia).T, alpha=0.2))
  plt.axis([-1, 1, -1, 1])
  plt.show()
except LA.LinAlgError as lae:
  print("Nie udało się znaleźć macierzy odwrotnej, informacje o błędach: " + str(lae))
```


![png](output_187_0.png)


#### Wyznacznik
Wyznacznikiem macierzy kwadratowej $M$, zapisywanym jako $\det(M)$ lub $\det M$ albo $|M|$, nazywamy wartość wyliczaną z jej elementów $(M_{i,j})$ za pomocą różnych równoznacznych metod. Jedną z najprostszych metod jest podejście rekurencyjne:

$|M| = M_{1,1}\times|M^{(1,1)}| - M_{2,1}\times|M^{(2,1)}| + M_{3,1}\times|M^{(3,1)}| - M_{4,1}\times|M^{(4,1)}| + \cdots ± M_{n,1}\times|M^{(n,1)}|$

* gdzie $M^{(i,j)}$ jest macierzą $M$ bez rzędu $i$ i kolumny $j$.

Na przykład, obliczmy wyznacznik następującej macierzy o rozmiarze $3 \times 3$:

$M = \begin{bmatrix}
  1 & 2 & 3 \\
  4 & 5 & 6 \\
  7 & 8 & 0
\end{bmatrix}$

Za pomocą powyższej metody uzyskujemy:

$|M| = 1 \times \left | \begin{bmatrix} 5 & 6 \\ 8 & 0 \end{bmatrix} \right |
     - 2 \times \left | \begin{bmatrix} 4 & 6 \\ 7 & 0 \end{bmatrix} \right |
     + 3 \times \left | \begin{bmatrix} 4 & 5 \\ 7 & 8 \end{bmatrix} \right |$

Teraz musimy obliczyć wyznacznik każdej z tych macierzy o rozmiarze $2 \times 2$ (wyznaczniki te są nazywane **minorami**):

$\left | \begin{bmatrix} 5 & 6 \\ 8 & 0 \end{bmatrix} \right | = 5 \times 0 - 6 \times 8 = -48$

$\left | \begin{bmatrix} 4 & 6 \\ 7 & 0 \end{bmatrix} \right | = 4 \times 0 - 6 \times 7 = -42$

$\left | \begin{bmatrix} 4 & 5 \\ 7 & 8 \end{bmatrix} \right | = 4 \times 8 - 5 \times 7 = -3$

A teraz czas obliczyć ostateczny wynik:

$|M| = 1 \times (-48) - 2 \times (-42) + 3 \times (-3) = 27$

Wyznaczanie wyznaczników macierzy (szczególnie większych rozmiarów) jest wyjątkowo żmudnym zadaniem, w którym bardzo łatwo popełnić błąd. 

Na ratunek przybywa numpy oraz funkcja
```python
numpy.linalg.det(macierz)
```


```python
M = np.array([
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 0]
    ])
LA.det(M)
```




    27.0




```python
M = np.array([
        [2, 2, 3, 4, 5, 6],
        [7, 8, 9, 10, 11, 12],
        [13, 14, 0, 16, 17, 18],
        [19, 20, 21, 22, 23, 24],
        [25, 26, 27, 28, 0, 30],
        [31, 32, 33, 34, 35, 0],             
])
print(M)
print(LA.det(M))
```

    [[ 2  2  3  4  5  6]
     [ 7  8  9 10 11 12]
     [13 14  0 16 17 18]
     [19 20 21 22 23 24]
     [25 26 27 28  0 30]
     [31 32 33 34 35  0]]
    375840.0000000006
    

### Wektory własne i wartości własne
**Wektorem własnym** (zwanym także **wektorem charakterystycznym**) macierzy kwadratowej $M$ nazywamy wektor niezerowy niezmieniający swojego kierunku po przekształceniu liniowym zdefiniowanym przez macierz $M$. Zgodnie z bardziej formalną definicją jest to dowolny wektor $v$, który

$M \cdot v = \lambda \times v$

gdzie $\lambda$ jest wielkością skalarną zwaną **wartością własną**, powiązaną z wektorm $v$.

Na przykład każdy wektor poziomy pozostaje taki po zastosowaniu powinowactwa osiowego (co widać na poniższym wykresie), zatem jest on wektorem własnym przekształcenia $M$. Wektor pionowy zostaje nieco przechylony w prawo, zatem wektory pionowe *NIE SĄ* wektorami własnymi macierzy $M$.


Funkcja
```python
numpy.linalg.eig(macierz_kwadratowa)
```
modułu NumPy zwraca listę jednostkowych wektorów własnych i odpowiadające im wartości własne dla dowolnej macierzy kwadratowej.

####Zadanie z egzaminu

Wyznaczyć wartości własne i wektory własne przekształcenia liniowego $\phi: \mathbb{R}^2 \rightarrow \mathbb{R}^2, \phi(x,y) = (2x+y, x+2y)$


```python
baza = [[1,0],[0,1]]
PHI = np.array([[2, 1],[1, 2]])
wynik = np.dot(PHI, baza)

print(wynik)

rysuj_wektor(baza[0], color="b")
rysuj_wektor(baza[1], color="r")
rysuj_wektor(wynik[0], color='y')
rysuj_wektor(wynik[1], color='y')
rysuj_wektor(wynik[0], poczatek=baza[0], color="g", linestyle="dotted")
rysuj_wektor(wynik[1], poczatek=baza[1], color="g", linestyle="dotted")
plt.axis([-0.5, 4, -0.5, 4])
plt.show()

try:
  eigenvalues, eigenvectors = LA.eig(PHI)

  print("Wartości własne:")
  print(eigenvalues)
  print("Wektory własne:")
  print(eigenvectors)


except LA.LinAlgError:
  print("Nie udało się wyliczyć wartości i wektorów własnych")



```

    [[2 1]
     [1 2]]
    


![png](output_194_1.png)


    Wartości własne:
    [3. 1.]
    Wektory własne:
    [[ 0.70710678 -0.70710678]
     [ 0.70710678  0.70710678]]
    

Pakiet ten umożliwia też między innymi rozwiązywanie układu równań typu
$Ax=B$

służy do tego funkcja

```python
numpy.linalg.solve(A,B)
```
która wylicza dokładną wartość x równania macierzy pełnego rzędu.

A musi być macierzą kwadratową, pełnego rzędu, wszystkie wiersze muszą być od siebie liniowo niezależne.

Jeżeli warunek ten jest nie spełniony należy skorzystać z 
```python
numpy.linalg.lstsq(A,B)
```
metodę najmniejszych kwadratów do aproksymacji wyniku równania

**Przykładowe zadanie**

Rozwiązać układ równań

$2x_1 +5x_2 +4x_3 = 2 \\
x_1 +3x_2 +2x_3 = 1 \\
2x_1 +5x_2 +2x_3 = 3$




```python
A = np.array([[2,5,4],[1,3,2],[2, 5, 2]])
B = np.transpose(np.array([[2,1,3]]))

LA.solve(A,B)
```




    array([[ 2. ],
           [ 0. ],
           [-0.5]])



#Praca domowa

Celem pracy domowej będzie zaprojektowanie filtra stosowanego w wielu programach graficznych (np. Photoshop). Pozwala on na przejście z jednego obrazu do drugiego. By to osiągnąć trzeba dla każdego pixela obrazu A sprawdzić czy jego wartość jest mniejsza niż 0.5 a następnie zastosować poniższy wzór.



**Overlay blending mode formula:**

\begin{equation}
  f(a,b) =
    \begin{cases}
      2ab & \text{gdy a < 0.5}\\
      1 - 2(1-a)(1-b) & \text{w przeciwnym przypadku}\\
    \end{cases}       
\end{equation}


gdzie:
>**a** - to pojedynczy pixel obrazu A znormalizowany do przedziału 0-1

>**b** - to pojedynczy pixel obrazu B znormalizowany do przedziału 0-1

Do rozwiązania tego zadania została wykorzystana biblioteka OpenCV, o której więcej powiem następnym razem.

**Ważne by oba zdjęcia miały takie same wymiary!!!**

Zdjęcia w OpenCV przechowywane są w następujących wymiarach.

>(wysokość, szerokość, 3)

3 wynika z faktu iż obraz kolorowy składa się z trzech kanałów (RGB - red, green, blue)

Powyższy wzór trzeba zastosować dla każdego kanału! 

Powyższy wzór trzeba zastosować dla znormalizowanego obrazu (zmienne norm_image i norm_filter)

Celem pracy domowej nie jest napisanie rozwiązania optymalnego, iterowanie po całym obiekcie zdjęcia jest dopuszczalne.


```python
import cv2
import matplotlib.pyplot as plt
import numpy as np

# poniższe linie nie są potrzebe jeżeli nie korzystacie z google colab
from google.colab import drive
from google.colab.patches import cv2_imshow
drive.mount('/content/drive')


# obraz który będzie wykorzystywany jako filtr
# imread potrzebuje ścieżkę do pliku, jeżeli jest w tym samym folderze 
#co skrypt to po prostu 'nazwa_pliku.rozszerzenie'
filter_img = cv2.imread('/content/drive/My Drive/Warsztaty/filter.jpg')


# domyślnie cv2 otwiera obrazy w trybie BGR, zmieniamy to na RGB
filter_img = cv2.cvtColor(filter_img, cv2.COLOR_BGR2RGB)
# (opcjonalne) wyświetlenie zdjęcia
# plt.imshow(filter_img)
# plt.show()

# obraz na który będziemy nakładać filtr
img = cv2.imread('/content/drive/My Drive/Warsztaty/foreground.png')
# domyślnie cv2 otwiera obrazy w trybie BGR, zmieniamy to na RGB
img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
# (opcjonalne) wyświetlenie zdjęcia
# plt.imshow(img)
# plt.show()

# normalizacja obrazu
norm_image = cv2.normalize(img, None, alpha=0, beta=1, norm_type=cv2.NORM_MINMAX, dtype=cv2.CV_32F)
# (opcjonalne) wyświetlenie zdjęcia znormalizowanego
# plt.imshow(norm_image)
# plt.show()

# normalizacja obrazu
norm_filter = cv2.normalize(filter_img, None, alpha=0, beta=1, norm_type=cv2.NORM_MINMAX, dtype=cv2.CV_32F)
# (opcjonalne) wyświetlenie zdjęcia znormalizowanego
# plt.imshow(norm_filter)
# plt.show()


# pobranie wysokości i szerokości zdjęć (oba powinny być takich samych rozmiarów)
height = norm_image.shape[0]
width = norm_image.shape[1]

#utwórz tablicę o wymiarach (wysokość, szerokość), 
#która przechowuje 3 obiekty typu float

# miejsce na twój kod

#przeiteruj po wszystkich pixelach zdjęć (podwójna pętla, raz po wysokości, raz po szerokości) i zastosuj wzór,
#wynik wzoru przypisz do odpowiedniej komórki zdefiniowanej tablicy

# miejsce na twój kod

# wyświetl utworzoną przez ciebie tablicę, 
# u mnie nazywa się ona mod_img

plt.imshow(mod_img)
plt.show()
```

    Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount("/content/drive", force_remount=True).
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-104-e2eb292735ca> in <module>()
         59 # u mnie nazywa się ona mod_img
         60 
    ---> 61 plt.imshow(mod_img)
         62 plt.show()
    

    NameError: name 'mod_img' is not defined


## Co dalej?

Na następnych zajęciach zaczniemy pracę z rzeczywistymi danymi, rozszerzymy naszą wiedzę o bibliotece Matplotlib i wiele więcej!

Poniżej przykładów kilka kodów, które napisałem w 2-3 semestrze na potrzeby różnych przedmiotów. Po następnych zajęciach, napisanie tego typu kodu nie powinno stanowić dla ciebie większego problemu :)




```python
#ZADANIE2
#Napiecie wyjsciowe Vce
Vce=np.array([0, 0.5, 1, 2, 3, 4, 5, 6, 7, 8])
#Prad wyjściowy Ic(mA) przy stałej wartości prądu wejściowego
Ib0=np.array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0])
Ib10=np.array([0, 1.07, 2.43, 2.61, 3.41, 8.13, 2.95, 3.11, 4.22, 3.61])
Ib20=np.array([0.01, 1.15, 5.32, 6.11, 6.27, 6.14, 6.17, 6.98, 6.12, 5.87])
Ib30=np.array([0.01, 1.19, 8.28, 9.47, 9.55, 9.75, 8.57, 7.08, 6.53, 6.57])
Ib40=np.array([0.02, 1.21, 12.20, 12.26, 12.03, 12.82, 12.20, 7.24, 8.12, 8.86])
z1=np.polyfit(Vce,Ib0,2)
z2=np.polyfit(Vce,Ib10,5)
z3=np.polyfit(Vce,Ib20,6)
z4=np.polyfit(Vce,Ib30,5)
z5=np.polyfit(Vce,Ib40,6)
p_1=np.poly1d(z1)
p_2=np.poly1d(z2)
p_3=np.poly1d(z3)
p_4=np.poly1d(z4)
p_5=np.poly1d(z5)
xp=np.linspace(start=0.1,stop=7.8, num=100)
p1 = plt.plot(Vce,Ib0,color="blue",linestyle='-',marker="o", alpha=0.5,label="Wartości odnotowane Ib = 0"+u'\u03bc'+"A")
p11 = plt.plot(xp,p_1(xp),'b:',alpha=0.3)
p2 = plt.plot(Vce,Ib10,color="aqua",linestyle='-',marker="v",alpha=0.5,label="Wartości odnotowane Ib = 10"+u'\u03bc'+"A")
p22 = plt.plot(xp,p_2(xp),'b:',alpha=0.3)
p3 = plt.plot(Vce,Ib20,color="aquamarine",linestyle='-',marker="s", alpha=0.5,label="Wartości odnotowane Ib = 20"+u'\u03bc'+"A")
p33 = plt.plot(xp,p_3(xp),'b:',alpha=0.3)
p4 = plt.plot(Vce,Ib30,color="teal",linestyle='-',marker="p", alpha=0.5,label="Wartości odnotowane Ib = 30"+u'\u03bc'+"A")
p44 = plt.plot(xp,p_4(xp),'b:',alpha=0.3)
p5 = plt.plot(Vce,Ib40,color="cyan",linestyle='-',marker="x", alpha=0.5,label="Wartości odnotowane Ib = 40"+u'\u03bc'+"A")
p55 = plt.plot(xp,p_5(xp),'b:',alpha=0.3,label="Krzywe dopasowania")
plt.subplots_adjust(wspace=20)
plt.legend(loc='upper right')
plt.xlabel("Napięcie wejściowe Vce[V]")
plt.ylabel("Prąd wyjściowy Ic[mA] gdy Ib=const")
plt.show()
```


```python
import random
import numpy as np
import statistics as st
import matplotlib.pyplot as plt

data = []
miejsce = [] #0 - wies 1 - miasto
dochod = []
czas_pracy = []
for i in range(100):
    if i<=49: miejsce.append(1)
    else: miejsce.append(0)
    if miejsce[-1]==0:
        dochod.append(random.randrange(1500,3000))
    else:
        dochod.append(random.randrange(1800,4000))
    if dochod[-1] in range(1500,2200):
        czas_pracy.append(random.randrange(6,9))
    else:
        czas_pracy.append(random.randrange(8,11))
data = [(miejsce[i], dochod[i], czas_pracy[i]) for i in range(100)]

min_dochod = min(dochod)
max_dochod = max(dochod)
min_czas_pracy = min(czas_pracy)
max_czas_pracy = max(czas_pracy)
range_dochod = max_dochod - min_dochod
range_czas_pracy = max_czas_pracy - min_czas_pracy
mean_dochod = round(np.mean(dochod),2)
mean_czas_pracy = round(np.mean(czas_pracy),2)
median_dochod = st.median(dochod)
median_czas = st.median(czas_pracy)

print("\nTotal:\n")
print(
    "\tMinimalny dochod: ",min_dochod, "\t\t\t\tMaksymalny dochod:",max_dochod,"\n",
"\tMinimalny czas pracy: ",min_czas_pracy,"\t\t\t\tMaksymalny czas pracy: ",max_czas_pracy,"\n",
    "\tRozstep dochodow: ",range_dochod,"\t\t\t\tRozstep czasu: ", range_czas_pracy,"\n",
    "\tSredni dochod: ",mean_dochod, "\t\t\t\tSredni czas pracy: ", mean_czas_pracy,'\n',
    "\tMediana dochodu: ",median_dochod, "\t\t\t\tMediana czasu: ",median_czas)
mode_dochod=-1
mode_czas=-1
try:
    mode_dochod = st.mode(dochod)
    mode_czas = st.mode(czas_pracy)
except st.StatisticsError:
    print ("\nNo unique mode found\n")
variance_dochod = round(st.variance(dochod),2)
variance_czas = round(st.variance(czas_pracy),2)
stdev_dochod = round(st.stdev(dochod),2)
stdev_czas = round(st.stdev(czas_pracy),2)
q1_dochod = np.percentile(dochod,25)
q1_czas = np.percentile(czas_pracy,25)
q3_dochod = np.percentile(dochod,75)
q3_czas = np.percentile(czas_pracy,75)
iqr_dochod = q3_dochod-q1_dochod
iqr_czas = q3_czas-q1_czas
print(
    "\tModa dochodu: ", mode_dochod,"\t\t\t\tModa czasu: ",mode_czas,"\n",
    "\tWariancja dochodu: ", variance_dochod,"\t\t\t\tWariancja czasu: ",variance_czas,"\n",
    "\tOdchylenie dochodu: ",stdev_dochod,"\t\t\t\tOdchylenie czasu: ",stdev_czas,"\n",
    "\tKwartyl dolny dochodu: ",q1_dochod,"\t\t\t\tKwartyl dolny czasu: ",q1_czas,"\n",
    "\tKwartyl gorny dochodu: ",q3_dochod,"\t\t\t\tKwartyl gorny czasu: ",q3_czas,"\n"
    "\r Roz kwartylowy dochodu: ",iqr_dochod,"\t\t\t\tRoz kwartylowy czasu: ",iqr_czas,"\n"
)



min_dochod = min(dochod[50:])
max_dochod = max(dochod[50:])
min_czas_pracy = min(czas_pracy[50:])
max_czas_pracy = max(czas_pracy[50:])
range_dochod = max_dochod - min_dochod
range_czas_pracy = max_czas_pracy - min_czas_pracy
mean_dochod = round(np.mean(dochod[50:]),2)
mean_czas_pracy = round(np.mean(czas_pracy[50:]),2)
median_dochod = st.median(dochod[50:])
median_czas = st.median(czas_pracy[50:])

print("\nWies:\n")
print(
    "\tMinimalny dochod: ",min_dochod, "\t\t\t\tMaksymalny dochod:",max_dochod,"\n",
"\tMinimalny czas pracy: ",min_czas_pracy,"\t\t\t\tMaksymalny czas pracy: ",max_czas_pracy,"\n",
    "\tRozstep dochodow: ",range_dochod,"\t\t\t\tRozstep czasu: ", range_czas_pracy,"\n",
    "\tSredni dochod: ",mean_dochod, "\t\t\t\tSredni czas pracy: ", mean_czas_pracy,'\n',
    "\tMediana dochodu: ",median_dochod, "\t\t\t\tMediana czasu: ",median_czas)
mode_dochod=-1
mode_czas=-1
try:
    mode_dochod = st.mode(dochod[50:])
    mode_czas = st.mode(czas_pracy[50:])
except st.StatisticsError:
    print ("\nNo unique mode found\n")
variance_dochod = round(st.variance(dochod[50:]),2)
variance_czas = round(st.variance(czas_pracy[50:]),2)
stdev_dochod = round(st.stdev(dochod[50:]),2)
stdev_czas = round(st.stdev(czas_pracy[50:]),2)
q1_dochod = np.percentile(dochod[50:],25)
q1_czas = np.percentile(czas_pracy[50:],25)
q3_dochod = np.percentile(dochod[50:],75)
q3_czas = np.percentile(czas_pracy[50:],75)
iqr_dochod = q3_dochod-q1_dochod
iqr_czas = q3_czas-q1_czas
print(
    "\tModa dochodu: ", mode_dochod,"\t\t\t\tModa czasu: ",mode_czas,"\n",
    "\tWariancja dochodu: ", variance_dochod,"\t\t\t\tWariancja czasu: ",variance_czas,"\n",
    "\tOdchylenie dochodu: ",stdev_dochod,"\t\t\t\tOdchylenie czasu: ",stdev_czas,"\n",
    "\tKwartyl dolny dochodu: ",q1_dochod,"\t\t\t\tKwartyl dolny czasu: ",q1_czas,"\n",
    "\tKwartyl gorny dochodu: ",q3_dochod,"\t\t\t\tKwartyl gorny czasu: ",q3_czas,"\n"
    "\r Roz kwartylowy dochodu: ",iqr_dochod,"\t\t\t\tRoz kwartylowy czasu: ",iqr_czas,"\n"
)



min_dochod = min(dochod[:50])
max_dochod = max(dochod[:50])
min_czas_pracy = min(czas_pracy[:50])
max_czas_pracy = max(czas_pracy[:50])
range_dochod = max_dochod - min_dochod
range_czas_pracy = max_czas_pracy - min_czas_pracy
mean_dochod = round(np.mean(dochod[:50]),2)
mean_czas_pracy = round(np.mean(czas_pracy[:50]),2)
median_dochod = st.median(dochod[:50])
median_czas = st.median(czas_pracy[:50])

print("\nMiasto:\n")
print(
    "\tMinimalny dochod: ",min_dochod, "\t\t\t\tMaksymalny dochod:",max_dochod,"\n",
"\tMinimalny czas pracy: ",min_czas_pracy,"\t\t\t\tMaksymalny czas pracy: ",max_czas_pracy,"\n",
    "\tRozstep dochodow: ",range_dochod,"\t\t\t\tRozstep czasu: ", range_czas_pracy,"\n",
    "\tSredni dochod: ",mean_dochod, "\t\t\t\tSredni czas pracy: ", mean_czas_pracy,'\n',
    "\tMediana dochodu: ",median_dochod, "\t\t\t\tMediana czasu: ",median_czas)
mode_dochod=-1
mode_czas=-1
try:
    mode_dochod = st.mode(dochod[:50])
    mode_czas = st.mode(czas_pracy[:50])
except st.StatisticsError:
    print ("No unique mode found")
variance_dochod = round(st.variance(dochod[:50]),2)
variance_czas = round(st.variance(czas_pracy[:50]),2)
stdev_dochod = round(st.stdev(dochod[:50]),2)
stdev_czas = round(st.stdev(czas_pracy[:50]),2)
q1_dochod = np.percentile(dochod[:50],25)
q1_czas = np.percentile(czas_pracy[:50],25)
q3_dochod = np.percentile(dochod[:50],75)
q3_czas = np.percentile(czas_pracy[:50],75)
iqr_dochod = q3_dochod-q1_dochod
iqr_czas = q3_czas-q1_czas
print(
    "\tModa dochodu: ", mode_dochod,"\t\t\t\tModa czasu: ",mode_czas,"\n",
    "\tWariancja dochodu: ", variance_dochod,"\t\t\t\tWariancja czasu: ",variance_czas,"\n",
    "\tOdchylenie dochodu: ",stdev_dochod,"\t\t\t\tOdchylenie czasu: ",stdev_czas,"\n",
    "\tKwartyl dolny dochodu: ",q1_dochod,"\t\t\t\tKwartyl dolny czasu: ",q1_czas,"\n",
    "\tKwartyl gorny dochodu: ",q3_dochod,"\t\t\t\tKwartyl gorny czasu: ",q3_czas,"\n"
    "\r Roz kwartylowy dochodu: ",iqr_dochod,"\t\t\t\tRoz kwartylowy czasu: ",iqr_czas,"\n"
)
f = open('dane.txt','w')
for i in range(100):
    line = str(miejsce[i])+","+str(dochod[i])+","+str(czas_pracy[i])+"\n"
    f.writelines(line)
f.close()
bx1_dochod = [dochod[:50]]
plt.boxplot(bx1_dochod)
#"1 dochody w mieście"
plt.title("Boxplot dochodow w miescie")
plt.show()

bx2_dochod = [dochod[50:]]
plt.boxplot(bx2_dochod)
#"1 dochody na wsi"
plt.title("Boxplot dochodow na wsi")
plt.show()

bx_dochod = [dochod[:50], dochod[50:]]
plt.boxplot(bx_dochod)
#"1 - dochody wszystkich 2 - dochody w mieście 3 - dochody na wsi"
plt.title("Boxplot dochodow na wsi i w miescie")
plt.legend()
plt.show()

bx3_dochod = [dochod]
plt.boxplot(bx3_dochod)
#"1 - dochody wszystkich 2 - dochody w mieście 3 - dochody na wsi"
plt.title("Boxplot dochodow (w sumie)")
plt.legend()
plt.show()

##########################################################

bins_edges=[1500,1750,2000,2250,2500,2750,3000,3250,3500,3750,4000]
h1_dochod = [dochod[:50]]
plt.hist(h1_dochod,bins=bins_edges)
plt.ylabel("Liczba osób")
plt.xlabel("Dochody (zł)")
plt.title("Histogram dochodow w miescie")
plt.show()

h2_dochod = [dochod[50:]]
plt.hist(h2_dochod,bins=bins_edges)
plt.ylabel("Liczba osób")
plt.xlabel("Dochody (zł)")
plt.title("Histogram dochodow na wsi")
plt.show()

h_dochod = [dochod[:50], dochod[50:]]
plt.hist(h_dochod,bins=bins_edges)
plt.ylabel("Liczba osób")
plt.xlabel("Dochody (zł)")
plt.title("Histogram dochodow na wsi i w miescie")
plt.show()

h3_dochod = [dochod]
plt.hist(h3_dochod,bins=bins_edges)
plt.ylabel("Liczba osób")
plt.xlabel("Dochody (zł)")
plt.title("Histogram dochodow (w sumie)")
plt.show()

##########################################################

bx1_czas=[czas_pracy[:50]]
plt.title("Boxplot czasu pracy w miescie")
plt.boxplot(bx1_czas)
plt.show()


bx2_czas=[czas_pracy[50:]]
plt.title("Boxplot czasu pracy na wsi")
plt.boxplot(bx2_czas)
plt.show()

bx_czas=[czas_pracy[:50], czas_pracy[50:]]
plt.title("Boxplot czasu pracy na wsi i w miescie")
plt.boxplot(bx_czas)
plt.show()

bx3_czas=[czas_pracy]
plt.title("Boxplot czasu pracy (w sumie)")
plt.boxplot(bx3_czas)
plt.show()

##########################################################

h1_czas = [czas_pracy[:50]]
bins_edges=[6,7,8,9,10,11]
plt.hist(h1_czas,bins=bins_edges,range=[6,11], density=False)
plt.ylabel("Liczba osób")
plt.xlabel("Czas pracy (h)")
plt.title("Histogram czasu pracy w miescie")
plt.show()

h2_czas = [czas_pracy[50:]]
bins_edges=[6,7,8,9,10,11]
plt.hist(h2_czas,bins=bins_edges,range=[6,11], density=False)
plt.ylabel("Liczba osób")
plt.xlabel("Czas pracy (h)")
plt.title("Histogram czasu pracy na wsi")
plt.show()

h_czas = [czas_pracy[:50], czas_pracy[50:]]
bins_edges=[6,7,8,9,10,11]
plt.hist(h_czas,bins=bins_edges,range=[6,11], density=False)
plt.ylabel("Liczba osób")
plt.xlabel("Czas pracy (h)")
plt.title("Histogram czasu pracy na wsi i w miescie")
plt.show()


h3_czas = [czas_pracy]
bins_edges=[6,7,8,9,10,11]
plt.hist(h3_czas,bins=bins_edges,range=[6,11], density=False)
plt.ylabel("Liczba osób")
plt.xlabel("Czas pracy (h)")
plt.title("Histogram czasu pracy (w sumie)")
plt.show()
```


```python
import matplotlib.pyplot as plt
import numpy as np

# funkcje wykorzystane w zadaniu

def y1(N):
    n = np.arange(0,N)
    phase = np.pi/4
    y = np.cos(2 * np.pi * n/N +phase)
    return y


def y2(N):
    n = np.arange(0,N)
    phase = 0
    y = 0.5 * np.cos(4 * np.pi*n/N + phase)
    return y


def y3(N):
    n = np.arange(0,N)
    phase = np.pi / 2
    y = 0.25 * np.cos( 8 * np.pi*n/N + phase)
    return y


def y4(y1, y2, y3):
    a = y1 + y2 + y3
    return a


if __name__ == "__main__":
    N = 32  # zmienna okreslająca ilość próbek

    # Wygenerowanie funkcji
    func1 = y1(N)
    func2 = y2(N)
    func3 = y3(N)
    func4 = y4(func1, func2, func3)

    # Część rzeczywista funkcji sinusoidalnych
    plt.figure().suptitle("Część rzeczywista funkcji sinusoidalnych")
    plt.subplot(2, 2, 1)
    plt.plot(func1)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.title(r'$y_1=\cos$(2$\pi \cdot \frac{n}{N}$+$\frac{\pi}{4}$)')
    plt.subplot(2, 2, 2)
    plt.plot(func2)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.title(r'$y_2=\frac{1}{2}\cos$(4$\pi \cdot \frac{n}{N}$)')
    plt.subplot(2, 2, 3)
    plt.plot(func3)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.title(r'$y_3=\frac{1}{4}\cos$(8$\pi \cdot \frac{n}{N}$ +$\frac{\pi}{2}$)')
    plt.subplot(2, 2, 4)
    plt.title(r'$y_4$ = $y_1+y_2+y_3$')
    plt.plot(func4)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.tight_layout()
    plt.show()
    

    # Wyliczenia transformat Fouriera oraz innych parametrów dla każdej funkcji
    fourier1 = 2*np.fft.fft(func1)/N
    real1 = fourier1.real
    imaginary1 = fourier1.imag
    angle1 = np.angle(fourier1)
    modulus1 = np.abs(fourier1)

    fourier2 = 2*np.fft.fft(func2)/N
    real2 = fourier2.real
    imaginary2 = fourier2.imag
    angle2 = np.angle(fourier2)
    modulus2 = np.abs(fourier2)

    fourier3 = 2*np.fft.fft(func3)/N
    real3 = fourier3.real
    imaginary3 = fourier3.imag
    angle3 = np.angle(fourier3)
    modulus3 = np.abs(fourier3)

    fourier4 = 2*np.fft.fft(func4)/N
    real4 = fourier4.real
    imaginary4 = fourier4.imag
    angle4 = np.angle(fourier4)
    modulus4 = np.abs(fourier4)


    # Transformata Fouriera cz. rzeczywista
    plt.figure().suptitle("Część rzeczywista Transformaty Fouriera")
    plt.subplot(2, 2, 1)
    plt.ylim(-0.05, 0.8)
    plt.stem(real1, use_line_collection=True)
    plt.hlines(np.abs(round(real1[1], 3)), 0, 32, colors="red", linestyles="dotted")
    plt.yticks((0,0.25,0.5, np.abs(round(imaginary1[1], 3))))
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.title(r'$y_1=\cos$(2$\pi \cdot \frac{n}{N}$+$\frac{\pi}{4}$)')
    plt.subplot(2, 2, 2)
    plt.ylim(-0.05, 0.8)
    plt.yticks((0,0.250, np.abs(round(real2[2], 3)),0.707))
    plt.stem(real2, use_line_collection=True)
    plt.hlines(np.abs(round(real2[2], 3)), 0, 32, colors="orange", linestyles="dotted")
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.title(r'$y_2=\frac{1}{2}\cos$(4$\pi \cdot \frac{n}{N}$)')
    plt.subplot(2, 2, 3)
    plt.ylim(-0.05, 0.8)
    plt.yticks((np.abs(round(real3[4], 3)),0.250,0.50,0.707))
    plt.stem(real3, use_line_collection=True)
    plt.hlines(np.abs(round(real3[4], 3)), 0, 32, colors="gold", linestyles="dotted")
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.title(r'$y_3=\frac{1}{4}\cos$(8$\pi \cdot \frac{n}{N}$ +$\frac{\pi}{2}$)')
    plt.subplot(2, 2, 4)
    plt.ylim(-0.05, 0.8)
    plt.yticks((np.abs(round(real3[4], 3)), 0.25, np.abs(round(real2[2], 3)),np.abs(round(real1[1], 3)) ))
    plt.hlines(np.abs(round(real1[1], 3)), 0, 32, colors="red", linestyles="dotted")
    plt.hlines(np.abs(round(real2[2], 3)), 0, 32, colors="orange", linestyles="dotted")
    plt.hlines(np.abs(round(real3[4], 3)), 0, 32, colors="gold", linestyles="dotted")
    plt.title(r'$y_4$ = $y_1+y_2+y_3$')
    plt.stem(real4, use_line_collection=True)
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.tight_layout()
    plt.show()
```

#1. Matplotlib
---------

0. Podstawowe informacje
1. Plot
2. Scatter + Stem + subplots
3. Box charts - wykresy pudełkowe
4. Bar charts - wykresy kolumnowe
5. Pie charts- wykresy kołowe
6. Polar - wykresy liczb urojonych
7. Obsługa obrazów - PIL

## 0. Podstawowe informacje

**Matplotlib** jest to podstawowa biblioteka do generowania wykresów graficznych i wizualizacji danych w Pythonie.

Przydatne linki:

* https://matplotlib.org/
* https://matplotlib.org/tutorials/
* https://matplotlib.org/tutorials/introductory/pyplot.html
* https://matplotlib.org/3.1.1/tutorials/index.html
* https://towardsdatascience.com/matplotlib-tutorial-learn-basics-of-pythons-powerful-plotting-library-b5d1b8f67596
* https://python-graph-gallery.com/  - gotowe kody różnych wykresów


###Dodatkowe biblioteki bazujące lub podobne do matplotlib:

>**Seaborn** - biblioteka oparta na matplotlib stworzona konkretnie do wizualizacji danych statystycznych, posiada dobrą współpracę z biblioteką pandas. Gdzie matplotlib nie może, tam seaborn pośle.
* https://ksopyla.com/python/seaborn-wizualizacja-danych/
* https://seaborn.pydata.org/examples/index.html
* https://seaborn.pydata.org/tutorial.html

>**Plotly** - biblioteka do tworzenia pięknych i interaktywnych wykresów z wykorzystaniem biblioteki/frameworku **Dash**. Istnieje wersja płatna , lecz rozwiązanie w wersji darmowej oferuje sporą część swojej rozległej funkcjonalności.
* https://pypi.org/project/dash/
* https://plotly.com/python/
* https://dash.plotly.com/

##1. Plot

Spróbujmy wygenerować nasz pierwszy wykres. W tym celu należy pobrać bibliotekę
```python
import matplotlib.pyplot as plt
```
podać oś X, oś Y i poleceniem 
```python
plt.plot(oś X, oś Y)
```
wygenerować wykres


```python
import matplotlib.pyplot as plt

x = [2005,2010,2015,2020]
y = [2385.39, 3231.13, 3942.78, 5282.8]
plt.plot(x,y)
plt.show() # bez tej komendy w jupiter notebook wyświetli nam wykres, ale w normalnych warunkach ta komenda jest niezbędna
```


![png](output_212_0.png)


Mamy nasz wykres, ale co oznaczają konkretne dane? Podpiszmy wykres oraz osie. Służą do tego polecenia
```python
plt.xlabel("Opis osi X")
plt.ylabel("Opis osi Y")
plt.title("Opis wykresu")
```


```python
import matplotlib.pyplot as plt

x = [2005,2010,2015,2020]
y = [2385.39, 3231.13, 3942.78, 5282.8]
plt.plot(x,y)
plt.title("Przeciętne zarobki w Polsce w sektorze przedsiębiorstw - Polska")
plt.xlabel("Rok")
plt.ylabel("Wynagrodznie (zł)")
```




    Text(0, 0.5, 'Wynagrodznie (zł)')




![png](output_214_1.png)


Jest już trochę lepiej, ale jak popatrzymy na nasze dane, to mamy informacje z konkretnych lat, zaś biblioteka sobie automatycznie dopasowała krok w osiach. Jeżeli chcemy sami ustawić dla osi X:

```python
plt.xticks(ticks=None, labels=None)
```

Dla osi Y:
```python
plt.yticks(ticks=None, labels=None)
```

>**gdzie:**
* ticks - lista wartości, które chcemy wyświetlać
* label - lista o takim samym rozmiarze co **ticks**, która precyzuje co ma być wyświetlane, jeżeli istnieje jakiś alternatywny zapis, nie jest obowiązkowa

Przykład:


```python
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(0, 2*np.pi, 0.1)
y = np.sin(x)
plt.plot(x,y)
plt.title("y = sin(x)")
plt.show()
```


![png](output_216_0.png)


Po zastosowaniu formatowania tekstu na osiach



```python
import matplotlib.pyplot as plt
from math import sqrt

x = np.arange(0, 2*np.pi, 0.1)
y = np.sin(x)
plt.plot(x,y)
plt.title("y = sin(x)")
plt.xticks([0,np.pi/6, np.pi/4, np.pi/3, np.pi/2, np.pi, 3*np.pi/2, 2*np.pi], ['0', r'$\frac{\pi}{6}$',r'$\frac{\pi}{4}$', r'$\frac{\pi}{3}$', r'$\frac{\pi}{2}$', r'$\pi$', r'$\frac{3\pi}{2}$', r'$2\pi$' ] )
plt.yticks([0,0.5, sqrt(2)/2, sqrt(3)/2, 1],['0',r'$\frac{1}{2}$', r'$\frac{\sqrt{2}}{2}$', r'$\frac{\sqrt{3}}{2}$', '1'])
plt.show()
```


![png](output_218_0.png)


Wracając do przykładu z wynagrodzeniem


```python
import matplotlib.pyplot as plt

x = [2005,2010,2015,2020]
y = [2385.39, 3231.13, 3942.78, 5282.8]
plt.plot(x,y)
plt.title("Przeciętne zarobki w Polsce w sektorze przedsiębiorstw - Polska")
plt.xlabel("Rok")
plt.ylabel("Wynagrodznie (zł)")
plt.xticks([2005,2010,2015,2020])
plt.yticks([2000,3000,4000,5000])
plt.show()
```


![png](output_220_0.png)


Do ograniczenia zakresu wykresy wykorzystywane są metody 

Dla osi X:
```python
plt.xlim(limit_dolny, limit_górny)
```
Dla osi Y:
```python
plt.ylim(limit_dolny, limit_górny)
```

Domyślnie biblioteka stara się dopasować zakresy do danych, które jej podamy. Ale nic nie stoi na przeszkodzie byśmy ograniczyli tego do naszych potrzeb. 


```python
import matplotlib.pyplot as plt

x = [2005,2010,2015,2020]
y = [2385.39, 3231.13, 3942.78, 5282.8]
plt.plot(x,y)
plt.title("Przeciętne zarobki w Polsce w sektorze przedsiębiorstw - Polska")
plt.xlabel("Rok")
plt.ylabel("Wynagrodznie (zł)")
plt.xticks([2005,2010,2015,2020])
plt.yticks([2000,3000,4000,5000])
plt.xlim(2010,2020)
plt.ylim(3000, 5000)
plt.show()
```


![png](output_222_0.png)


By wykres był lepiej sformatowany można skorzystać z wielu dodatkowych parametrów, które można przekazać do metody **plot**, takich jak:

| Nazwa parametru |                    Opis                    |
|:---------------:|:------------------------------------------:|
|     color/c     |                kolor wykresu               |
|      alpha      |         przezroczystość, od 0 do 1         |
|      label      |  opis wykresu do wykorzystania w legendzie |
| marker          | definiuje styl punktów charakterystycznych |
| linestyle       | styl linii                                 |

i wiele innych


```python
import matplotlib.pyplot as plt

x = [2005,2010,2015,2020]
y = [2385.39, 3231.13, 3942.78, 5282.8]

plt.title("Przeciętne zarobki w Polsce w sektorze przedsiębiorstw - Polska")
plt.xlabel("Rok")
plt.ylabel("Wynagrodznie (zł)")
plt.xticks([2005,2010,2015,2020])
plt.yticks([2000,3000,4000,5000])

plt.plot(x,y, color="cyan", alpha=0.5, label="Wynagrodzenie", marker="o", linestyle="--")
plt.legend() #polecenie potrzebne by dodać legendę
plt.show()
```


![png](output_224_0.png)


Jako, że styl linii i kolor podaje się często, istnieje uproszczony zapis
> litera koloru, marker, styl linii

np.


```python
import matplotlib.pyplot as plt

x = [2005,2010,2015,2020]
y = [2385.39, 3231.13, 3942.78, 5282.8]

plt.title("Przeciętne zarobki w Polsce w sektorze przedsiębiorstw - Polska")
plt.xlabel("Rok")
plt.ylabel("Wynagrodznie (zł)")
plt.xticks([2005,2010,2015,2020])
plt.yticks([2000,3000,4000,5000])

plt.plot(x,y, "ro:", alpha=0.5, label="Wynagrodzenie")
plt.legend() #polecenie potrzebne by dodać legendę
plt.show()
```


![png](output_226_0.png)


##2. Scatter + Stem + subplots

Do dużej liczby danych rozproszonych zamiast metody plot warto skorzystać z metody scatter. Reszta parametrów nie ulega zmianie i jest bardzo podoba do tego co przed chwilą omówiliśmy.


> Źródło: https://matplotlib.org/3.3.2/gallery/lines_bars_and_markers/scatter_masked.html



```python
import matplotlib.pyplot as plt
import numpy as np

# Fixing random state for reproducibility
np.random.seed(19680801)


N = 100
r0 = 0.6
x = 0.9 * np.random.rand(N)
y = 0.9 * np.random.rand(N)
area = (20 * np.random.rand(N))**2  # 0 to 10 point radii
c = np.sqrt(area) # kolor zależy od pola
r = np.sqrt(x ** 2 + y ** 2)
area1 = np.ma.masked_where(r < r0, area)
area2 = np.ma.masked_where(r >= r0, area)
plt.scatter(x, y, s=area1, marker='^', c=c)
plt.scatter(x, y, s=area2, marker='o', c=c)

plt.show()
```


![png](output_228_0.png)


Wykresem który łączy plot ze scatter jest stem. 

```python
plt.stem(x,y)
```

>**Gdzie:**
* x - lista danych z osi X
* y - lista danych z osi Y



```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0.1, 2 * np.pi, 41)
y = np.exp(np.sin(x))

plt.stem(x, y, use_line_collection=True)
plt.show()
```


![png](output_230_0.png)


Domyślnie program tworzy jedną figurę (tak nazywany jest poszczególny obraz w matplotlib) i będzie ją nadpisywać tak długo jak długo nie wywołamy metody **show**. Pozwala nam to zawrzeć kilka wykresów na jednym obrazie. 


```python
#ZADANIE2
#Napiecie wyjsciowe Vce
Vce=np.array([0, 0.5, 1, 2, 3, 4, 5, 6, 7, 8])
#Prad wyjściowy Ic(mA) przy stałej wartości prądu wejściowego

Ib20=np.array([0.01, 1.15, 5.32, 6.11, 6.27, 6.14, 6.17, 6.98, 6.12, 5.87])
Ib30=np.array([0.01, 1.19, 8.28, 9.47, 9.55, 9.75, 8.57, 7.08, 6.53, 6.57])
Ib40=np.array([0.02, 1.21, 12.20, 12.26, 12.03, 12.82, 12.20, 7.24, 8.12, 8.86])

z3=np.polyfit(Vce,Ib20,6)
z4=np.polyfit(Vce,Ib30,5)
z5=np.polyfit(Vce,Ib40,6)

p_3=np.poly1d(z3)
p_4=np.poly1d(z4)
p_5=np.poly1d(z5)
xp=np.linspace(start=0.1,stop=7.8, num=100)

p3 = plt.plot(Vce,Ib20,color="aquamarine",linestyle='-',marker="s", alpha=0.5,label="Wartości odnotowane Ib = 20"+u'\u03bc'+"A")
p33 = plt.plot(xp,p_3(xp),'b:',alpha=0.3)
p4 = plt.plot(Vce,Ib30,color="teal",linestyle='-',marker="p", alpha=0.5,label="Wartości odnotowane Ib = 30"+u'\u03bc'+"A")
p44 = plt.plot(xp,p_4(xp),'b:',alpha=0.3)
p5 = plt.plot(Vce,Ib40,color="cyan",linestyle='-',marker="x", alpha=0.5,label="Wartości odnotowane Ib = 40"+u'\u03bc'+"A")
p55 = plt.plot(xp,p_5(xp),'b:',alpha=0.3,label="Krzywe dopasowania")
plt.subplots_adjust(wspace=20)
plt.legend(loc='lower right') #można dokreślić gdzie ma znajdować się legenda
plt.xlabel("Napięcie wejściowe Vce[V]")
plt.ylabel("Prąd wyjściowy Ic[mA] gdy Ib=const")
plt.show()
```


![png](output_232_0.png)


Jeżeli jednak chcemy rozbić nasze obliczenia na kilka różnych obrazów. Musimy zrozumieć koncepcje figur, osi oraz subplotów. Dotychczasowy zapis, który wykorzystywaliśmy jest tak naprawdę uproszczeniem poniższego zapisu.

```python
plt.subplots(nrows=1, ncols=1)
```

>**Gdzie**:
* nrows - ile szeregów wykresów
* ncols - ile kolumn wykresów

Metoda ta zwraca figurę, oraz osie (lub listę osi) w których będziemy rysować wykresy.


```python
import numpy as np
import matplotlib.pyplot as plt


# First create some toy data:
x = np.linspace(0, 2*np.pi, 400)
y = np.sin(x**2)

# Create just a figure and only one subplot
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_title('Simple plot') #metody wykorzystywane w osiach różnią się nazwą, zamiast plt.title mamy ax.set_title

# Create two subplots and unpack the output array immediately
f, (ax1, ax2) = plt.subplots(1, 2, sharey=True)
ax1.plot(x, y)
ax1.set_title('Sharing Y axis')
ax2.scatter(x, y)

# Create four polar axes and access them through the returned array
fig, axs = plt.subplots(2, 2, subplot_kw=dict(polar=True))
axs[0, 0].plot(x, y)
axs[1, 1].scatter(x, y)
plt.show()
```


![png](output_234_0.png)



![png](output_234_1.png)



![png](output_234_2.png)


Całkowity obraz składa się z poszczególnych obrazów (**figure**), które z kolei składają się ze składowych/osi (**axes**). Na początku, może to nastręczać dużo problemów w rozumieniu. Zapis jest też trochę utrudniony, niektóre metody nazywają się inaczej. Zachęcam do przeczytania wyjaśnienia, np. tutaj:

>https://medium.com/towards-artificial-intelligence/day-3-of-matplotlib-figure-axes-explained-in-detail-d6e98f7cd4e7


```python
import matplotlib.pyplot as plt
import numpy as np

# funkcje wykorzystane w zadaniu

def y1(N):
    n = np.arange(0,N)
    phase = np.pi/4
    y = np.cos(2 * np.pi * n/N +phase)
    return y


def y2(N):
    n = np.arange(0,N)
    phase = 0
    y = 0.5 * np.cos(4 * np.pi*n/N + phase)
    return y


def y3(N):
    n = np.arange(0,N)
    phase = np.pi / 2
    y = 0.25 * np.cos( 8 * np.pi*n/N + phase)
    return y


def y4(y1, y2, y3):
    a = y1 + y2 + y3
    return a


if __name__ == "__main__":
    N = 32  # zmienna okreslająca ilość próbek

    # Wygenerowanie funkcji
    func1 = y1(N)
    func2 = y2(N)
    func3 = y3(N)
    func4 = y4(func1, func2, func3)

    # Część rzeczywista funkcji sinusoidalnych
    plt.figure().suptitle("Część rzeczywista funkcji sinusoidalnych")
    plt.subplot(2, 2, 1)
    plt.plot(func1)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.title(r'$y_1=\cos$(2$\pi \cdot \frac{n}{N}$+$\frac{\pi}{4}$)')
    plt.subplot(2, 2, 2)
    plt.plot(func2)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.title(r'$y_2=\frac{1}{2}\cos$(4$\pi \cdot \frac{n}{N}$)')
    plt.subplot(2, 2, 3)
    plt.plot(func3)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.title(r'$y_3=\frac{1}{4}\cos$(8$\pi \cdot \frac{n}{N}$ +$\frac{\pi}{2}$)')
    plt.subplot(2, 2, 4)
    plt.title(r'$y_4$ = $y_1+y_2+y_3$')
    plt.plot(func4)
    plt.xlabel("Nr próbki")
    plt.ylabel("Amplituda")
    plt.tight_layout()
    plt.show()
    

    # Wyliczenia transformat Fouriera oraz innych parametrów dla każdej funkcji
    fourier1 = 2*np.fft.fft(func1)/N
    real1 = fourier1.real
    imaginary1 = fourier1.imag
    angle1 = np.angle(fourier1)
    modulus1 = np.abs(fourier1)

    fourier2 = 2*np.fft.fft(func2)/N
    real2 = fourier2.real
    imaginary2 = fourier2.imag
    angle2 = np.angle(fourier2)
    modulus2 = np.abs(fourier2)

    fourier3 = 2*np.fft.fft(func3)/N
    real3 = fourier3.real
    imaginary3 = fourier3.imag
    angle3 = np.angle(fourier3)
    modulus3 = np.abs(fourier3)

    fourier4 = 2*np.fft.fft(func4)/N
    real4 = fourier4.real
    imaginary4 = fourier4.imag
    angle4 = np.angle(fourier4)
    modulus4 = np.abs(fourier4)


    # Transformata Fouriera cz. rzeczywista
    plt.figure().suptitle("Część rzeczywista Transformaty Fouriera")
    plt.subplot(2, 2, 1)
    plt.ylim(-0.05, 0.8)
    plt.stem(real1, use_line_collection=True)
    plt.hlines(np.abs(round(real1[1], 3)), 0, 32, colors="red", linestyles="dotted")
    plt.yticks((0,0.25,0.5, np.abs(round(imaginary1[1], 3))))
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.title(r'$y_1=\cos$(2$\pi \cdot \frac{n}{N}$+$\frac{\pi}{4}$)')
    plt.subplot(2, 2, 2)
    plt.ylim(-0.05, 0.8)
    plt.yticks((0,0.250, np.abs(round(real2[2], 3)),0.707))
    plt.stem(real2, use_line_collection=True)
    plt.hlines(np.abs(round(real2[2], 3)), 0, 32, colors="orange", linestyles="dotted")
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.title(r'$y_2=\frac{1}{2}\cos$(4$\pi \cdot \frac{n}{N}$)')
    plt.subplot(2, 2, 3)
    plt.ylim(-0.05, 0.8)
    plt.yticks((np.abs(round(real3[4], 3)),0.250,0.50,0.707))
    plt.stem(real3, use_line_collection=True)
    plt.hlines(np.abs(round(real3[4], 3)), 0, 32, colors="gold", linestyles="dotted")
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.title(r'$y_3=\frac{1}{4}\cos$(8$\pi \cdot \frac{n}{N}$ +$\frac{\pi}{2}$)')
    plt.subplot(2, 2, 4)
    plt.ylim(-0.05, 0.8)
    plt.yticks((np.abs(round(real3[4], 3)), 0.25, np.abs(round(real2[2], 3)),np.abs(round(real1[1], 3)) ))
    plt.hlines(np.abs(round(real1[1], 3)), 0, 32, colors="red", linestyles="dotted")
    plt.hlines(np.abs(round(real2[2], 3)), 0, 32, colors="orange", linestyles="dotted")
    plt.hlines(np.abs(round(real3[4], 3)), 0, 32, colors="gold", linestyles="dotted")
    plt.title(r'$y_4$ = $y_1+y_2+y_3$')
    plt.stem(real4, use_line_collection=True)
    plt.xlabel("Nr pasma częstotliwościowego")
    plt.ylabel("Amplituda")
    plt.tight_layout()
    plt.show()
```


![png](output_236_0.png)



![png](output_236_1.png)


##3. Boxplots - wykresy pudełkowe

Do danych giełdowych bardzo często wykorzystywane są tak zwane wykresy pudełkowe, świecowe. Zakres pudełka oznacza pierwszy (dolny) i trzeci (górny) kwartyl, które odpowiednio oznaczają, że 25% i 75% danych znajduje się poniżej tych wartości. Linią przecinającą pudło oznacza się gdzie występuje mediana wartości. Zaś wąsami pudła oznacza się maksymalne odchylenia wartości (minimum i maksimum), z ograniczeniem rozmiaru wąsów dla ich czytelności.


![Boxplot_vs_PDF.png](data:image/png;base64,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)


```python
import numpy as np
import matplotlib.pyplot as plt

data = np.random.rand(50)
fig, ax = plt.subplots(1,2)
ax[0].boxplot(data, labels=["Próbka"])

ax[1].plot(data, "co:")

plt.show()


```


![png](output_239_0.png)



```python
import numpy as np
import matplotlib.pyplot as plt

data = np.random.rand(50,10) # wygenerowanie 10 serii po 50 wartości z przedziału 0 - 1
plt.boxplot(data)
plt.title("Wykres pudełkowy")
plt.show()
```


![png](output_240_0.png)


##4. Barplots - wykresy kolumnowe

Kolejnym wykresem są bardzo popularne wykresy kolumnowe, wykorzystywane do porównania danych dyskretnych. Każdy słupek w wykresie ma odpowiednią wysokość, która koresponduje proporcjonalnie do wartości danej zmiennej.

```python
plt.bar(x, height, width=0.8)
```

>**Gdzie**:
* x - sekwencja koordynatów wykresu kolumnowego
* height - sekwencja wysokości poszczególnych kolumn, lub pojedyncza wartość
* width - szerokość kolumn (opcjonalne) 



```python
import numpy as npx
import matplotlib.pyplot as plt
 
# Make a fake dataset:
height = [3, 12, 5, 18, 45]
bars = ('A', 'B', 'C', 'D', 'E')
y_pos = np.arange(len(bars))
 
# Create bars
plt.bar(y_pos, height)
 
# Create names on the x-axis
plt.xticks(y_pos, bars)
 
# Show graphic
plt.show()
```


![png](output_242_0.png)


By wygenerować wykres kolumnowy poziomy należy użyć metody
```python
plt.barh(y, height)
```


```python
# libraries
import numpy as np
import matplotlib.pyplot as plt
 
# Make fake dataset
height = [3, 12, 5, 18, 45]
bars = ('A', 'B', 'C', 'D', 'E')
y_pos = np.arange(len(bars))
 
# Create horizontal bars
plt.barh(y_pos, height)
 
# Create names on the y-axis
plt.yticks(y_pos, bars)
 
# Show graphic
plt.show()
```


![png](output_244_0.png)



```python
puchar_domow = {
    "Slytherin": { 
        "Obrona przed Czarną Magią": 100,
        "Eliksiry" : 200,
        "Transmutacja": 150,
        "Zielarstwo": 50
     },
     "Gryffindor":{
        "Obrona przed Czarną Magią": 120,
        "Eliksiry" : 180,
        "Transmutacja": 300,
        "Zielarstwo": 120
     },
     "Ravenclaw":
     {
        "Obrona przed Czarną Magią": 140,
        "Eliksiry" : 120,
        "Transmutacja": 130,
        "Zielarstwo": 150 
     },
     "Hufflepuff":
     {
        "Obrona przed Czarną Magią": 120,
        "Eliksiry" : 120,
        "Transmutacja": 120,
        "Zielarstwo": 120
     }
}
```


```python
import matplotlib.pyplot as plt
import numpy as np

barWidth = 0.3

for index, dom in enumerate(puchar_domow):
  plt.bar(
      3*np.arange(len(list(puchar_domow[dom].keys())))+(index*barWidth), #musimy przesunąć kolumny tak by na siebie nie nachodziły
      list(puchar_domow[dom].values()),
      width = barWidth, 
      label=str(dom))

plt.xticks([0.5, 3.5, 6.5, 9.5], list(puchar_domow['Slytherin'].keys()))
plt.legend()
plt.show()


```


![png](output_246_0.png)



```python
import matplotlib.pyplot as plt
import numpy as np

barWidth = 0.3

temp = []
temp.append(np.zeros(4))
for index, dom in enumerate(puchar_domow):
  if index == 0:
    continue
  temp.append(list(puchar_domow[list(puchar_domow.keys())[index-1]].values()))

sum_temp = np.zeros(4)
for index, dom in enumerate(puchar_domow):
  sum_temp += temp[index]
  plt.bar(
      list(puchar_domow[dom].keys()), 
      list(puchar_domow[dom].values()),
      width = barWidth, 
      label=str(dom),
      bottom=sum_temp) #musimy podać co będzie dołem kolejnych kolumn, żeby je skleić
plt.legend()
plt.show()
```


![png](output_247_0.png)


Bardzo popularnym wykresem kolumnowym jest histogram. Histogram to nic innego jak wizualizacja rozkładu jakiejś cechy. 
```python
plt.hist(x, bins=None)
```

>**Gdzie:**
 * x - lista danych na podstawie, której chcemy wygenerować histogram
 * bins - na ile kolumn chcemy podzielić nasz histogram, domyślnie równa się liczbie unikatowych danych podanych w x. Może być liczbą, albo sekwencją liczb od których uwzględniamy kolejne kolumny

 Wygenerujmy dane z rozkładu normalnego i wykreślmy ich histogram.

 Źródło: https://matplotlib.org/3.1.1/gallery/pyplots/pyplot_text.html#sphx-glr-gallery-pyplots-pyplot-text-py
 


```python
import numpy as np
import matplotlib.pyplot as plt

# Fixing random state for reproducibility
np.random.seed(19680801)

mu, sigma = 100, 15
x = mu + sigma * np.random.randn(10000)

# the histogram of the data
n, bins, patches = plt.hist(x, 50, facecolor='g', alpha=0.75)


plt.xlabel('Smarts')
plt.ylabel('Population')
plt.title('Histogram of IQ')
plt.text(60, 602.5, r'$\mu=100,\ \sigma=15$')
plt.grid(True)
plt.show()
```


![png](output_249_0.png)


Jeżeli zamiast liczby w populacji interesuje nas prawdopodobieństwo wystąpienia danej kolumny histogramu w metodzie ustawiamy pole **density=True**.


```python
import numpy as np
import matplotlib.pyplot as plt

# Fixing random state for reproducibility
np.random.seed(19680801)

mu, sigma = 100, 15
x = mu + sigma * np.random.randn(10000)

# the histogram of the data
n, bins, patches = plt.hist(x, 50, density=True, facecolor='g', alpha=0.75)


plt.xlabel('Smarts')
plt.ylabel('Probability')
plt.title('Histogram of IQ')
plt.text(60, .025, r'$\mu=100,\ \sigma=15$')
plt.xlim(40, 160)
plt.ylim(0, 0.03)
plt.grid(True)
plt.show()
```


![png](output_251_0.png)


Do generowania histogramu dwuwymiarowego stosujemy polecenie 
```python
plt.hist2d(x, y, bins=10, density=False)
```

>**Gdzie:**
* x, y - wartości na osiach X,Y
* bins - analogicznie do histogramu jednowymiarowego
* density - analogicznie do histogramu jednowymiarowego

Utworzony wykres jest heat mapą danych


```python
import matplotlib.pyplot as plt
import numpy as np
 
# create data
x = np.random.normal(size=50000)
y = x * 3 + np.random.normal(size=50000)
 
# Big bins
plt.hist2d(x, y, bins=(50, 50), cmap=plt.cm.jet)
plt.show()
```


![png](output_253_0.png)


## 5. Piecharts - wykresy kołowe

Dotarliśmy do ostatniego kręgu piekła jeżeli chodzi o wizualizację danych. Wykresy kołowe owiane złą sprawą są z reguły niepotrzebne, a nasze dane możemy przedstawić w innej, lepszej formie. Jeżeli jednak uprzemy się na nie, je również można zrealizować w matplotlib.

![obraz.png](data:image/png;base64,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)

![obraz.png](data:image/png;base64,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)


```python
import matplotlib.pyplot as plt

tasks = 'task_1', 'task_2', 'task_3', 'task_4', \
         'task_5', 'task_6', 'task_7', 'task_8', \
         'task_9', 'task_10', 'task_11', 'task_12', \
         'task_13', 'task_14', 'task_15', 'task_16', \
         'task_17', 'task_18', 'task_19'

time =[0.722539930138737,
     0.28336817817762494 + 0.5273803339805454,
     0.1135483211837709 + 0.13343579485081136,
     0.8881094930693507 + 0.3978329210076481 + 0.34098400291986763 + 0.4007001109421253 + 0.3937181669753045,
     3.1206228479277343 + 4.390893992036581 + 4.731932940194383 + 3.0876565920189023 + 15.17197903408669,
     0.052445481065660715 + 0.019446991849690676 + 0.019331110874190927 + 0.09747512708418071 + 0.060720112873241305,
     0.029143241932615638,
     0.7307675471529365,
     0.10479382984340191,
     0.4169424350839108,
     1.1366547809448093,
     1.5477838290389627,
     0.05833269190043211,
     0.12475891201756895,
     0.08382681896910071,
     0.0744338259100914,
     0.0875642818864435,
     0.11377762793563306,
     0.04675672412849963]

colors = ['red',
          'pink',
          'orange',
          'purple',
          'indigo',
          'blue',
          'lightblue',
          'cyan',
          'teal',
          'green',
          'lightgreen',
          'yellowgreen',
          'yellow',
          'gold',
          'orange',
          'darkorange',
          'brown',
          'gray',
          'darkslategray']

plt.figure(figsize=(15,  10))

patches = plt.pie(time,
                  colors=colors,
                  radius=1,
                  )

plt.legend(tasks, bbox_to_anchor=(1,1),
           fontsize=18)
plt.tight_layout()
plt.title("Czas trwania zadania")
plt.show()
```


![png](output_257_0.png)


Jedyną informację jaką jesteśmy w stanie wyciągnąć z naszego wykresu jest to, że istnieje jedno zadanie, którego czas trwania stanowi ok. 75% całego czasu. Z wykresu nie jesteśmy w stanie jednak wyczytać ile trwa poszczególne zadanie (możemy dodać tę informację, ale przy dużej liczbie małych fragmentów, będzie to nieczytelne). Dlatego tego typu wykresy mają tylko sens, przy małej liczbie unikatowych kategorii, na które chcemy dzielić nasze dane przy ich wizualizacji. 

By poczytać więcej na ten temat zachęcam do lektury:
>https://www.businessinsider.com/pie-charts-are-the-worst-2013-6?IR=T

Popularną alternatywą dla wykresu kołowego jest wykres kołowy z wcięciem w środku, tzw. pączek. By go zrobić należy do wykresu dodać białe koło i upozycjonować je na środku wykresu kołowego.


```python
import matplotlib.pyplot as plt

tasks = 'task_1', 'task_2', 'task_3', 'task_4', \
         'task_5', 'task_6', 'task_7', 'task_8', \
         'task_9', 'task_10', 'task_11', 'task_12', \
         'task_13', 'task_14', 'task_15', 'task_16', \
         'task_17', 'task_18', 'task_19'

time =[0.722539930138737,
     0.28336817817762494 + 0.5273803339805454,
     0.1135483211837709 + 0.13343579485081136,
     0.8881094930693507 + 0.3978329210076481 + 0.34098400291986763 + 0.4007001109421253 + 0.3937181669753045,
     3.1206228479277343 + 4.390893992036581 + 4.731932940194383 + 3.0876565920189023 + 15.17197903408669,
     0.052445481065660715 + 0.019446991849690676 + 0.019331110874190927 + 0.09747512708418071 + 0.060720112873241305,
     0.029143241932615638,
     0.7307675471529365,
     0.10479382984340191,
     0.4169424350839108,
     1.1366547809448093,
     1.5477838290389627,
     0.05833269190043211,
     0.12475891201756895,
     0.08382681896910071,
     0.0744338259100914,
     0.0875642818864435,
     0.11377762793563306,
     0.04675672412849963]

colors = ['red',
          'pink',
          'orange',
          'purple',
          'indigo',
          'blue',
          'lightblue',
          'cyan',
          'teal',
          'green',
          'lightgreen',
          'yellowgreen',
          'yellow',
          'gold',
          'orange',
          'darkorange',
          'brown',
          'gray',
          'darkslategray']

plt.figure(figsize=(15,  10))

patches = plt.pie(time,
                  colors=colors,
                  radius=1,
                  )

plt.legend(tasks, bbox_to_anchor=(1,1),
           fontsize=18)
plt.tight_layout()
plt.title("Czas trwania zadania")

# dodaj koło na środku
my_circle=plt.Circle( (0,0), 0.7, color='white')
p=plt.gcf()
p.gca().add_artist(my_circle)
 

plt.show()
```


![png](output_260_0.png)



```python
import matplotlib.pyplot as plt

tasks = 'task_1', 'task_2', 'task_3', 'task_4', \
         'task_5', 'task_6', 'task_7', 'task_8', \
         'task_9', 'task_10', 'task_11', 'task_12', \
         'task_13', 'task_14', 'task_15', 'task_16', \
         'task_17', 'task_18', 'task_19'

time =[0.722539930138737,
     0.28336817817762494 + 0.5273803339805454,
     0.1135483211837709 + 0.13343579485081136,
     0.8881094930693507 + 0.3978329210076481 + 0.34098400291986763 + 0.4007001109421253 + 0.3937181669753045,
     3.1206228479277343 + 4.390893992036581 + 4.731932940194383 + 3.0876565920189023 + 15.17197903408669,
     0.052445481065660715 + 0.019446991849690676 + 0.019331110874190927 + 0.09747512708418071 + 0.060720112873241305,
     0.029143241932615638,
     0.7307675471529365,
     0.10479382984340191,
     0.4169424350839108,
     1.1366547809448093,
     1.5477838290389627,
     0.05833269190043211,
     0.12475891201756895,
     0.08382681896910071,
     0.0744338259100914,
     0.0875642818864435,
     0.11377762793563306,
     0.04675672412849963]

colors = ['red',
          'pink',
          'orange',
          'purple',
          'indigo',
          'blue',
          'lightblue',
          'cyan',
          'teal',
          'green',
          'lightgreen',
          'yellowgreen',
          'yellow',
          'gold',
          'orange',
          'darkorange',
          'brown',
          'gray',
          'darkslategray']

plt.figure(figsize=(15,  10))

plt.bar(tasks, time, color=colors)
plt.tight_layout()
plt.title("Czas trwania zadania")
plt.ylabel("Czas (s)")
plt.show()
```


![png](output_261_0.png)


Od razu lepiej. Dla lepszej czytelności możemy zmienić skalę w której wyświetlamy nasze wykresy. Służą do tego polecenia

```python
plt.xscale("skala")
```
dla osi X
```python
plt.yscale("skala")
```
dla osi Y


Dopuszczalne wartości:
*  'linear' - skala liniowa
* 'log' - skala logarytmiczna
* 'symlog' - skala logarytmiczna, symetryczna
* 'logit' - skala logit



```python
import matplotlib.pyplot as plt

tasks = 'task_1', 'task_2', 'task_3', 'task_4', \
         'task_5', 'task_6', 'task_7', 'task_8', \
         'task_9', 'task_10', 'task_11', 'task_12', \
         'task_13', 'task_14', 'task_15', 'task_16', \
         'task_17', 'task_18', 'task_19'

time =[0.722539930138737,
     0.28336817817762494 + 0.5273803339805454,
     0.1135483211837709 + 0.13343579485081136,
     0.8881094930693507 + 0.3978329210076481 + 0.34098400291986763 + 0.4007001109421253 + 0.3937181669753045,
     3.1206228479277343 + 4.390893992036581 + 4.731932940194383 + 3.0876565920189023 + 15.17197903408669,
     0.052445481065660715 + 0.019446991849690676 + 0.019331110874190927 + 0.09747512708418071 + 0.060720112873241305,
     0.029143241932615638,
     0.7307675471529365,
     0.10479382984340191,
     0.4169424350839108,
     1.1366547809448093,
     1.5477838290389627,
     0.05833269190043211,
     0.12475891201756895,
     0.08382681896910071,
     0.0744338259100914,
     0.0875642818864435,
     0.11377762793563306,
     0.04675672412849963]

colors = ['red',
          'pink',
          'orange',
          'purple',
          'indigo',
          'blue',
          'lightblue',
          'cyan',
          'teal',
          'green',
          'lightgreen',
          'yellowgreen',
          'yellow',
          'gold',
          'orange',
          'darkorange',
          'brown',
          'gray',
          'darkslategray']

plt.figure(figsize=(15,  10))

plt.bar(tasks, time, color=colors)
plt.tight_layout()
plt.title("Czas trwania zadania")
plt.ylabel("Czas (s)")
plt.yscale("log")
plt.show()
```


![png](output_263_0.png)


Jak widać mając te same dane, w zależności od tego co chcemy przekazać użyjemy różnych metod do ich wizualizacji. Bardzo ważną częścią pracy z danymi jest umiejętny dobór narzędzi do wizualizacji danych. Ludzie są wzrokowcami, często prawidłowe dane, przedstawione w nieprawidłowy sposób prowadzą do niewłaściwych wniosków. 

Polecam poczytać o 5 rzeczach, na które warto zwrócić uwagę analizując wykresy

https://venngage.com/blog/misleading-graphs/


## 6. Polar - wykresy liczb urojonych

Do wykresów liczb zespolonych istnieje specjalny wykres zwany polar. 

```python
plt.polar(theta, r)
```

>**Gdzie:**
* theta - lista kątów
* r - lista promieni

W konwencji tej 0 stopni oznacza liczbę rzeczywistą pozytywną, 180 stopni liczbę rzeczywistą negatywną, 90 stopni liczbę urojoną pozytywną, a 270 stopni liczbę urojoną ujemną. Wszystkie pozostałe stopnie to mieszanka liczb urojonych i liczb rzeczywistych czyli liczby zespolone. 

> Źródło: https://www.geeksforgeeks.org/plotting-polar-curves-in-python/


###Kardioida (wykres sercowy)

$r = a + a \cos{\theta} $


```python
import numpy as np 
import matplotlib.pyplot as plt 
import math 
  
  
# setting the axes 
# projection as polar 
plt.axes(projection = 'polar') 
  
# setting the length of  
# axis of cardioid 
a=4
  
# creating an array 
# containing the radian values 
rads = np.arange(0, (2 * np.pi), 0.01) 
   
# plotting the cardioid 
for rad in rads: 
    r = a + (a*np.cos(rad))  
    plt.polar(rad,r,'g.')  
  
# display the polar plot 
plt.show()

```


![png](output_267_0.png)


###Spirala Archimedesa

$ r = \theta$


```python
import numpy as np 
import matplotlib.pyplot as plt 
  
  
# setting the axes 
# projection as polar 
plt.axes(projection = 'polar') 
  
# creating an array 
# containing the radian values 
rads = np.arange(0, 2 * np.pi, 0.001)  
  
# plotting the spiral 
for rad in rads: 
    r = rad 
    plt.polar(rad, r, 'g.') 
      
# display the polar plot 
plt.show()

```


![png](output_269_0.png)


###Krzywa róży

$r = a \cos({n \theta})$


```python
import numpy as np 
import matplotlib.pyplot as plt 
  
  
# setting the axes 
# projection as polar 
plt.axes(projection='polar') 
  
# setting the length 
# and number of petals 
a = 1
n = 4
  
# creating an array 
# containing the radian values 
rads = np.arange(0, 2 * np.pi, 0.001)  
  
# plotting the rose 
for rad in rads: 
    r = a * np.cos(n*rad) 
    plt.polar(rad, r, 'g.') 
   
# display the polar plot 
plt.show() 

```


![png](output_271_0.png)


## 7. Obsługa obrazów - PIL

Poza generowaniem własnych wykresów biblioteka matplotlib umożliwia wczytywanie i wyświetlanie obrazów.

Odpowiednio:

```python
plt.imread(fname, format=None)
```

>**Gdzie:**
* fname - ścieżka do pliku na dysku, sama nazwa pliku jeżeli znajduje się w tym samym folderze co plik pythona, który uruchamiamy
* format - format pliku, jeżeli nie jest sprecyzowany, domyślnie próbuje otworzyć plik w formatowaniu PNG

```python
plt.imshow(X, cmap=None)
```

>**Gdzie:**
* X - obiekt PIL lub tablica o określonych rozmiarach:
  * (M, N)
  * (M, N, 3): obraz RGB, wartości rzeczywiste z zakresu 0-1, lub całkowite z zakresu 0-255
  * (M, N, 4): jak wyżej, z uwzględnieniem kanału przezroczystości alpha

* cmap - paleta kolorów, dla obrazów czarnobiałym warto zdefiniować odpowiednią paletę kolorów


Matplotlib posiada wiele palet kolorystycznych, poniżej znajduje się ich lista:

>https://matplotlib.org/examples/color/colormaps_reference.html


```python
import matplotlib.pyplot as plt

from google.colab import drive #polecenia potrzebne tylko w arkuszu Google by załadować zdjęcia z dysku Google, nie używać u siebie

drive.mount('/content/drive')

filter_img = plt.imread('/content/drive/My Drive/Warsztaty/filter.jpg')
plt.imshow(filter_img)
```

    Mounted at /content/drive
    




    <matplotlib.image.AxesImage at 0x7f6509650630>




![png](output_273_2.png)


###PIL (Python Imaging Library) 
jest standardową biblioteką do przechowywania obrazów w Pythonie. Biblioteka ta jednak przestała być rozszerzana przez autora w 2011 i nie jest kompatybilna z obecną wersją Pythona. Z tego powodu powstał fork tej biblioteki, który nazywa się Pillow, który jest aktualny z obecną wersją Pythona, a przy okazji w dużej mierze kompatybilny z oryginalnym PILem. Ze względów semantycznych importuje się go jako PIL, mimo iż to co pracuje pod jego kopułą to w rzeczywistości pillow. 

https://pillow.readthedocs.io/en/stable/
https://rk.edu.pl/pl/python-imaging-library/



```python
import PIL
import matplotlib.pyplot as plt

image = PIL.Image.open('/content/drive/My Drive/Warsztaty/filter.jpg')
plt.imshow(image) #działa tak samo, lecz obiekt PIL posiada o wiele więcej możliwości!
```




    <matplotlib.image.AxesImage at 0x7f6508bc57f0>




![png](output_275_1.png)


Już wcześniej wspomnieliśmy, że numpy jest domyślnym sposobem przechowywania informacji w Pythonie jeżeli chodzi o analizę danych, operację wykonywane na nim są stosunkowo szybkie.

 Z tego też powodu istnieje możliwość konwersji obiektów PIL do tablic n-wymiarowych numpy i odwrotnie. Logika jest taka, gdy potrzebujemy wysokiej funkcjonalności na obrazie - operujemy na obiekcie PIL, jeżeli potrzebujemy dokonać obliczeń - dokonujemy ich na macierzy numpy.

**Przykładowe konwersje macierzy numpy do obiektu PIL:**
```python
PIL_image = Image.fromarray(np.uint8(numpy_image)).convert('RGB')
PIL_image = Image.fromarray(numpy_image.astype('uint8'), 'RGB')
```

**Przykładowe konwersje obiektu PIL do macierzy numpy :**

```python
macierz = numpy.asarray(PIL.Image.open('obraz.jpg'))
```

W obu przypadkach ważne jest kodowanie obiektów, musimy dostosować by kodowanie w jednej wersji było kompatybilne do kodowania w drugiej wersji, najlepiej operować na kodowaniu **np.uint8** czyli liczbach całkowitych z zakresu 0-255. Jeżeli jest jakiś problem z obrazem w naszym kodzie zawsze warto jest sprawdzić czy aby na pewno korzystamy z dobrego kodowania.

Macierze numpy są wykorzystywane również przez **OpenCV** z tego względu, jest to unikatowy sposób zapisu naszych obrazów. Warto opanować tę umiejętność.

# 2. Pandas

O Pandas można myśleć jak o arkuszu kalkulacyjnym dla programistów. Biblioteka ta posiada wsparcie dla plików Excela, plików CSV, oraz wielu innych formatów w których przechowywane są dane. Jedna tablica numpy zawiera obiekty tego samego typu, w przypadku pandas dane muszą być tego samego typu w jednej kolumnie, lecz cała tablica może przechowywać różnego rodzaju dane. 

Jeżeli chcemy nauczyć się pracy z danymi jest to niezbędne narzędzie, najbardziej popularne wsród naukowców. 

> **Poradniki:**
* https://www.kaggle.com/learn/pandas
* https://www.learndatasci.com/tutorials/python-pandas-tutorial-complete-introduction-for-beginners/
* https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html


W przypadku Pandas kluczowym jest zrozumienie rozróżnienia pomiędzy Series (pojedyncze kolumny danych), a Dataframe (tabela zawierająca Series).

Przykładowe zbiory danych:
* https://gs.statcounter.com/screen-resolution-stats/mobile/worldwide
* https://data.europa.eu/euodp/en/data/dataset/covid-19-coronavirus-data
* https://www.kaggle.com/datasets

Cheat sheet:

https://www.kaggle.com/timoboz/data-science-cheat-sheets
https://github.com/datasciencescoop/Data-Science-Tutorials
https://github.com/datasciencescoop/Math-for-Data-Science


```python
# 3. Scipy, SymPy

> **Poradniki:**
* https://www.scipy.org/scipylib/index.html
* https://www.sympy.org/en/index.html

```

# CO DALEJ?

![hqdefault.jpg](data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAUDBAgICAgICAgICAoICAgKCAgICAgICAgKCggKCAgICAgIChANCAgOCggIDRUNDhERExMTCA0WGBYSGBASExIBBQUFCAcIDwkJDxYVEhUWFBUVFBQUFBQUFBQUFBQUFRQUFBQUFBQUFBQUFBUUFBQUFBQUFBQUFBQUFBQUFBQUFP/AABEIAWgB4AMBIgACEQEDEQH/xAAcAAEAAgIDAQAAAAAAAAAAAAAABQYBBAIDBwj/xABHEAABBAEDAgMGAwUFBgUDBQABAAIDEQQFEiEGMRMiQQcUMlFhcQgjgRVCUpGhJDNysdIWYnOywdEJNEPC1IKi8DVTY5Kz/8QAGwEBAAIDAQEAAAAAAAAAAAAAAAMEAQIFBgf/xAAzEQACAQMDAgQEBgICAwAAAAAAAQIDBBESITEFQRNRYYEicZGhBhQyscHwI9EV4TNCUv/aAAwDAQACEQMRAD8A+MkREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAcgsBSb9JkbKIjVuIAdzt5APevqu3K0N8bC8yR0ATW4gni6bY5Kj8WG2/Jb/JVsN6Xtz6ERSwpTTtIfOwvDmgbq8xN9rvt2XY/QpA9rNzLc0uBs1QNfLvwjqwTxkzGxryipKLw+CIRSOdpMkW3dRB9W2QOa5NcLbf09IBZkiAHclzgB9yWp40MLfkKwrttaXtz6EGshb2m6a6cuDXNG2r3X864oFbGRocjCwFzDvdtFF3c/O29ll1YJ4zuawsq0o61F48/sRAWSpPN0WWJu47XC+zbJHBNnjtwuyDp+R7Gv3xgObu5LuB9fKtfGhjOTf8hX1aNLzyQ6Leh05z5TC1zCRfmBJaaF8EDlbOVockTHPL2HbVgF18kD+H6rZ1Ip4bNIWdaUXJReFy/kRCKXn0GZrS62uoA02yTddhXflccHRJJW7w5g5Ip24HivkPqtfGhjOTf/AI+41adDzyRYXFb8+nlkjYt7HF1C2mwCTVHjgrdk6dlaCd8flBJ5d6Ak/u/RbOrFYyzWFlWnnTFvHPoQiwpiHQpXsDw5lOFgWb9fSu/C6sHR5JS4AhpZVh1g83Xp9FjxYb78GfyFfKWl78epGot/UdNdBQL2OJPZpJI7dwRx3W5H07IQDvj5APd3r2/dR1YJZbELGtKTiovK59CFWFLYuhySBxDmeV5byT3H6dl1RaRI6Qx8NIs26wCAasccrPiw8zH5Gts9L34I7sslSWoaQ6Fu5z4z28oJ3G/UAgWF2YehySxtkDmAOugSb4JHPH0WPFhjVnYyrGu5+GovPOCICyVKx6HI6R8Ycy2BpJs15hYrhdUukytlbGa8xADudtn60iqwe2TDsa6WXF4zj34I5CpjK0J8bC8yR0ATW4i65oWOT9F06fpD5mlzXNABrm/lfoE8WGM52Dsayn4el58iNWSpaTQpBI2PcwlzS4GzVC/p34XTqGkyQgF1OB9W2QOa5NcIqsG8JiVjXim3F4XJHrCm3dOyAWZIgPUlzgB9yWrT0/THTuc0OaNgsk3R5A4oIqsGs5ErGtGSi4vL4I+llS+ToUjNnmYd7g0UXdz87HZcczQ5ombztcLo7bJHBN9u3CKtB43MysK8c5i9uSJWVMY+gyPY1+9gDhfJdwPr5Vqxac503gtewnnzA2w0L4ICyqsHnfg1lZ1o6cxfxcepo0lKYytDkjY55cwhtWBuvkgcW36rEugzNYX200AaBJJ7dhXJ5WqrQfc3fT7hNpwe2/sRFLCltP0V8rN4c1vmLaduBsVfYfVa+Vp7o5Gx72OLq5abAJNUeOCtlUi3jJHK0qxipuOz4NJZU0/p2UAnfHwCTy705/hXXj6DK9geHNpwJFk33I+X0Wvj08ZySvptxnGh55IgopHB0iSUuHDCyrD7B57dguOpaY6Ctz2OJPZpJI+pBAoLbxY5xncidpWUNbi8eZHopuLp6VwaQ+PzAEcu9RY/d+q64NDkfu8zPI4tNk9x8uOyx40PMk/464yloe/BEpSkY9JkMpiNNI3cmw0gXZBrkLnqGjuhZvMkZ7U0E7jzXAI5WfEjnGTT8nW0uWl4XJGLCl8LQ5JWNkDmAOugS6+DXo1G6HIZHsDmWwNJNmvN2rhY8aGWsm66fXaTUXvx69yIQKSm0mRkjYzXnIAdzts/Wl35GgyRtLnSRAAE8uIuhdCxyfoniw235NfyNbf4Xtz6EMiktN0l87S4OaADXmu+1+gK7X6HIHtZuYS4OI5NCrJvj6I6sE8ZEbGtKKmovD4IhFJZ+kSw0TTgfUWQOQOeOO62T07IBZkiA+ZLgB9yW8J4sMZyZ/IV3Jx0vK5IVYW/p2mPmc5rXNG0WSSaPNcUF35OhyR7bew7nBoou7n5+XssurBPGdzWNlWlDWovHmRICUpXM0SWJu47XUeQ2yfXnt24XPF0KSRjX72AOF8l1jv38q18aGM5N10+u5aNDzz7G9rWoOZOxgaD4RDh35LmtNUPRdXUWS6TZG1oPla8ltkguaLBrtS14c4Py2TuGxocy6t1BoAv5nspLRGtYTKXEeK50bRVerXDm+FV0qmk8bpfc7iqSupTipfDKX0iuH7mt09lmMeG9pDSbDvqaHN8Bq3MfK8TMLeKjD2gg3YBPK7Ncy2NYYzIWOLSQAN24EEbTzwCVBaDkthm3SktG0i6J7rVQ8SLnjDaJJV/y04UNeYppt7bejJbqfKLGNjABD+b5sbXei6tVz3Px2N2jdLu3NBNt2uFcXfP1WjrecJpG7B5Wdjz5gTdkHspDGljfkTZO8hseyuO+5uz52OVmNPRBNrdb+5rVu3WrTUJbSxHtxhtv9/qaGgzuhedzfK+g41ZAu7A+ak8zM3ZEEQojfG7ddnzAcHmh9lv5+YyNvmlMe/4XgbiKo3VqpYU7W5DHud5Q8EmuavvSzTXitzaxsYr1PyUY0Izym03xss5LPruSYoSQAd1s5vgOaeRXqtCPUXDFssbYqNo5tzS13mq7/6LX6g1RkrRHHyLDi7kG+RVH7rnG6Od0ADyPCgt5rsWkuI5K1p0dMFqXfJtc3/iXD8OfZRXHfn6EdpskkMok2E1fBB9RXopnXs8GJjW8iTvfDm7XDu2+L+qlZMyMR+KXkMPY+vJIHHfuFTdRm3SucJDILHnI2k8D0vhbQ/zS1OOMEdy/wAjRdOE9Sl8tvUuOXOYonSAAljQQD2PIHoofRdRIZLbWjYHPbZI3OJaNvfn9OVnWNYjdEWR+feKdwW7a2kEfPstLDeySKHH3U4zG+OwdtAPyK1o0MQepdye76hqrx8OfEfTdvtn+8GoHSeKJdh+PdVGu+6vsrBl6oPALwBuNNcx3FbmustF2QPmt/HnYI+H2Ihtce3wDni1VtfyWySAtlLxXYt27eSdo+Y+v1WY/wCaWHHGCKpmwouUKmXPtt9Sy6W7+zMP+4T/AFcVF6RqJfPJYa0SkbjZpu1prkn1+qQavFHjMa07nhu0sIIHJN8/yUbh5LBBOwmnPMe0V3pxJ59FinQfxZXLN7jqEf8AEoT/AExy/njjP2OvPlfPIZNtXXDQa4Ff9FYcXUric5wDXxsvaQQ0gbQKJNk/RbOmNZG3wWv3FgBdfl+OiPWvVQfUuY19Bkrnc/AW0G8ckH1JKNqrJQ07LuYw7SnKv4mZS5W3P17Mlun37o3Htcrz/MNK0cjUn+9cMB22z17bj5j8iuGiapHFAWuPmDnENo88ChY7dlp4OezxppH+XeyUACzy4GgsxovXJtfI1qX8fBpRjLDzl+nzOzqOZ0spa1tiIlu5tndyTZI4Uj0/nUxsT2lm34XVQPJcdxJoLs0EMiY0b7dON4FUAG7gRd/RdPUmWwsdGJXBzauPbYfyDy70pYbU/wDFjbzJIxdFO8dT4nzHb2Wc+WDnoOSZpJ3kAWGChdccf9F163nuZPGwNB8NzXjvZJANH6LR6ZzY4TJ4jtu4Nrgm6PPZcf2k1+VHK4bWtcy6s8Nrn+i28F+I3jZIhfUE7SEdWJOWX9W9za6iynSBkbWg21jyW2SCQbaa7LHTuWYrY9pDSb3bTYPAAPoAtjRTG1z5t/8AeyOjaK+ZDgbuwtrW8xjWFhkLHOaSNrd24URt78An/Jaya/8AEo7EtOLbd5Kok12247d1ydMeX4mbtoUxsjQQbsU43f8A2WOqMksY2OgRJ682NrgRShdCyWRzB8hoU7mie4IHAXb1BqDZntDPhYTTufNdHkHstvy+Ki22SIn1JSs55l8Upcem38G/qmoufjsG0bpdwc0XbdrgRxd8/VaOhZD4Xnc0lr6DjRsCwbH1W9jyRyZEmR4h2xCM/D3sBh4uxypXOy2Rst0hj3fC9o3Edjdfb/NayaivDUeSanTdZ/mJVMaNlxultnty8mhn5u6aFjaI3Rvu+QTxR54W3reSYoXOAB3eTm+zg7lVXFna3Ia9ziWiQEurki7ulJdQaqyRojj8wsOLuRR5FUe/cLMrfEopLZckdPqidGrKUsSb2O/G1JwxSdrbbTGg3bg4Ot1Xz+iidPfJDIJAwmr4N+or0+6kIXRz+7sDyPDhO/jsWlzq5PPCnn5sYj8Uvph9fXuR2790nLw8pRznkUaTuVGcqmNCWHt82/bgi9d1AGJobyJrB3cObtc0/CDx+qkp5jHCZAL2MaaPY/D8lUNUmD5nOEhkHHnI2k8D0+nb9FMaprERh8OM7y5oa6wW7aDeR8+y1nb7RSXfckodVTdWU5JPCUeO2ePczouokMlsNG0PkbZI3Otvl78/5qHL5DL42w/HuqjXe6+y2sOVj4YoN1OM9njsCA2/kSrLjzMEdB9iEFrj2+Ac8X8lJOXhNtLkgoUneKMZVMKKyuOefsaORqg93MgaN3DXMdx8Qde3myPqtnRz/Z4z/uk//c5VzqDJbLIHMlLxR4Ldu3knaPmP+6kcXWIo8ZjQdz2trbRHdx/e+xUVS3ehaVyy1b9TX5iTqSWIxwntv9PM46TqTn5LyWtAlLQ42abtBA5J4v6qL1GZ88hfsrsPKCRxws4OS1sOQwmi/ZtFHmngnn04Vn0sMY3wWv3FgDjfHx0fnR9FLUapPUo+nsU7eLvYqnKphbyfHLb2x9zXwtS/KcXDa+NnDTYa4NDQOSbLjzwFz6flL43vqrldx8rAKi+pMxknDJXOp3LNtAUKJ3LloWpRQwOa53m3OIbR58orkduQo5Uc020t32LVO/UbqMJzTjFPfbc55mpPGVwwHw9zPXkWbcfrytbqSV0spY1tiIkBzedwJuyRwuvC1BnvEkr/ACB7ZeBZ5c0gD+ql9AayJg85LpwXAVVbd3rakaVPEsbpFanOV3qp6/hlJt8bJcber/Y6+nsymNhkaW7fhdyAbJJ3Emgueh5RmlmeQB5Wih24IHquHUeWzY+ISFrhVsAsOsgi3eld1H9M5rITJ4jtu4CuCfX6KN09cJTS3ZZV34NenQlNOMc77eTWH8je13PcyWNgaDsLXjvZPy49F09QZbpBHG1oO5rXnbZIJsFp+VLVfqLX5UcrvK1jm9rPDT3UjpBjD5MjeakldG0V33EOBu7C3UFCKbW6X3K7uHcVJwjP4ZS9NoruavT+WYbje2muN7qJINUPpS3Rl780MoVGJQCDe7yuN32/ktnWctjGlhlMbnNJBaN9jzCjzxZ4Vb0XIbHOHvNNp/NX3aQOB9ViMPETnjfBLUr/AJWdO315ipJt7bLPD/cm+qMksjDAAfF7nmxtIIpdOo6g92MwbW7pNzS0XuaG7SCBd8/VaPUGoNme0M5awmnc+a6vg9uykIXMknfkbiGxNjPwnnhrCOeRysRpaIR1LjL/ANCrdOvXqKnLZ4j243bftuR2hzvhkJLDTqDjRsCwSR9eFKanmh0sEbaILmPv94WSKIB4+ykMzLYyMOdIWbx5XAbiOAQav5KpskrID3OLmiQEuIPI3XdfNbQ/ytyawa3DdlBUIz1JtN8bFp1rJMcTnAA2dvN9nBwvhRuHqhbjElrbjprQSRuDi6zV819F1a9qbJW7IvOCQ4uoggixVevFLjHE2cY8Qc5uyN+87T5SC59c1fC0p0VGHxrvkluL2VS4fgvPw4Xq3tz6cnLS53wsgLpAGOkcHM2Dy0RZvue6l9WiZJA8kXtYXtNkc7eDwouTa+WHH8J8Ya8lwc6z5q9a4UvnNqCQDsI3D9AKWlZ/HF98/bJPZQxb1YvdJY3zzjfntkrnTUDXzHcL2t3N5PBBFFWLUMGOYEvZucGuDTZHoSOx+ZWl0qPyCf8A+Q+n0CkcmfZQa0vceQxvcjmz27Cv6rWvUk6vw9ibptrSjZ5qJPVvx/clbxmz48U5a/wyxzA5m1rr3bq5Pah/moYlWDW8mo3tML43SlriXO4O0n0rhV5dKi21lnlOoQjTkoRbwl3z5v8AgFy4oilOcFm1hEBncsLkiA4os0sIDluK4rkuKDIRclxQHKz81i0pZQzk4os0sIYOW5YtKSkM5MIi5IYMWhKBKQzkwizSyhgxayXLFLKGdRxRckQwYtZ3LFLKGcnFFyRDBxXKz81ikpDOTCIs0hgwuVn5rFJSGcmEREMBcty4rNIMglYXJYpAYWdywiAySsIiA7G+n3V8iLJmD99jgAe4uqseh7qhN7hX/ChaxjWMHAo1d96JVC/aSj5nqPw5FydRYWMb/cp+JEHZLWEW3xKIs9t1Vat02LG9gje22tqhZFUKHI57KG6c/v5uOwP6ecKcmlDBZ+zR6uPo0fUqC6qS1JI6XR7amqM5zw02+V2RXo8KSLIk8M+ENkrmGg+2C+OfnVWpnS8kTRDzbnAVJxVE3+nb5LTzsssuR+O9p2OjDi7gbg7028nutjQ4Wsha5ooyAF3N2QXD9FmvLNPMudjHTqSp3Omm9t2088bYwmkjU1jNjZkRAsNscHOIDbILWkC/+66ep8zysjaHAkNeT6Frm2B/VdAyI5s1r+NpcwHfQHAAN81XC29Hxw5z5ZCx7SSxofR7EUG36V2pS6IwSk1wii61S4lOnCSxKT38ku/ucOl8toaYneUlxIJ7HgAAfVbjMkPy9oBHhtc038wT/RctTYxkbtjYGu2k+YNa6qPLPXffZQvTso94LnuAtr7c41ZI+Z9VroVRSqJdiXx520qdtJppNb+hJdVTsbEGFtufRa6hxR5F91VFNdU5bJHtaw34dgngg2b8pB5ChVatYaaaycTrNZVbmTTylsv78ziiIrBygrv7Euo5dM1rDkigw5/eJYcWSPNxmZUXhz5ETZC2OThstDh3pZ+apCu/sT6f/aOtYcfvun4Ix5Ysp82pZQxICyCeJ742yuBBmcPhb60eRSA+j/8AxAc+PTmafpWHgabBBqEMs08keDBHkh+PkM8MRzsALGm6I9V84ezL2j5mge8jExdLyfejFv8A2jgRZpZ4e/b4RkP5YPiG670Pkvon8fMeHqseBquBrGjZMenxSQy40GowTZkjsjIYWOhghLt7GgW4kih818gBAfe/4u+qR0xg6NkaXpeiB+bJO2f3jSsaZtMgikbsFDbzI7+i+Meg8179cwcjxNOxnvz2SeLqEbf2ZC58u7dkx0QMVpPLewAX0x+PrqXTs7TOn2YWfhZjopskytxcvHyHRg40LQXtheSwEgjn5L49QHp34jersLWNWilwoIIRiYMOHlPxYoIcTKyoJZvHzMRsBr3WQvaWF3m21dL1v8EXTujz4mr5zxBla1BDnMwdOmMWQJYBiwyNlGA9pdKfeKZvH8Veq+Vl7b+GPS9Dy35kWTrOp6HqvgZLsLNgz8bTdOMQijDIcjJkPieI6c2WNFFsfzCA9Px8/UtS0nOweqehNXt8kUuNPoWgx6a6JsTC8iaV43VvomvS18ir7T9hmnarpGrszte640TUsGPGy2y4jepjmOkc+EtjqDI2sfTvmV8u+2jXdN1PXc/O0jFOFgzugONjGGLHMQbjRRvBhgc5jLkZIfKTe6/VAUxfUH/h56XjZWsau3KxsfJa3TYy1uRDHM1pOXGNwEjSAa9Qvl9fTP8A4fmu4WBrGrPzszEw2P02NrH5eTDjMe4ZcbtrXTOAc6gTQ5QEx057W8bM6j1HpzWtI05+Fm5WXpOI7TNNw8bMhkmzm4cM78h5trWxGS3NG7dtIHCgNY/DLMzrFmgxZeMMafHk1KHe/IMjcCPN8A475BDzmbL5A236qe6e9mOlYPUGo9S6x1Fok2LiZOXquFjaPrGLNnyzx5gzIIHQTMa14dGJGlrXWXFoB5tTPse9tUGve0CTVM6XE07Ex9Hz8XBfkvjwyYDmRzQDJdLMWHJIe6w11eU12QHDqH2o9P8ATuuQdMR6I2bT9MjyMDMfNiafPnzzvNY80WXI4Hw2iTkvAP0XZoXsTxum/aLocTfAytO1NupuxMbIvJljbj6dUnvXjRBjyZZC5u26AHalWPar7c4oeps+CDQ+ks6BuoNazUZcBmTLOy2fnvy2S7ZHd/OOPL9F7T7SOs9Hk646LyI9V0x8OPDr4yJ2Z+I6GAyYjRGJpRJtjLjwNxFnsgKv+Ln8OgzWS65oWPWSxoOXgQRvd7w1jIYIG6fiY0NNkAa5zrPPJXb+K/2eR5uD0hpmFjYWBk6hqMWMZTjtgp7sA8TmCPdtDgbFHn0UH1r+Ic6D15qLm5Q1LRsiPTmyNxphmthDMBrnnTg2dsLJXTOp9n0PqFN/jA9qWHFj9M6po+bp+bkYOq+9sgbkw5Oz+yO2e8RY8u5rbNHkc8WgKt7TtRxuhItO6V0LSYdQ1bJdi5c8+dhQanFOcmJ+NJj4YeBMHOyMaMtZtoAn1KpPUus9V5c2kQ670zjaXiO1zS7nboH7P3yePtbA6Zzac1zTJbD32/RXD2jQab17j4HUmma1h6LrOM7GxMiLV9Sx9MiYMaJ88mRhMjMkwPvGS3Y8kcMd2IV29tnUWEOmelMOXW9M1DMw9c6d9+lg1ODLLjCJBkZLn795i3cmR4HfmkBIfiZfrumZmDH0x0tg58MuNI/Jezp5mcGSiYta0viZTCWUaP3XzZ7X+uOpjh/s7XOn8DSY80sLH/sFunZLxDMyQ+BM4B1BwYHV6Or1X0R+JZmZreZhTdO9a6JpsUONJHkRu6kGH4khmL2v2Ypc11MoWaPovnP2s9BaxFhnUdT6s0TWxhljY8eDX36jmATTMjd4EMjO1lrnURw0n0QH1V+JqLVNLi0x3S/TWBnumdkDMDNBizvDDWRGEkRMHhWTJ377fovOPaNpGPqHQT9Q6pwcbQ9Xgkz3afjx4sWjvyZWU2GP3dzd+QDHudtB5q1Yfxae2U6VN05naBqmHlvglzjk42PnMyMaUGCOOMZkOJNb2gveW7iOQvPvxFZun9Y6MzqTA1rwJMcO950TVNRggI93i8J0mnabG6RxnkebsuG5vy7IC0+0rHxuhei9EytGwsGeXUcvFkyH6tiQ6g4HJ0wzytjc9oLGb4WUPS3fNZ9nGNjdc9E63l6xhYOPNpuXmSY8mlYkOnuvF0ts8TZCxpL2b8h9j1pvyXR7QNU0/rvo3RsLTtU0vTJtMy8Zk8evZ2Pp73+7aacd8kLGOkc6Nz527XEC9ru1UnQWq6f0J0XrODqOqaZqk+p5eVHBHoOdj57me9aaMeOSZj3RubE18DtzgDW5ve6QGt7VtGw2eybR8lmJjMnfFpBdkMgibO4ue7dulDdxv1s8rn/4eWjYeVhdQnKxMXJMc2FsORjwzFlwzk7TI07QaHb5Lq07XdP6s9nmL09i6jp+mZmmu02GX9t5mPgRSmAGSR+OQ975IvMACWjkHspP2B5OB7PNI1zJ1bV9H1L3mXC8LH0HUcfPynAb4HEQyuiJAMzXGrprXH0QEP8Ah+0TBx+iNS1XRMbH1fqFzGePp8sMWqOh26k+KDbp+3fDuxy93+9sv0UL7TsvJ1HpiQa/0Zq+BqGF7zNHqOBpEWmaXHuLWROy7G90bWdx8yq77CtD0vN0XP8A2d1HndP67G2IyHL1XH0rR8rdku8INcwmaYMgDyeOHvHoV6v7Jsl/TuPreX1b1PpPUeG/BYGadja2zV5pC2drntZh5hY17i2uAeaQHxMik+pcmGfNy5sdnhwy5WRJBHtazw4nyufGzY0kNphaKHApRiAsfs/6tyNFzBm40OHPII5I/DzsZmVBUgAcTFJxuFcH0sr7T6h6q8D2b4/VDNL0T9oSsxXOvSsY49yaiMZ9Q1x+X9e/K+Cgvr7qzqTTneyDEwG5+E7LbFhB2G3LgOWC3Vg9wOOH7wQzzHjgcoDp/B3pGJ1Zr+q69quLje8YAwjBj4sEOPp/5sE+K/xMLaWP8kbXf4vN3UX7H/bFnap1Rp+k5Wl9Pe7ZOoPhk8PRsZkuweJW1/O0+Qc0tL8B3tF03RtRzcHUJDAdW92bBkvdDHiQ+7syJnnKnmlb4QIIa2gbcQOFu+yX2S/snqbA1jJ6m6Rfj4ue6eRkOuROnLDv4Yx0bWl/mHBcEB5/+MDonB0HqR+Jp7ZGxTYkOU9sjw+pZ5ZjIGU0BsflbTfSl40vYPxbdd4PUPUcmZgCbwocWLEJmEY3yY8swfJEYpHtfC7c0tdfIPYLx9AXz2G+z2bqfWIdMhmihtj55HzGQAxQlpla0xscRIWk1xS969o/WztH1OHpHpDp+DNl0ps8E4ztKx9Uy8pzQMgSQvj/ADHtbG59lwBoD5LwH2K+0LI6Z1eHU8eOKUtY+GVsrHPHgylomLGte38za3izVr33r7pPD13Usbq3pnqbT9Im1LxJ82LVtag0/Ox3OIhEUUeKHuhBia8Oa55vcPQoCu6bpOrdT9S9O6T1ZobdHxsh+oiP3PS/2NLkbMN07/zCz83a+GH04Dj/ABKx/iZ9qOV031DPpOnaZoPu8GLhuYcjR8aaa34zXuLpON3P0V+/EX7UtF0/qPo3VxmQ6hBpztZOS3TMjFzJ2+Nhtx4vK2YNFvkHxOHDXd6VA/Ej7OGdT6/PrGB1J0pFBPjYbWR5mtwxTtMeO1jg9kbHtHP+8gOH42ujNPj0nQuoIYG4+XnjDgnZjtZDibDgvySWY8bAGyGQ/FZ4AC+TV9V/jT6+03I0vROnsWdmZkac3DnnysSWDIwHAYT8V0ceRFISZQ8WWlo4cPsvlRAEREBzaef1Vq1LUWnFBaHDxAWt7WC0tJulVm9x9wrK2ESZFgx+HEGOLbGzzNaHUO133VavGLw323Oz0upUSnCD/ViP77+yyaPTeWI5Hb784Av0HmBs36cKY1bLbvgjFkl8bg70IsgLZmhia2wyAEjyl4aGk/U/KlWGzXlNLnCmvAsHyAB37pPZirx01pOeODpVZVLKmqDknlr23LNq0zY4nue3cDbRwDyQaPPyWngaixuNu2n8sBru3Jduoj6Lq6mzIzH4bXBxc4OtpDm0LFWD3WqYPEZjxRuaN0bi8XwS0uPnA9a+a1p0VoWrzLF1fTVw/BaeI492ctIDQyIPhi2yPc3xHfFwRd80BypXUsZohJZ+X4dyN2drr+noot7YpPAx45HH8x1uLNpG4j0vlTOc2seQd6iIv7NpYrSeuL9ePc2saS8CpFpNKPKxzjLWV5Mr+jtOTL+a9ztrbF83RHlN+nJUtqGjxPBcB4e1ruGAUSASL/yXV0rC3wnP2+bcRu5uqBr5KUyZ2xN3PNCwOBZ9fQfZa1q0lUxDsSdPsaUrXXWw875f+yrYNxxzPdDHIGloJku23dUARx/2USVYtWyofDm2Pc50zmOosLaq75Pfuq6B810aTbTbR5a/hGm1CLzhPjHm/wCDiiIpTnhERAclxREByXv34cPZFjZOHP1ZrhDtH0sSzOgiDJ5Mp+LIx0+PPivbzA6Mu5DgeF8/r7g/Drq2Li+y/VZcmCDNZF+2HyYM03hNymBrSYXFh3ta4Ai28oCp9LaR0t1/jalpWmaVj6LqmHJm5unyYGIII8vDgaMfDizJ5XO8MyTZcZexo48IEdiFU/wpez3Hd1pm6JrmHiZvuWJqDJoZWjIgE8E0LN7CaDqtwDv94r038GnXeiZ+u5cWF01p+hSM0qZ7suDNyJXyMGXitOPtyPLtc5zXWOfyh9VGewWdjfat1G8vYGn9t04vaGm8qGqddFAeAfiO0rGweqtbxMOCLGggzCyGCFgZFG0RsO1jR2Fkn9V6j+B32WaZr+XnZupM94ZpZhDcKWOOTFyfeIp2kzB3mthY1za9QpD28ewLqPVupNX1LChwpMfLy3SQPdqeDG5zNjWglj5AW8g8FWT8FOXF01rWtdN6tIyDUcp2H4MUbmzwO8LFmypLyoiY21HKw8nuSO4QFR9j3XWja31Bp+jz9FdMwx5mS6J8sWPMZGBsb32ze+ify/Ueq9E9lPsS0LD611vSMnFi1TGj0jFzIW50MTxDJkZItsbWgNa1rfKPoqX7CfYP1FpPVGl6pmw4UeNjZb5Jnt1PCkc1ropGghjJNzuXjsF677IuttN1fr/X8zCyN0LdDwscvlaYPzYMsMlaBLRIB9R3QHk3tQ/DmdG6l0fLxoRm6Pn61gRTY7mB7onT5Ukk2OceFlN09sMYbvceLo/Nenan7LenW+0HC05ui6cMSTpfJyH4vu7fAdO3UPDbOWdvEDPLfyUT7F/xHuZr+paDrszpGP1fNi07PNyP3vzY8XEwDHDGGsxwzxHeK4/deg6tmQn2mae/xY9o6QywXeIzaD+0uxN1f0QHz/7VdfxtK1rUdOxPZ5omVBiZL4ocg6bnOMrAAQ8ui8p7n4eF4l7WOqodRkgjZ0/pugvxfEEseBBNA+Yv2lvjsmN20N44HxlfVXtS072nS6zqMmjaoyPT35LzgsGpaUwNhobQGS+ZvN8O5XzL7eOkeosDNZm9RvjmytT3O8duXi5T5fAZHF5/djTKZ4QHA4H0QHqv4CejNJ1jJ1tuqafiZ4ghwXQjKiEoiL5JmvLL+EkBt/YL5x6jiazMy2MaGtZkzta1ooNa2Vwa0fQABe9fgp13W8HI1g6NpmHqTpIsMTty9Sj04RBskpjLDIPzS4l1gdto+a8D1173ZWS57Qx5yJi9jXbg1xkcXNDh8QBsWgNJFxRAfTv4TNV0fW9RwdAzultClDMLIdJqDsd78yd8Ee8PlLnbC5x78KD/ABSa9peFqOr9N4PTOiYYx5sZkWpY8Mkea0bIMl1EO2jduLDx8JK6PwJStZ1hjue5rQMHUOXODRzCAOXGlX/xavDuttdc0hwOTj0QQQf7Hj9iDSA9RzegNJ9n+he9dQ4GLq+samJG4eFkQty9NgdjzgkiePY9m/HmY49/M0DsLWh7Y/ZhpWtaGeselom4mLCyRudgvijw4Ym4rAyWXGiG50kjpXDu7kBexfjT6x0nT4NFOdomDr4kfliNs+ZLF7sWxw7i33Yndv3D4v4FGaP1Fp+f7LdblwtPxdHjfj6k1uBBkumaHNlaHSAzHcXP719BSAr/ALf/AGRYUnTPSo0PSMSHP1LL0qKXIgxyxzvH06QudkysB2QmUsc5zuAQCqf7RNM6b6K0ZukS4ODreu5kbJ8iXKijni08SwPxciHGysdzSHw5GPvYx4v8wk9wF7J7dvaRmdO9K9JZ2nZA3MyNIblQMljHvUDdMfLJiymnOZG90TQSBYXkXtO6C0zrDSn9WdMiHHyY7/bWmEjHj958KTUNRymz5cgdPIDPCwBjadVjmwgLqemtH0z2faNrkPS2latnS42niVs+HJM+Yyktllf4HnL+LvtyvI8/2lQwRukm9nPT8LG0DJLp+dGwWabb3EAWeO6+jdGGtzeznQYem8pkGo+56cWu95xYHCIFxmBdkeUeUt4PK8g6u6C9qWrYcuBqOdFlY0xYZYJNV0kMf4cjZY72EHh7Gu792hAfK5KWhWEBa/Zv1Vj6TkSz5GkadrLZITG2DUmPfFE7e1/jMEbgRJTS37OK+uPa7i9O6L0hpPUcPSWgTT6j+zfEx5cZwgj96w5Ml+wscHHa6MAWexXw6F9p/idyY3ezDppjXsLmnQbaHsc4VpcwNgGx3QGl+FnpXROodJ6n1LL0HTPEGbO7EhZjl7MRpwRI2DGDiXCMP5A+ZXlH4UegzmdVYGPq2kyTYj4s3xY8zDm93JbhSvjLzIwNBDw2rPel7P8AgJzhB0z1G8StikblSOjJexrg5unNLXNDjyQ6v5Ko/hQ9snUeqdVYGFqms5GRiyRZplim93bG4swpXx7nCMEU8NPfuAgPLvxZaJh6b1bqmHgY0OJjwjE8OCBgjiZuw4XvLWjgEuLnH6lfQnSMHT+T0HldVP6S6f8AecVmTtxxjOMEngTtgBe4u3W4Ek0e68J/GhI1/Wurua4OBGFRaQ4H+wQeoNL6U6G9n+ow+zXM6ekGKNQymZfgw++4pY4T5LJo7mD9jTss8n0QHzv+FHorS+pOpJv2kYseGD+2RYI8IY+S45bAMDZMbdDskI2t81NXoEms6CNV1nStU6HxcPCiOo4uLqOl6Pl5GZ4jJjj48zA+mfBuk3Djc1tcFeO+wjpzGl6iiw83VptFyoMpkeBk42OzM/tzMlsbG7i7ZGwEOd4htvlHzX0bpuie0+HWIvE1r3nTotSZvkfqGksdPhMyRue6Fo3Nc+AWWDkbqQHxz1biY0Gdlw4bsl2PFO9sDsyLwMoxg00zwj+7lru1RNr3T8amZoc3Ucn7HY1srPHbq7mslaJM73l5kk3SOLZLbt8zPKurXPYliY/RMHVbdUc+eWPGcdPMUQa3xssYxHiCXcaB3fCgPEVi1hEAREQBERAc2dx91eW4cTo3NYGtEjWguZRPBB+ddwqMByr5p2P4UbWBxdXN1R5o9lRvnhRaZ6X8O01OVROOVjny5Ks175pmQue8tDw0WboXXA+ysE+kQvY1m0NqvO0DcaFc38+6jenoQciUuFltlvfg7xyrBI8NBceAASf0UFzVlGSUTp9KsqdSlOpVWct89kirY+KY8iRgY2QMElCSwCG3zwfioKe01kTmNkayNriDez927Fd+OFq5WdASX73WI3sDfDPO4O9fT4l3aBjhkW4OJ8SnVVVW4Vd8rNabcMvZ7GnTqEKdxohiS3fbbjHr6HRqckLMiF5NPDgZD5uG03bx27fJceo84NjDGPovHmFd2ObY7haeQI585ove1xjBonnytBAK78HDOS97pWlzGN2MI8o8pAANdztW6hGKjKXZEEq9Sq6lKkl8Umk16cvbzO3pSdvhGO/NuLttHtQF32W147XZTQ02WMcHDng2eOV1ZWnRQsMkUb3ObZFONNoE7zY5aKHCjenZXSZLnHkua8mh8/oFq4xnqqR8iSNapQ8O1qJZyuM8G/1V4Xheb4+Nnftfm7cfzVSVg6ulaXMaDZYCHDng3dG1AFWrRNU1k4nW6indSxjbC2OKIisnICIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIDm08j7q5Z+oMbj+Ix/LhUZ2nlzS3dwR8j6qmsHKskmIXztgAJii2uI9Rva0uJd35Kq3EIvDl23O10mtVhGap8yxH3ef4ya/S+S0TP3nmQU3ju4uBrjspbV5wHRR35vFYao9rIu/usP0aBoJbE5xAsNDjZ+gUGJ3vyYw4Vse1jWmraA6g013I+agSjVlrj2Oo6lazoqhUx8T2a+e5ZNX8PwneL8PNXfxU7b2WvpuZEMdp30GNp3B8pJdtHbldXVUrRFsJpxcCG83XmF/a1HSY7vBhiiaT47Nz29y4tc7kE9hXyWlKkpU1q8yxdXrpXLdNJ4j75fHHqNHgicIt7JA57iGvDgGk36cdwpbOxTFEDCa8Jxk85u+BxwOe3qtCaAhmPDHIzd4j6LH2Be2uRyFL5rSMd4PcRGz8yG8pWm9cXnl8e5pY0YqjUTW6iviXnhPGV5MgcSSXMlpxDQ1vmAtoLQeRQ9eVt5uh7fNC/YGtcTuJs1Z4LR8qWelcZux0gvdZb9KoH+ampHNAtxAHbzEAc+nKxWruFTTDjyN7Hp0K9v4lbeT3zn+SoYbYy2R0zJXUR5mkAC7+Ikdyo1ysuqNYyHI2vj/ADHxlrWOFgC78o+6rRXQpS1bnmL6l4TUdnzv7nBERSlAIiIAiIgCIiAys0sKS6ewpZ52CKCXI2HxHxwxOld4bCC9xY0HygdyeOViTwsm8I6pJHY7p/OAgccTIAyonS45MT/z42Eh8kXHnYC0gkfIpomkPynHzNijbXiTybhFFd7PEc0HbuIofVejYsc2oMzWRGSExTxsxGylzHYsLvEc+CJovwWuvljeCVPSdLQRY78ExyRg7fEJa1k7qf4rfEJaLPPqOy41fq8aXwy5yvZc5+/1PY2P4TlX+NP4cN77ZabSX1W/zPF9E0x2XkxYzHNa6V20Ode0fU0Ca/RaeRGWPcw/uuIJ+xpekTaRjftN+Y8yxYGP4DpX6fsZM5uxkbvc3EeGZRIebI9V59qmOY5XgtkaCdzBMNshY4ksc75kto2OF0qNdVHleS28mefv7F2y0yW+p/F2a4WPdM0URFYOWEREAREQBERAd0UbnuaxoLnOIa1oFkkmgAPUkle0aF+HDW8jFbkSvhwnV+bj5UeVHPjEuLWNnaISGOcA1w57PC8k6dhkflQCJj5HCWNwbG0uedrwfKG82vvHVun9ay87RtTidlx4bo8852HIcps8riPDxjkYwaWOc1wsbzwOy5XUrqrSSVLybbxnhbL3Z1LC1hUWqpxlJdvn9EfNOu/hw1vHxXZET4c11flY+LHlST5JDg17YWmEB7mguceezCvF5Y3Mc5jgWuaS1zSKIINEEehBC+/tJ6f1rEztZ1OV2XJhtjwDhYcZynTxOA8PJOPjFoa1zjydh5F2vg7qKGRmVOJWPjcZZHFsjSx43PJ8wdzadMuqtVNVfJNPGOVuvZi/tYQWqnxlp9/l9URiIi6pywiIgCIiAIiIDmpT/Z7OrHd7pkAZbHvxXeE+shkZIkfCa/Ma0tNkdqXVoeDNPM1kMEuQ4ed0cMbpX7GeZ7trQTtA7nsvS8USZ4zo4fEh8KWFuGybdG7EjcXOljiaL8AO9Wt4Nqrc3Ko79u/pvg6/TOmO7eE9+yXfZv8Ag830TSJMp5FtijbXiTybhDFdhpkc0HaCeB9SsaNpj8rIjxmlrXSvDA517b+ZoXS9o/2Wghxn4JjkjDqEhc1rMh3nErd5Leeaqx2VSytHxjqRyneJHg4rYHTvwCxszmhrGSDFfWw5G5wuyPVUaHVYVpSS28v4+vl6HavfwvO1pwm/i4bSfzb9klz6nnGZAY5HxkgljnNJHYkEji/sulb2sw7Jn+WVrXOc6LxxUro3EmNz/QuLaJI4u1oLrxeUeSqLEmsGERFkjCIiAIiIAiIgObByPuro3TQ1jgxzg57Wjc9xNUWkdhfoqW1XzTInsjY2R2518myeDVclUr2Tik0z0n4epxnKalHO3PlyVuTNmneyAuDaeGhwFc/DZI5KkJ9AaWjY4iTjc5zjRNc1QvutXQsZr8iRxu4yXNr57x3+ishNc9q7kqCvWdNpQ2Oj02xjc05Tr75eE2+Ev2KjFB+c5kwkkEYdew8+X1sj4fVT2m4UVMlZvHldtDnXQILT2H3WMgRb3Sh0Q/JkaQHNtziHc16nkJ09E9sVudYfRYLJ2jzCueyzWqNwzxwa2FrGncaGlLl58sYw8nTk40UeTC9pDbeAW2A1oFUe/F/VdvUGX4cNDaTJbSCeQC34gAVG6nCJc1rN1BxjFjmra30XJmN73K5rjtDGNaCBuvbTL5KzoXwym+FlkcriS8SjRjjVJpb+m5udKuHgkWL3k1Yuto5rvS2Z3B87GGnN2OLmXY3Au5IvgrR9wbiAyCV3yrZw71DTTuAa7rX0Gfxcp76rcHmvla1lBScqkXtglp3EqUKdrUjiWVnfO397Gx1JhRCLe0NYRVNFDdZ5NdzSrCsPWDuY/qDx+qrqt2mfDTZwut6PzMlBYxjg4oiKycgIiIAiIgCIiA5hXr2N5MsGc+VkjoQ6CWMyB2wO3gXGXHg7v4fVUReleyqfGkgkxJBuf4vitY4O2jYyg/cCPMLPCpdRlpoS2+Z3Pw7SVS+gm0sPKz3a7e57X7O+nPEnfkmCPwqeZd7SDK8sPhvDSKko+oPBXHN0KeZmFMXyOmzGzGZ+QdjIzEdrd7y3y20fvd+KV89mLoctmIDlyxMxoXRZETYtzHyP5jJJFmvm3herZfs+97gxYciFga5svvh3B9kODobF+fkDt2XgqNvWrtuKzjH+v+/Y+h33XIWVfTPbnt23+ufT0Pk7U8eJ5dF7rFjxu2g40bHMiHa3BjufMRuv5ryLr3HM0Mea9pje6V0HhgEMDIo2hhG7myP04X1j7WulmRNmmftimgaC/YWv8YENaxrnX2DfkF8te17Vt0jcTa0iPbIJA4kneytpHYUuv0SpUdfTjfvnt5/XYqfiCrbVum+ItlskscvbG/os/U86REXsz5WEREAREQGVtaZiPyJooI63zSxxss0Nz3BjbPoLI5Wqt3Rc042Tj5AaHGCaKUNJoOMbw/aSOwNUsSzh4N4Yysn0f7EfZti42qDE1CYQywiWSeaN0R8OSAtPhwySCnRuB54vhfQGDPP1pkZDsPWdW0TG04xNg/ZsjYJMts8bXudlslDqex8bmt2+jja+bcnXTqMcmoOYyJ2U2SYxtfvbE4h1NDnck+Ud1Oew/wBoGdpEcGVG50olbIcjHe/azIIMscRkdsLgWAgiu9C15a3v505OVb/6w/o8eywfS73oVO5t4wt/1aE4rhLdOTz5vONz3bNnn6LyMc5mtatreNqJlbP+0pGzyYjYI3Pa7EZEG2975Gtdu9Gil4B7bfZti5OqHEwJhNLMIpIJ5HRjxJJy4+HNJGKbG0DihfK2fbh7QM7Vo58qR7ohE2M4+O125kBJijlMb9gcS8Ak38+FB42unTo49QaxkrsVscwjc/Y2VwDbaXN5HxHt8kuL+dSSlR/+sL6LPs8iy6FTtreULj9XhtyXKe70vPmuNj5/1PEfjzSwSVvhlkjfRsbmOLHUfUWDytZbmtZpycnIyC0MM80spaDYaZHl+0E9wLpaS9THONz5nPGXgwiIsmoREQBERAXn2P5EkGoeMyR0I8GZhka7YPPGRsLu3m7V6r372ddNCXJdkOgjMXm8YvaQZXFjhG4AipNp9fReI+yybGljkw5Rve+UStYQ4N8jPiLmkURzwvqX2XvhyY8Rpy5Ym4kb2ZMbYt7Xvk3OiJsWa/3fnyvE9eqSdbC2fHpjt9z6j0HFv0zxI4eW22t3F43W32+ZRczQp5o8OdzpHTZZnErsgljI/CO1he8ttltH730pQOqY0TnOi90hxo3BrXY8bHMh9Nz9rubcQHX60F9Y5XQBysbGx54WAP8AF99O8OsA7obF+fkN7dl5L7Wuk2Rsmlftimx2biWFrvFaBsja510ABzxyubUo1rdJyTSePrjP2ydLpvXKF3Pw3hvdL0TePpt9MZ5Pk7r7H8aBua9vhvE7sZsQBDBHEwFjhu5vmvlwqKvRva9q25zMTa0hu2TxA4k8tLdldgAvOV7vp0pSoxcljy+XY+cfiKNON7OMHnHLxjL7nFERXThhERAEREAREQHbF3H3Cu+XlCOEyAtJa0bQXCnG2ggUee/oqM0dlYMiDe+LEs7WG99c+drXci64VW5pqTjntv7Hc6RcTpQmoLd4S+bzj++g6VlBllJoFzeBYFkuHAvupfVJKEbQfjkaHNvktNggjuWrQZojIvzBM8bfNYYCRXyG7kqPkzPGyYj/AAuY2/V1O+Ig9ifkq7hGrPXF7I6ka1W0oKjVWJN7brhvcm9SwYnRu8rY6shwoEkA02yfVc9LkaIIzub5Wc+YcGzQPPBXR1O78g/8Rv8A7lDyAxQMaPN44a8nsWbXOFD5rSFN1KaTfcsXF1G2uG4RW0N8er22+ZnR8ZjnMeMjbKXcN8Muo3xyeFMPjkxogWfmU9z38BttoWPp29FpSwyxR4zWsIeJZKBAv92u/dS2bfu8l9/CN/fbz/Vb1ptyXdNkFhQUKU9mpRWcrPdJ929/MhxqE2U/w4hsaW08eV3B4c7kD0PZcZdLmx3b4HbvKS51NFDmxTifQWu3pTG4dLY5tu2ufQ3anniwRXcEH7EUVpVr+HPRFLHcks+nu6o+NVb1vdPPHyKbE1s5e+ebY6/4C7dwf4eB6fzUe4Kyajh+DBk0wtaZItl+o810Sq3S6FGaksrg8zfUZUmoy/Vu29998fwcERFKUAiIgCIiAIiIDKk+n9Wlw5hLE6j2d28zSRubyDVgd1HrCxOKkmmtiSlVlSmpweGt0z2no72yPx5drbw43uD3vsTcsHkG0xE89uPmvYx+Kpvbxv6H/wCOvjFclypdGo5zByj56Xg70vxFVqr/ADwhN+clv9sHvPtD9sMOTIySEeMwOJbAC5ngna0OdvMQL95v7UvDMuUyPc/tuJNd6s9l0LKtWdhStlin7tlLqPV617pjPCjHhJbI4IiK4coIiIAiIgCIiAsPTOdycabK93gc4SPPheJbmA7BTRu/eI4Ncr2STqjQ/dvGGqgznk4vumRxb6I8XbtNN8y+fQslc686bTuWtTa+WP8AR6Dpv4iuLGOmmk+N3l7LtzsvkfQMfVGh+7eMdVAnHIxfdMjmn0B4u3aLb5l431NndsaHK94gY4yMPheFT5AN4pw3HsBya4UCESz6ZTtm9Lb+eP8AQ6l+Iri+jpqJLndZWz7c7r5nBERdE8+EREAREQBERASWhapLiTCaJ21wBB4abaeHN8wI5HC9X6R9sckEpYwHCZId0km4TctBLBtMRP8Au8fNeMD5oqd1YUbj/wAi38zrWHWLizjopv4W8uLWU/76H2afxVNqvG/of/jLy/2ie2OHKfHJEPHaHkiC3M8J1Dc/xDEC7eb49KXgaKp/wtJtOcpSx2byXIfiGdJPwacIt90t/u2jvz8jxZHyVW5znVd1ZJq1roi6yWFhHAnNybb5ZxREWTQIiIAiIgCIiA5s7j7q5NxZGNke1++SRjA3ytb2La+nw2qa1XvTC8xs8UU++RQHHG3gfRU72Tik0ei/D9OM5TTznGzXblfXfYhZtZmkLI4m7X3RNg7jwOxFDnn9UyNFlbtlY/dIXBxbtAo/ETd0aK6dFxd+S51geGd3bvTgKCtKr1qqotKCXqdGysnewlOu298R34x3SKdM580pZky7CwEXt3cg/DTPrfKnNOwiNkgm8RrGPEY2beCHDv8Ac+q5TYW2V8jWGnQy73ckbiHfPt6J0+6Qx+ccCvD4AtvN9u/K2rVM08x29NjFjaaLjTVTbbeHv2xjO+MexryYPhZMDgSWueA0OJJBAG70pbeuZIjhdYJ3hzRXoa9VFasHyZjY2ktJMe2yQGktbzx2WMmJ+XJta6gxjbDyaLmgNcQBfcoqerTKT4WWaSutCq0qMd3LC+m5v9Lf3B/4h/5QtnM88jInE7XNLzXDrBcB5vko/Bw5cQF5fHto20uPPqdoIA30OF16RleLlvcCdpD9od3A7gfRayp5lKonsTULpwp07ecWpNpNehnqDTdke9rnbW1ua5xJsniuKVbVj6veR4bQTRBseho8cKtlXLVt002cHrShG5lGCxjBhERWDkBERAEREAREQBERAEREAREQBERAEREAREQBERAZW1p+FNkSCKCN8r3XtYxpc40C40ByaAJ/Raq9a9g2PG5uZIWML2GAMeWgvYHCQODXHltjvXdVr258Ck6mM4L/AE6z/NV1SzjJ5O9pBpcbVt9rGPHFquQyNjI2gQ0xjQxouFhNNbwObVSUtGr4kIz80mV7mj4NWVPybRhERSEAREQBERAEREAREQBERAEREAREQBERAEREAREQHYzuPuFfJ5hFGZCCQxrSQO/oPX7qhNVgy2vcI8Xcd9ne6zsIcGuYCe5r7Krc0tbjn+o7vR7t0IVMLLaSXz3x/fQz0s/dLMfm2/8A7wpjUXlrWgcb3hjvs4G6PofqojD0eaFweJIxVE25waRfZ3HZdeVneLkRAE01zA4A8FwdyW89vkVXnTVSpqi8o6dC6nb23hVItSb29cskNQ0obHeG94Is+ZxqgDYoDv2W3pXEEf8AgP8Am5a/Ub3NhcWkjzgccd93CiRM+LGDS43LtdGQTTQC4OB+X6KONOVWmsvuWatzTtLltR/9N/4GlwzSSMyN8bnB3AfJ5jt4AIu6UlHeMwOexpL5Dvc23EMNHg/p6qOhqCPGkDbcJX3dgurbQP0U9muvHkPa4Sa+7bpS1p/El2exVsaKVOUstTitXnyk88dyKzdVE58KOMPDhVvBBaTY3CjQq+60ooJsOQO2h1tPayK5HcevC2ek8dwc6WvKQW3frbTVd6VgeLBFkWCD+oIWlSrGi9CW3c3trKpew/MTk1PPw7FTe2TLLnl7GhvZrnhoF2aaHHtwop3Cm8nCZHFk+pY+MNcQQaO66F0oNX6TTW3B5y+pyhJa/wBTy28+rX8HFERSlAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIDkF677Af7rP/xY/wDlIvJsWIyPaxvd7mtHpySAOfTuvov2VezTVtObmR5MUAc98VBmVDIRtDw7cGE7e4791xevV4U7VqTSbxhee6Ov0OvTpXkJTaS35+R4/wC2L/8AV8n/AAwf/wCDFUF7B7ZPZzqjZs7VHRw+7wsgdIRkwukaNscNmIHf8ZHp9V4+rnTK0KlvDS08JJ47PCKd/VhUuakoPK1P9ziiIrxUCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiA5s7j7q3NikZ4k72MLtjNoFmiNrePUGlUW/NXvSsgyxMeW7STVC/ShfKp3knFJnoeg0o1JTTeHjK+6z7ZIzK11haGsZvc7hzXtNdhYFOs8qOlwZoi3I2N5cHBgs1fmA29wPRZ0jHc/J3NHwP3O5qhu7/AFVsUFSpGhhRXPJ0La1qdQTqVZYw8RwvuVPIypct/hnbHQNtLi1pIvvuPxc0pTFwZCYvEbG5kTHgUd26w4g/Xk+i4ZOCwZL3O8++KV/Ira6nVVH0pd/T+SXx7S2vDoA883ZsrNWpiGYcf7MWdtm4ca7bbb99OHusHRIyduRAJHmRu8bHUBzQ3cDlb2sTtZA/ca3NLW8E2a7cKL1fIlOSxkfJaWlgoE7nNaT3HK69WfJkuEcf5gaxjnAACnUA+yRfc0sKm5OMnhbZMyu40Y1adNNtvCzv2x83g3ulf7g/8Q/5BbeVI8vbE12wuaXb63VVgt2n5qN0VmRjgh8TtnJPby9rcTV0AOyzp+YZct3mDmtbIGGq8vJHpz+q0nT+OU+VyT212o0KdB5Um0muNu/qcOoI8hsf94ZGGt/lDaN+X6lVpWfq2dzWsjB8rxbhQ5p3HPoqwr1q26abPPdaUY3LjFvbHLz9DiiIrByAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgO+CVzHNc005pBafkQbB/mvpv8Lms5OoO13My5TLPPNhOmlLGNLz4czQS1gDRwB2C+X1zilc34XObfyJH+SodSsFd0XTzhvvjPdP+DaEtMtS5/vlg9Z/EFr2Xja7rWLDMWQ50WAzKjDWETNjx4ZIwS5ttp4B8tLyMrk9xPJJJ+ZNlcFYtbdUKUYLsks45wsZMN5bfmYREU5gIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIDnH3H3C9AfK1jN7zQaGknk12HYKgBWLOyZnRMgu5XlwezaLryuj9KH6KpdUtbid/o10qEajxvhY+fkOmHAzTEdiDX/wDcKZzpixra7vcGA/wkj4vrXyVf0nFyoXbhG4g0HChZFg1z2WzqGdvnhjaezmlza5a/cQQTVmlXq0tVTK3WDqWl46NtoknGTfdY5fY2c+HJbG4tmLu9t2Bvlo7jf2W3pR/Ij+jT/mV1dQTujhc5hol23sDwQQe6i4c2WPG8xpx2+DbR5m24Orijz81GoSq0+3JYlXpWty86n8OXl5/fzOrCM0k7Mkxuc0OHwNoENoUPS+FIYDW448R7XMdK8tO40GtsOsilo4Z8BmPJueQZHhzQfLQrs39VN6iGvgeaB/LLhYBq23Y+RU1aW6jjZ7FKwpfBKpn4o/Fvvu0nn3NHV8+J48Ju6QuFtLHfvEEAHjn7KK08uxJd0jHi2uodjzxfPotjpaG5HOLbaGmnEWA6weCf3lYcmBrwQWtJ2kAuaDVg1yRxytZ1I0f8eMrubULatfL8znEk/h28v3KxnyS5bi6ONzmR3VN5aDz5iO57qHU17o6GLJO9wcx8Y8riGnduu/n2UMr9LGMR4R529U9SlUzqeW/rj+DgiIpCiEREAREQBERAEREAREQBERAEREAREQBERAZSlO9JdLZ2rTOgwIDPI2N0haHMZTGkBx3SOA7ubxd8q1N9ifUlgDTjyaH9oxfXj/8AdVete0KUtNScU/JtL9zSVWEXhs83Rd+Vjvie6N42uY4tcD6EGiP5rqVlNNZRucURFgBERAEREAREQBERAEREAREQBERAEREAREQBERAEREBzZ3/VWpjPzH5L43tDGRlgPFkbWH05VWjPI+6veFKyWNrgLa7ja4Dmq7jtSqXc9KTx6HoOhUVVlLfdYaXqs7+xp52qQiMc794otY4BzbAPeuD6KAEL4pGz+G8M3gtJ7kXuHPYmlz0+EuyRTdzWv8wqxW71HyVsdG0gAtaQOwIBA+wKrylG32W+eS/To1epZqTeNLxHC7lc1PPfl1FCxxHxFtAusXzY9KIWxDhukMDJYpGtjY8OJ4s+Zwo1x6LjJp+3IedxaHRyyM8M7aA3ENPHbjsFI6JkiSIDzEs4cXc2TuP68LapNQh8C2/2YtKEq1w1Xe727Yelp4waMjnHIhhfFG1rX3TAdrtwBI5PPopPU3BsDxYH5bgASB6cAWozWtRLMiNoaD4RDh35LmtPK6epcsvDIw0HyseSLJtzeWmvktdEpuD47kruadvTrRT1POFt6Yx7G70qPyD/AMQ/5Bb2RM4OEbAC5w3AO4btF3yDd8KF6bzfDHhvaQCbDqN2aAHyA+q24MrxMwtoDw2vaCObonlR1KT8SUmtuSeyvIq2hTTw21E1dfllbGWOjjAeQXPbZPB4s3SritfVWUWxiKgRJzdnjafkqoAr9q8084PO9bio3LipZwu/bucURFYOOEREAREQBERAEREAREQBERAEREAREQGVvaFE2TKxo3jc188LXD5tdIA4cfQrRXfhGQSRmLdvD2+Hsvdv3DbtrnddUsSWzNo8o+2ehumsLR3ajj4jtkc+e6RsD2+GIKbsbDC57y6eMCvP+is7yALJAA7k0APuT2XmvSxzdQxcJuWZmajjwNEhyA5j/K4ue6YvG9uTvLeKHCtGpafqU8LYXPxwKp7hJJulG2qksUQTz918X6pRcrhupPLzu36be5N1Ho1BVovxFFS3kpbOKfkede3bpLBkxdc1d1zZAx9NbASwtjxtszIXuila/bM57DRBHlpfMK+j/wAQ8ebDpww8acsxcYb8xm9zTk+O+F0bXNA2vayUEjt39V83r6X+G3J2iblq8vRJJJfyTXlvToaYU8taU033zvk4oiLvFEIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgObRyPur/C1rGgDaxor5Bo7WVQG+n3Vl1HUS7Gb5Rc25pAJtu0tIIH1VO7pubikeg6Jcwt41JS5xsY6ZP5032P/ADhTOVMIwPm47WfLce1/IKr6DkmF5LgacAHGjYFgkj6qW1PN3SQsABDnRvv15JFEeir16LlU9DqWF9Gna4ziWf3Zz1CWdjC50cR4LLBcXAOBuueB3WzozGiFhAAttuIHc27k/NY1rKMUT3AXZLeb7ODhfCj8HUy3Gcdo8m1oBJ8wdus9/T6LTTKpT2Xcs+LStrr45N/C3uuPt3NKLPD8tk7hsaHMvu6g0AXwL9FIaG1rC6Uv/vXOja2jz5muHK19KlfEyAue0RvkcHNLAS2iLs1fqpXVYWSQOJ52sL20a5rg8d1NWkk1Ds9jn2VJyg67eZL4sNY3aznZ8Y42OvW8prWGMymNxaSBtLtwII2/Sz6qB0HIbFNukO0bXC6J7jjsuzpqFr5jvBO0W3k8EEUfqrBqGDHKLezc4NcG0SOeSOB9VhyhS/xvvyzMKVe9auoYTi9lv28/+iua/nNneNvLWWA7nzXzdeiilM4zZoIpyHBmxzA5hY1xO7cByRxQ/wA1ClXqKSWI8I8/fOc566n6pbvbHp/BxREUhRCIiAIiIAiIgCIiAIiIAiIgCIiAIiIDK29IyRDPDKQSIpY3kDuQ14cQL9eFqrisNZWDKeHk+1ekdcwtXB1DS5mtyJ7dkQTl0vu+/wAz4ntY0DxBTDYJHKnsluoRsMj58NjWiy50EwaB8zz2XxL031Dl6c8y4kpjc5paeA4USCfK4EXwOVKdOdc5uLluyHyyTNmcTkROfxI0v3ua3cCI7PqBwvD3f4TnOpKVOax2TWX8slyVVV6kXVaedm3FPC9GeofiglhbBge75UkpmfkjJHiuc121sJYC0geUOLqBul4IVaevurZNUkZbPCiivwora4tLmtEhMgaC6ywGj2VXXp+k2krW2jSlys5+preODqNQk2lsm/7wcERF0ioEREAREQBERAEREAREQBERAEREAREQBERAEREAREQHNp5H3VmiLJMh2RvIbE1hvaeeGsP1HKrLO4V8j8OaOhTmOABqxdVY+fdVLqenHrsd7olDxXLdbYaT7tZx7ZMZmUxjNzpNm8eV9F1Ggbr7KoxS1kB7nEt8Sy8gixuvdX9VzxIt2S1hst8Sqv03V3VsnxInsbG5ttbVCyKoUOR9FDmNDZ75Oh4dbqXxxxHQ9lvuyE6h1OORnhx+YEhxdRFVYqiPsutsbcj3aMOI2Rv3naeCC59c9+FmHCkiyJPDPhgMlcwkB9sF8c/Ou6mtLyGyxA7g5wFPoVRN/T5fJZnJU4fB/cmLejO6rvxnhvbGOVFp4TzkiZRG+SHH8OSMCQlweefMG/RTGoNrHkA9IiP0ApR2q5rI8iIFp3McHPIAsggEAH1/VdXU2aNrY27gSGuPyLXN4HHdRuEqkoY2XJP49OhTrZab/TxjthL2NjpUDwSaF+Iea57D1+SksifZwGlzj2Y34iObd9hShul8xgYYz5Xbi4E0AeAKH+8ttuQ1+XtF+SN7XX8wT2+ijq0m6km1tyWbG7jG1hGL3bUfuaGt5FRyNMT2OlLXEvqjtJ7ClXVbOqZmNj2FtufRa6hwAeRfcfoqnS6Fq8wzg811qOm405zheWPU4oiKwccIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgOcY5Cv+DA2NjWMuhRFmzzRKoDO4+6tuo6k33YObvBkBaw9iC0tu6PCpXkJT0peZ6LoVenRVSc+UtjU6cAM83A4Bq/Tzjn6KdmkDBZ+wHq4+jR9Sqx03mNZI7ffnAF+gO4G3X6KY1TKG+GPuS9jgR8JFkcFV7ik5VPQ6vTb2FO1bT3y/uzhn5e25HwSNOx0YcaDfMDx2+pXfoUDWQtc27kALub5BcBXyXbq0rGRPL27hyAKB5IdR5+S0tO1FjcbdTqjAa7t3duquey1eZ0vhXcnThQus1JJ/C3wtvPj0I45Ec2ax3dm5gO8ADgAG+arhbukY+975Jdj2m2Rh5B7EUGg+ldqWro7GgRB8Ee2R7m+ISd3BF2N1ClK6hjNERMZ2eFcja+YH1P2U9Wai1Bbdjm2dGVSMq8sPDcmt1yl59kuDGpRRxxuMbYmuAJF01wFHzM5vddUobp2b+0Fz3clr/M41Z+pPqsaS12XN+a8nY2+ebAcPKfpyVLajo0TgXN/L2tdwwcEgE82f0WMxprw5Pd9woVbmSuaUUoxeyzjOCL6nyWSPa1hvYCCeKNm+CDyFChSmnt2xyvdFHIA5oJeSC27AoAjj/spnSdHjYy5Gte53cHkNon4XNPNilP4kaMMeRz/wAnWv62pbN7v07L58FQQKV1vTfANjlrvhJq+ACePTuurSdPM7wOzRW53HAsAkX3PPZTKrFx1Z2OdKyqxq+Fj4iPpZpbuqYDoH7T2PLT8xZq67HjspjQNIaWiSUB24eVvBFEdzR4P0WJ1oxjqJLfp9WtW8JLD757FZWVO9QaV4dysADb5HA22aAAuyovCxHTPDGiyf09L7rMKsZx1I0uLGrRreE1v29fkaqBSms6W6EgjzNPY8XdAusDtyVsdPaYJfO+i0Hhtg7iCLaRdgVfKw60FDXnY2h0+tKt4OMMhaXFWfXdHaWmSJobtHLRwKAJLrJ5PbhVyKMucGjuTSU60Zx1Ixd2NW3qeHNfL1OtZKl9R0V0UYf3oecWOHbiABXxCq5XTounGd3JprfiNi+bqge/IWfFjp1Z2MOxqqoqTju+COQK36no0cjPy2tY4dgOA6yB5iTx6qplhB2+oNLWlWjUWUSX3TqtrJRn34aOtZUz+w3eD4n73xVYrZtu/v8ARaGn4hlkDBQ+dkDi+e/dbKrFptPginZVYSjGUd5cGqslXGXRYTF4YABH/qV5jV9+aF8fyVUy4HRPMbu7TzRv+oWtKvGpnBPfdMq2qTnw/Lz8joRTGBorpY3P9TWwWOTuo7r7cWoqVhaSPkt41IybSfBVq2tWlFTmsJ8HUiItyuEREAREQBERAc1xpWTp/SWkCWUBwI8reCCCDyaNgg+i6uodKDLljADf3m8ANs0ABdkKBXMNeg6b6TWVv4+NvLvjzIFYpbGFjOleGtFk/wD539FuavpboKPcGueLuhu4HYWpHUipaW9ypC1qzpuolsuWRiypnQNMEp3vraDwLBsgt4Iuw2j3W7rejtLS+IBpaOWjgULJdZPftwo5XEFPQy5S6TWqUHWS28u5WAi5xsLnBoHJUrqGivija/uQPOLHB3UA2u4qlJKpGLSb5KdK1qVIuUVlLkh6RSGjYHjvommt+I2L5uqBPPZT+o6NG5lRtDXN7VxuPA5JPHqo6lzGElFlu26TWuKTqQWy+/yKesrm6Mhxb6gkf9FLDQn+D4l+b4ttitm3df8Ai+illOMeWVKVrVq5UI5xyQxWQtjCxHSyBgofOyBwO/f1Vpl0aHwvDAAI/wDUrznknkXX0UVW4hTaTLdn0utcxlKHbz7vyKaFgrZzcZ0TzG7uPkQe4schb+n6M+WNz+xI/LFjk2AQb+EVaklUjFZb2KtO0q1JuEY7rOfYiFkhdzMZxkDKol1cmh3ruVacPRomx7XNDnOHLiLLSQB5aNEArSrcRglksWfTK1y2o7Y5yU5Fv6vgGB+08g2WniyLIBNdjwu3R9LM9k+Vo7ni7oltA9xa3dWKjqzsQKzqur4SXxeRHNHP8lZmwCTI4LPCiDHFtjwxua0Oodrvuq/lYropCx4og/cfzVybhRGMhgDN7Wgubz6tPz+YVa5qpJPzOr0m0nOU4tfpabT52zt9RLjwtbYZAD+7uADSfqfkquyZxyW7iPLIAOba0B3ZpPZoXOOWSaVkL3uLd+0etD4eB9lPZGjwuY1oAaRVvaPM6hXNmue6iTVHabzkuzhO+eqjFRUXxxlmr1NmMMewO3Fzg7ykFtDcOSD3WoYPEZjxRlo3xkvF0CWlx89fvV810Y+LsyJGCNswYH8SEtBDb83B70FYNOhicxsjY2Mc5p+Gztu2kcn5LMpRowWBRpVL6vJzwuzW/Cazh4wRL2xSeBjskLvO63bCCN1enqprOFY72/KIi/s2rVXk1RzpWzeGwPaQbG6nUAACN3bj0XZma7LIwsprQQQaBsg+nJNLadvKTjjtuQW/U6NOFTPLWFhPjGFyyT6Vgb4bpK824t3c3VA1XbupbImaxu55oXV0T37cD7Kpabq74GljWtIJu3A32r0PZdj9ckMgk2ssNLao1RN38XdR1LSU6jk+Czadao0LZU4/q77ff1NvVsqExzbJC50rmODdjhVXfJ791KaB/wCXi+zv+cqtajqZnA3RsBb2I3Ajmz+9S2MbXXxtDGRxhrew859b7l3zUlW2cqeleZXtOqUqdy6k3tpwsJ+eeG2bXV5d5AWU0E7XXe4kNsfSlu9Mf+XH+N3+TVBahqzp2hr42cXRG4EXV/vV6eq7MPW3xMDGRxgA3++efny5JW83SUO4pdSoRvZV224teW5P65j+LC4F23bb+13taePotXpP+6d/j/6KG1HWJJ2BjmtAsG23fAI9T9VywNYdAzaxjPmSd9k9rPm/yWFbS8LQby6rQd4qyWyW/r7E31O53gEAW3y266o2aFfVafRw4l+7P/ctPL1x8rCx0bCPl5x9uzl1afqroWkNjZzVk7yTV1+9Xr6JGhNUXDuaVOpUZXsa+XpS8i2ZcHixujvbvoXV1yD2UH0q3bLK27pv/vatTK12SRjmFjAHCiQHWOb48y19N1M497WMJdwXHcTVg18VeixTtpxpyj5klz1ahUuoVY5wuX/GC1ao5whfsG62uDuaobTbvr9lX+kv78/4XLMnUMjgWmOMggg8O7Hg/vLTwdRMLi9sbLN995oH0Hm/zW1K3lGnKLXJFedTo1bmFWLeI87fsXRw4PpYI/mq1pkHg53hg7qvmqu2E9lh3UUhFbGcj5O+38SjtPzTC/xA1rnehdu49DwCL7+q1oW04Rkn3RLf9WoV6tOUf/V5b9PIu0jiGktbucK2tsCzY4v0VP0n/wA2y+PzB+nmW1/tJL/BH/J3+paMObsl8URssEEC30Dd38V3/RbULeVOMk+5H1LqdG4qU5RbxF75Rd1V9Wx/DymOu/EIcRVVbyK+vZP9pJP4Gfyd/qUd74TKZHNa4kk0d1A3fFEH+q1t7acG2yXqXVqFeMVHlNPPkXh/r+qpesknIcXN2ncLbd129VuDqSX+CP8Ak7/UtDLzvEk8R0bL9QC8B3FC/NxX0pZtreVNtsi6t1Olc04xg3s+6LsP+yr3VmLRbLu5dTdtdtrRza6f9o5f4I/5O/1KN1HNdM/e4AGgKbdcCvUrFvbThPUyTqnV7evb+HFNvb0waaIsgroHlTCLJKwgCIiAIiIC19I/3T/8Tf8Aqu/qV7vAcA22mtzrrb5hXHrag8DV3QN2tjZz3J3Ek/P4q/kuzJ118jCx8cZBqx5x27chyoO2m6uvtk9RT6rRVl4GWpYa4Nvo3/1v/o/zKnMqHxGOjvbvG2+9cg3Xqqlp2pugBDGMs/ETuJNGx+9X8l35WvPkY5hYwBwokB1j1483da1bacqupehvZdWoUbTwZbvD++Ta6XZtmlbd7WkX9ntUxqTnCJ+xu87XAi9tDabd9a+Sqem6kYLLWNJPBcdxNWDXDq9FuSdRSOBBjjogg8O7Hg/vLNW2lKpqRrZdVo0rZ0m2m88LjJx6W/8AMf8A0v8A+Uq1n+SpWDqHgvL2Rss3V7ztBFEDzdvva3T1HL/BH/J3+pLi2nUllGeldVoW9B0585b2RywMbwc4Rh26j3qrtt9lY5XOAJa3c4VTbq+e1+ipWFmGJ+8Na53oXbuPnVEf1Uj/ALRy/wAEf8nf6kr205yTXZGOm9WoUKc4vKy21jfCNTAs5bLFHxRY+Xm7WrlapEedtk8URsu7At9A3e74rv8Aot//AGkl/gj/AJO/1LNzbzqYwa9J6pQtozU293ngzrWOWZLXB1+IS4iqq3kV9eys7vX9f+qozs0ulMrmtcS4nadwaCTfFG/6qRPUcv8ABH/J3+pYr205qKXY3sOrUKE6knlKT2XJqa2XHIfubtdbbbd1wPUK5M7D/CP8gqTl5/iSCR0bL9QN9O4oX5uK+lLeHUcv8Ef8nf6lm4t5VIxS7EfTOpULerUnNt6ntt8+fqbPVWPy2XdySG7a7UO9qbwv7qL/AIbP+UKm52oOlkEjmt4obRuDSB+t/wBVvR9QyNAbsYAAAPi7DgfvLFS2nKnGPdElr1ahTuZ1N0pcf7HVTnGVoc2gG003e4bjTvp9lPaP/cRf4f8A3FVbUNTM9F8bLbVEbxxZNfFXqtqHX5GNDGxxgAUB5zXr3LltVt5SpqK7Edn1KhSup1pNtPjbclep8XfEH7q8PsK77nAfot3TcbwY2x3urm6rvR7Kqalqr59thrdt/DfN13s/RbTuoZttBrGniiAbFfc0tHbTdNRyTw6vaxuJ1cPdJL18zu6fga6eQuFltkd+DvHPCsLnBoLjwACSfoOVTMDUnwvc8Bri8UdwPzviiFsZWuySbbawbXBwoO5I9DbuyVrWdSeexiw6zQt6LWPiy+3qS+TnQFxf4hsRPYG7Hc7g6ufTuuzp7GDIt26/Ep3attbhX1UJl626Rmx0cZF3xvHPNHh31WcXXZI2NYGspooEh19758y2nbydPSv79jSj1WjGv4k99njCa3fpl9iFREV88sEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQH//Z)
