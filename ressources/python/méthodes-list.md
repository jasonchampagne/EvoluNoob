# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Ajouter un élément à la fin](#append)
> + [Insérer un élément à une position spécifique](#insert)
> + [Ajouter les éléments d'un itérable à la fin d'une liste](#extend)
> + [Supprimer le premier élément ayant la valeur spécifiée](#remove)
> + [Supprimer un élément et le renvoyer](#pop)
> + [Supprimer tous les éléments](#clear)
> + [Autres méthodes...](#dautres-méthodes)

---

## append

+ `list.append(value)`

```python
li = list("EvoluNoo")
li.append("b")
print(li) # ['E', 'v', 'o', 'l', 'u', 'o', 'o', 'b']
```

## insert

+ `list.insert(i, x)`

```python
li = list("Evoluoob")
li.insert(5, "N")
print(li) # ['E', 'v', 'o', 'l', 'u', 'o', 'o', 'b']
```

## extend

+ `list.extend(iterable)`

```python
li = [1, 2, 3]
print(li) # [1, 2, 3]
li.extend([4, 5, 6, 7, 8, 9])
print(li) # [1, 2, 3, 4, 5, 6, 7, 8, 9]

li = list("Evolu")
print(li) # ['E', 'v', 'o', 'l', 'u']
li.extend("Noob")
print(li) # ['E', 'v', 'o', 'l', 'u', 'o', 'o', 'b']
```

## remove

+ `list.remove(x)`

```python
li = [36, -7, 0, 145, 3, 137, -45, 0, 1]
print(li) # [36, -7, 0, 145, 3, 137, -45, 0, 1]

try:
    li.remove(0)
    print(li) # [36, -7, 145, 3, 137, -45, 0, 1]
except ValueError:
    print("Cet élément n'existe pas dans la liste", file = sys.stderr)
```

## pop

+ `list.pop([i])`

```python
li = list("EvoluNoob")

try:
    li.pop()  # Supprime et renvoie le dernier élément
    print(li) # ['E', 'v', 'o', 'l', 'u', 'N', 'o', 'o']

    li.pop(3) # Supprime l'élément à l'indice 3
    print(li) # ['E', 'v', 'o', 'u', 'N', 'o', 'o']
except IndexError:
    print("Indice incorrect ou liste vide", file = sys.stderr)
```

## clear

+ `list.clear()`

```python
li = list("Evoluoob")
print(li) # ['E', 'v', 'o', 'l', 'u', 'o', 'o', 'b']

li.clear()
print(li) # []
```

---

## D'autres méthodes

> [Documentation Python](https://docs.python.org/3/library/stdtypes.html#typesseq-list)
