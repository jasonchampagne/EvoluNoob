# Python - corrigé des exercices (EP7)

## Demander à l'utilisateur de saisir son prénom, puis l'afficher

```python
firstname = input("Comment t'appelles-tu ? ")
print("Ton prénom est", firstname)
```

## Recopiez et exécutez un programme puis expliquez son résultat

+ Le programme n'a pas fait la somme des deux nombres parce que la fonction `input()` convertit les données lues en chaînes de caractères (type `str`).
+ On peut d'ailleurs vérifier ces derniers avec ce code :

```python
print(type(n1)) # type "str"
print(type(n2)) # type "str"
```
