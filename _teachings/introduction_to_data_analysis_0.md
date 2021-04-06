---
layout: page
title: Introduction to Data Analysis with Python 
description: PART -1 Setup
img: /assets/img/teachings/intro_to_d_a/markus-spiske-FXFz-sW0uwo-unsplash.jpg
importance: 1
---

Cover photo by <a href="https://unsplash.com/@markusspiske?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Markus Spiske</a> on <a href="https://unsplash.com/collections/2488721/data-science?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>


# Przygotowanie środowiska pracy
1. Podstawowe informacje
2. Instalacja
3. IDE
4. Jupyter notebook & Google Colab
5. Hello world

## 1. Podstawowe informacje
Python jest *interpretowanym*, *wieloparadygmatowym* językiem wysokiego poziomu do zastosowań ogólnych z *dynamicznym* i *silnym* typowaniem danych. 

* Interpretowany - skrypt programu **nie musi być** wcześniej **kompilowany**, podczas uruchamiania jest na bieżąco interpretowany przez wbudowany interpreter

* Wieloparadygmatowy - nie ma jednego podejścia (paradygmatu) w jakim należy używać tego języka, można pisać m.in. **obiektowo** jak i **strukturalnie** (na tych warsztatach skupimy się na tym ostatnim)

* Typowanie dynamiczne - przypisanie typu danych do wartości przechowywanych w zmiennych odbywa się w trakcie działania programu

* Typowanie silne - nie można wymusić dla jednego typu danych by automatycznie zachował się jako drugi typ danych (musimy dokonać konwersji typów o ile jest to możliwe)

Obecnie nadal istnieją dwie wersje Pythona (Python 2 oraz Python 3) różniące się, nie w pełni kompatybilne, lecz od 2020 roku **Python 2** przestał otrzymywać wspieranie. **Obecny kod powinien być więc pisany tylko i wyłącznie w wersji 3!**

 Istnieje wiele źródeł informacji pisanych w Pythonie 2, można je wykorzystywać mając świadomość, że część rzeczy może być inaczej realizowana w Pythonie 3, na przykład podejście do funkcji **print**.

## 2. Instalacja
W celu pobrania Pythona należy wejść na 
[oficjalną stronę dystrybutora](https://www.python.org/downloads/) i postępować z instrukcjami zgodnymi z systemem operacyjnym na którym pracujemy.

#### Dodatkowe informacje przydatne do instalacji:
(PL)
[DjangoGirls](https://tutorial.djangogirls.org/pl/installation/)

#### Windows:
[Python Docs](https://docs.python.org/3/using/windows.html)

[Guru99](https://www.guru99.com/how-to-install-python.html)


#### Linux:
https://tecadmin.net/install-python-3-8-ubuntu/

``` apt-get install python```

#### MacOS:
```brew install python```

## 3. IDE 
>IDE (*ang. integrated development environment*; *pol. zintegrowane środowisko programistyczne)* - zbiór narzędzi do tworzenia oprogramowania

Pomimo iż nic nie stoi na przeszkodzie, żebyśmy pisali programy w konsoli terminalu, dla ułatwienia naszej pracy możemy skorzystać z przeróżnych programów mających na celu ułatwienie nam pracy.

Ze swojej strony jako IDE mogę polecić [PyCharm](https://www.jetbrains.com/pycharm/) oferujące darmową wersję **Community** oraz płatną wersję **Professional**, która jest dostępna **za darmo dla wszystkich studentów naszej uczelni** (muszą oni wyrobić mail uczelniany, informacja sprawdzona dla 2019 roku).

Jest to dość potężne oprogramowanie, którego wszystkich dobrodziejstw nie wykorzystamy, lecz posiada bardzo dobry system podpowiedzi, który może być przydatny na początkowym etapie nauki tego języka.

## 4. Jupyter notebook & Google Colab

### Jupyter notebook 

Jupyter notebook to technologia która umożliwia nam tworzenie interaktywnych dokumentów w których możemy zagnieżdżać fragmenty kodu oraz je uruchamiać. Idealne rozwiązanie do wizualizacji danych, demonstracji kodu etc. 

To co właśnie czytasz to dokument utworzony w tej technologii!

Więcej informacji na ten temat możesz znaleźć m.in. [na stronie twórców](https://jupyter.org). Osobiście polecam instalacje tej technologii w ramach pakietu [Anaconda](https://www.anaconda.com/distribution/) zawierającej wszelkie potrzebne biblioteki jeżeli chcemy zacząć naszą przygodę z analizą danych w Pythonie.

### Google Colab

Google Colab jest rozwiązaniem Google które dostarcza i obsługuje środowisko Jupyter notebook. Dzięki temu nie musimy nic pobierać, instalować. Mamy gotowe środowisko do pracy :)

#### Przydatne informacje:

* [Wprowadzenie do Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb)

* [(PL) Konfiguracja Google Colab - połączenie z GitHubem, zmiana runtime'u, ładowanie danych z Google Drive ](https://bulldogjob.pl/news/738-google-colab-pythonowy-obszar-roboczy-w-chmurze)

* [Tutorial Google Colab ze strony, którą bardzo wszystkim polecam](https://towardsdatascience.com/getting-started-with-google-colab-f2fff97f594c)

## 5. Hello world

Jeżeli udało nam się prawidłowo zainstalować i skonfigurować środowisko pracy należy napisać pierwszy program. W tym celu w utworzonym pliku o rozszerzeniu *.py (nie dotyczy to rozwiązania Jupyter) wklejamy poniższą linię:


```python
print("Hello world")
```

    Hello world
    

A następnie zapisujemy plik i uruchamiamy go przez nasze IDE, lub w konsoli otwartej w folderze gdzie znajduje się nasz zapisany plik (przykładowo *main.py*)

``` python main.py ```

lub

``` python3 main.py ```

Jeżeli wszystko poszło dobrze, to właśnie udało Ci się napisać pierwszy program w Pythonie 😃