# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Mettre une chaîne en majuscule](#upper)
> + [Mettre une chaîne en minuscule](#lower)
> + [Mettre une chaîne en minuscule sans distinction de casse](#casefold)
> + [Commencer une chaîne par une majuscule](#capitalize)
> + [Commencer chaque mot d'une chaîne par une majuscule](#title)
> + [Inverser les caractères majuscules et minuscules](#swapcase)
> + [Centrer une chaîne dans une autre avec des caractères de remplissage](#center)
> + [Compter le nombre d'occurences d'une chaîne dans une autre chaîne](#count)
> + [Récupérer l'indice le plus bas d'une chaîne où se trouve une autre chaîne](#find--index)
> + [Vérifier si une chaîne commence par une suite de caractères](#startswith)
> + [Vérifier si une chaîne se termine par une suite de caractères](#endswith)
> + [Vérifier si tous les caractères d'une chaîne sont en majuscule](#isupper)
> + [Vérifier si tous les caractères d'une chaîne sont en minuscule](#islower)
> + [Vérifier si tous les caractères d'une chaîne sont alphanumériques](#isalnum)
> + [Vérifier si tous les caractères d'une chaîne sont alphabétiques](#isalpha)
> + [Vérifier si la chaîne est vide ou ne contient que des caractères ASCII](#isascii)
> + [Vérifier si tous les caractères d'une chaîne sont des chiffres](#isdigit)
> + [Vérifier si tous les caractères d'une chaîne sont numériques](#isnumeric)
> + [Vérifier si tous les caractères d'une chaîne sont décimaux](#isdecimal)
> + [Vérifier si tous les caractères d'une chaîne sont des espaces](#isspace)
> + [Vérifier si tous les caractères d'une chaîne sont imprimables](#isprintable)
> + [Vérifier si chaque mot d'une chaîne commence par une majuscule](#istitle)
> + [Vérifier si une chaîne est un identifiant valide en Python](#isidentifier)
> + [Concaténer les chaînes d'un type itérable dans une autre chaîne](#join)
> + [Remplacer une chaîne par une autre](#replace)
> + [Convertir une chaîne en liste composée des portions de celle-ci](#split)
> + [Convertir une chaîne en liste composée des lignes de celle-ci](#splitlines)
> + [Convertir une chaîne en séquence immuable d'octets (_bytes_)](#encode)
> + [Formater une chaîne](#format)

---

> [!NOTE]
> Une chaîne de caractères étant **immuable**, les méthodes s'appliquent sur une copie (qu'elle renvoie éventuellement) de celle-ci.

## upper

+ `str.upper()`

```python
s = "EvoluNoob"
print(s.upper()) # EVOLUNOOB
```

## lower

+ `str.lower()`

```python
s = "EvoluNoob"
print(s.lower()) # evolunoob
```

## casefold

+ `str.casefold()`

```python
s = "Ein Großes Haus"
print(s.casefold()) # ein grosses haus
```

## capitalize

> _Met le premier caractère (ou première lettre du premier caractère) en majuscule et le reste en minuscule_

+ `str.capitalize()`

```python
s = "chuck"
print(s.capitalize()) # Chuck
```

## title

+ `str.title()`

```python
s = "one more light"
print(s.title()) # One More Light
```

## swapcase

+ `str.swapcase()`

```python
s = "Hello World"
print(s.swapcase()) # hELLO wORLD
```

## center

+ `str.center(width, fillchar = ' ')`

```python
s = "Titre du programme"
print(s.center(50))      #                 Titre du programme
print(s.center(50, '-')) # ----------------Titre du programme----------------
```

## count

+ `str.count(sub[, start[, end]])`

```python
s = "Apprendre à programmer en Python"
print(s.count(''))         # 33 (longueur de la chaîne)
print(s.count('e'))        # 4
print(s.count('y', 9))     # 1
print(s.count('y', 3, 15)) # 0
```

## find / index

+ `str.find(sub[, start[, end]])`
+ `str.index(sub[, start[, end]])`
    + _Identique à `str.find()` mais lève une `ValueError` si la chaîne est introuvable_

```python
s = "Python Python Python"
print(s.find("Python"))     # 0
print(s.find("Python", 10)) # 14
print(s.find("Java"))       # -1
print(s.index("Java"))      # ValueError
```

## startswith

+ `str.startswith(prefix[, start[, end]])`

```python
s = "Programmer en Python"
print(s.startswith('e'))                                # False
print(s.startswith("Programmer"))                       # True
print(s.startswith("Programmer", 10))                   # False
print(s.startswith(("Coder", "Créer un programme")))    # False
```

## endswith

+ `str.endswith(suffix[, start[, end]])`

```python
s = "Programmer en Python"
print(s.endswith('e'))             # False
print(s.endswith("Python"))        # True
print(s.endswith("Python", 0, 10)) # False
print(s.endswith(("C", "C++")))    # False
```

## isupper

+ `str.isupper()`

```python
s = "EvoluNoob"
print(s.isupper()) # False

s = "EVOLUNOOB"
print(s.isupper()) # True
```

## islower

+ `str.islower()`

```python
s = "EvoluNoob"
print(s.islower()) # False

s = "evolunoob"
print(s.islower()) # True
```

## isalnum

+ `str.isalnum()`

```python
s = "ekJ82kR1pvR3xqU1SZq2Dg8KE2hEb5"
print("".isalnum())  # False (chaîne vide)
print(s.isalnum())   # True

s = "a-a"
print(s.isalnum())   # False
```

## isalpha

+ `str.isalpha()`

```python
s = "EvoluNoob"
print("".isalpha()) # False (chaîne vide)
print(s.isalpha())  # True

s = "Paris 9e"
print(s.isalpha())  # False
```

## isascii

+ `str.isascii()`

```python
s = "EvoluNoob"
print("".isascii())      # True
print(s.isascii())       # True

s = "   T-98p_ ;.]--Mlo"
print(s.isascii())       # True

s = "😏"
print(s.isascii())       # False
```

## isdigit

+ `str.isdigit()`

```python
s = "1234"
print("".isdigit()) # False (chaîne vide)
print(s.isdigit())  # True

s = "3.14"
print(s.isdigit())  # False

s = "⅓"
print(s.isdigit())  # False

s = "²"
print(s.isdigit())  # True

s = "四"
print(s.isdigit())  # False
```

## isnumeric

+ `str.isnumeric()`

```python
s = "1234"
print("".isnumeric()) # False (chaîne vide)
print(s.isnumeric())  # True

s = "3.14"
print(s.isnumeric())  # False

s = "⅓"
print(s.isnumeric())  # True

s = "²"
print(s.isnumeric())  # True

s = "四"
print(s.isnumeric())  # True
```

## isdecimal

+ `str.isdecimal()`

```python
s = "1234"
print("".isdecimal()) # False (chaîne vide)
print(s.isdecimal())  # True

s = "3.14"
print(s.isdecimal())  # False

s = "⅓"
print(s.isdecimal())  # False

s = "²"
print(s.isdecimal())  # True

s = "四"
print(s.isdecimal())  # False
```

## isspace

+ `str.isspace()`

```python
s = "Bonjour à tous"
print("".isspace()) # False
print(s.isspace())  # False

s = "     "
print(s.isspace())  # True
```

## isprintable

+ `str.isprintable()`

```python
s = "Bonjour à tous"
print("".isprintable()) # True
print(s.isprintable())  # True

s = "\n"
print(s.isprintable())  # False
```

## istitle

+ `str.istitle()`

```python
s = "Ha ha ha"
print("".istitle())        # False
print(s.istitle())         # False

s = "Python Python Python"
print(s.istitle())         # True
```

## isidentifier

+ `str.isidentifier()`

```python
s = "channel_name"
print(s.isidentifier()) # True

s = "0name"
print(s.isidentifier()) # False
```

## join

+ `str.join(iterable, /)`

```python
letters = ["P", "y", "t", "h", "o", "n"]
print("".join(letters))  # Python

values = ("145", "36", "8")
print("-".join(values)) # 145-36-8
```

## replace

+ `str.replace(old, new, /, count=-1)`

```python
name = "Programmer en Rust"
print(name) # Programmer en Rust

name = name.replace("Rust", "Python")
print(name) # Programmer en Python
```

## split

+ `str.split(sep=None, maxsplit=-1)`

```python
animals = "castor-dauphin-fourmi-pingouin"
print(animals.split("-")) # ['castor', 'dauphin', 'fourmi', 'pingouin']

name = "Chuck Norris"
print(name.split())       # ['Chuck', 'Norris']
```

## splitlines

+ `str.splitlines(keepends=False)`

```python
text = "Bonjour.\nComment allez-vous ?"
print(text.splitlines())     # ['Bonjour.', 'Comment allez-vous ?']

text = "Bonjour.\nComment allez-vous ?"
print(text.splitlines("\n")) # ['Bonjour.\n', 'Comment allez-vous ?']
```

## encode

+ `str.encode()`

```python
s = "Python"
print(f"Valeur : {s} / Type : {type(s)}") # Valeur : Python / Type : <class 'str'>
s = s.encode()
print(f"Valeur : {s} / Type : {type(s)}") # Valeur : b'Python' / Type : <class 'bytes'>
```

## format

+ `str.format(*args, **kwargs)`

```python
language_name = "Python"
channel_name = "EvoluNoob"
print("Apprenez à programmer en {} sur la chaîne {}".format(language_name, channel_name))

x = 145
y = 63
print("Coordonnées x = {1}, y = {0}".format(y, x))
```

---

🔗 [Toutes les méthodes de la classe str](https://docs.python.org/fr/3.14/library/stdtypes.html#text-sequence-type-str)
