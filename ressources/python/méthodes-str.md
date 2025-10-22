# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Commencer une chaîne par une majuscule](#capitalize)
> + [Mettre une chaîne en majuscule](#upper)
> + [Mettre une chaîne en minuscule](#lower)
> + [Mettre une chaîne en minuscule sans distinction de casse](#casefold)
> + [Centrer une chaîne dans une autre avec des caractères de remplissage](#center)
> + [Compter le nombre d'occurences d'une chaîne dans une autre](#count)

---

> [!NOTE]
> Une chaîne de caractères étant **immuable**, les méthodes s'appliquent sur une copie (qu'elle renvoie éventuellement) de celle-ci.

## capitalize

> _Met le premier caractère (ou première lettre du premier caractère) en majuscule et le reste en minuscule_

```python
s = "chuck"
print(s.capitalize()) # Chuck
```

## upper

```python
s = "EvoluNoob"
print(s.upper()) # EVOLUNOOB
```

## lower

```python
s = "EvoluNoob"
print(s.lower()) # evolunoob
```

## casefold

```python
s = "Ein Großes Haus"
print(s.casefold()) # ein grosses haus
```

## center

```python
s = "Titre du programme"
print(s.center(50))      #                 Titre du programme
print(s.center(50, '-')) # ----------------Titre du programme----------------
```

## count

```python
s = "Apprendre à programmer en Python"
print(s.count(''))         # 33 (longueur de la chaîne)
print(s.count('e'))        # 4
print(s.count('y', 9))     # 1
print(s.count('y', 3, 15)) # 0
```

---

🔗 [Documentation Python](https://docs.python.org/fr/3.14/library/stdtypes.html#text-sequence-type-str)
