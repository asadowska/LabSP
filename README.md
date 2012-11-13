#Zadania

##Laboratorium 4

~1. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.

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

~2. Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę.

```sh
find . -type f -exec ls -l '{}' ';' | cut -d ' ' -f1,5,9
```
?

~3. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku.

```sh
ls -S
```

~4. Wyświetl zawartość pliku /etc/passwd posortowaną według numerów UID w kolejności od największego do najmniejszego.

```sh
sort -t : -n -k3 -r /etc/passwd
```

~5. Wyświetl zawartość pliku /etc/passwd posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID.

~6. Podaj liczbę plików każdego użytkownika.

~7. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj ile razy zostało ono przydzielone).

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
```
