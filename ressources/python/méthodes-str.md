# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Commencer une chaîne par une majuscule](#strcapitalize)
> + [Mettre une chaîne en majuscule](#strupper)
> + [Mettre une chaîne en minuscule](#strlower)
> + [Mettre une chaîne en minuscule sans distinction de casse](#strcasefold)
> + [Centrer une chaîne dans une autre avec des caractères de remplissage](#strcenter)
> + [Compter le nombre d'occurences d'une chaîne dans une autre](#strcount)

---

> [!NOTE]
> Une chaîne de caractères étant **immuable**, les méthodes s'appliquent sur une copie (qu'elle renvoie éventuellement) de celle-ci.

## str.capitalize()

> _Met le premier caractère (ou première lettre du premier caractère) en majuscule et le reste en minuscule_

```python
s = "chuck"
print(s.capitalize()) # Chuck
```

## str.upper()

```python
s = "EvoluNoob"
print(s.upper()) # EVOLUNOOB
```

## str.lower()

```python
s = "EvoluNoob"
print(s.lower()) # evolunoob
```

## str.casefold()

```python
s = "Ein Großes Haus"
print(s.casefold()) # ein grosses haus
```

## str.center()

```python
s = "Titre du programme"
print(s.center(50))      #                 Titre du programme
print(s.center(50, '-')) # ----------------Titre du programme----------------
```

## str.count()

```python
s = "Apprendre à programmer en Python"
print(s.count(''))         # 33 (longueur de la chaîne)
print(s.count('e'))        # 4
print(s.count('y', 9))     # 1
print(s.count('y', 3, 15)) # 0
```

---

🔗 [Documentation Python](https://docs.python.org/fr/3.14/library/stdtypes.html#text-sequence-type-str)
