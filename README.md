#Zadania

##Laboratorium 4

1\. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.

```sh
ls | tr [:lower:] [:upper:]
```
dla polskich liter
```sh
ls | tr [:lower:]ąćęóśłżź [:upper:]ĄĆĘÓŚŁŻŹ
```

or
```sh
ls | tr '[a-z]' '[A-Z]'
```

2\. Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę.

```sh
find . -type f -exec ls -l '{}' ';' | cut -d ' ' -f1,5,9
```
rozwiazanie nie działa dla plików z datami dwucyfrowymi 

```sh
translate 
```

3\. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku.

```sh
ls -S
```

4\. Wyświetl zawartość pliku /etc/passwd posortowaną według numerów UID w kolejności od największego do najmniejszego.

```sh
sort -t: -k3 -nr /etc/passwd
```

5\. Wyświetl zawartość pliku /etc/passwd posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID.

6\. Podaj liczbę plików każdego użytkownika.

```sh

```

7\. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj ile razy zostało ono przydzielone).

Czy potrafisz odpowiedzieć jaki będzie efekt wykonania poniższych poleceń?

```sh
ls -l > lsout.txt
```
odp. Tworzy plik i wpisuje do niego liste plików z bieżącego katalogi
```sh                
ls -la >> lsout.txt                        
```
odp. dopisuje w pliku liste uruchomionych procesów 
```sh
ps >> psout.txt                            
```
odp. dopisuje ilość wolnej pamięci do pliku psout.txt

##Laboratorium 5

1\. Znajdź w swoim katalogu domowym (bez podkatalogów) wszystkie pliki, które zostały zmodyfikowane w ciągu ostatnich dziesięciu dni i wyświetl ich nazwy.
```sh
find ~/ -maxdepth 1 -type f -mtime -10
```
2\. Znajdź wszystkie pliki zwykłe w systemie, które mają w nazwie ciąg znaków „conf” i wyświetl ich nazwy na ekranie.
```sh

```
3\. Znajdź w swoim katalogu domowym wszystkie pliki, które nie były używane w ciągu ostatnich 20 dni.
```sh

```
4\. Znajdź w katalogu /etc wszystkie niepuste podkatalogi i pliki o nazwach zaczynających się na literę „a”.
Zadania różne
```sh

```
5\. Z bieżącego katalogu usuń pliki, których nazwa zaczyna się na literę „x” i zawiera dokładnie trzy znaki.
```sh

```
6\. Skonstruuj polecenie tworzące katalog, którego nazwą będzie aktualna (w momencie wywołania) systemowa data w formacie rrrr-mm-dd.
```sh

```
