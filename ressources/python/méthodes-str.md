# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Mettre une chaîne en majuscule](#upper)
> + [Mettre une chaîne en minuscule](#lower)
> + [Mettre une chaîne en minuscule sans distinction de casse](#casefold)
> + [Commencer une chaîne par une majuscule](#capitalize)
> + [Commencer chaque mot d'une chaîne par une majuscule](#title)
> + [Inverser les caractères majuscules et minuscules](#swapcase)
> + [Centrer une chaîne dans une autre avec des caractères de remplissage](#center)
> + [Compter le nombre d'occurences d'une chaîne dans une autre](#count)
> + [Convertir une chaîne en séquence immuable d'octets (_bytes_)](#encode)

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

## encode

+ `str.encode()`

```python
s = "Python"
print(type(s)) # <class 'str'>
s = s.encode()
print(type(s)) # <class 'bytes'>
```

---

🔗 [Toutes les méthodes de la classe str](https://docs.python.org/fr/3.14/library/stdtypes.html#text-sequence-type-str)
