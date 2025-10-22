# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Démarrer une chaîne par une majuscule](#strcapitalize)
> + [Mettre une chaîne en majuscule](#strupper)
> + [Mettre une chaîne en majuscule](#strlower)
> + [Mettre une chaîne en minuscule, sans distinction de casse](#strcasefold)

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

## str.lower()

## str.casefold()

```python
s = "Ein Großes Haus"
print(s.casefold()) # ein grosses haus
```

---

🔗 [Documentation Python](https://docs.python.org/fr/3.14/library/stdtypes.html#text-sequence-type-str)
