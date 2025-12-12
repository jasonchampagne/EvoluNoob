# Méthodes pour les chaînes de caractères (str)

> **SOMMAIRE**
> + [Ajouter un élément à la fin](#append)
> + [Insérer un élément à une position spécifique](#insert)
> + [Ajouter les éléments d'un itérable à la fin d'une liste](#extend)
> + [Supprimer le premier élément ayant la valeur spécifiée](#remove)
> + [Supprimer tous les éléments](#clear)
> + [Autres méthodes...](#dautres-méthodes)

---

## append

+ `list.append(value)`

```python
li = list("EvoluNoo")
li.append("b")
print(li)
```

## insert

+ `list.insert(i, x)`

```python
li = list("Evoluoob")
li.insert(5, "N")
print(li)
```

## extend

+ `list.extend(iterable)`

```python
li = [1, 2, 3]
li.extend([4, 5, 6, 7, 8, 9])
print(li)

li = list("Evolu")
li.extend("Noob")
print(li)
```

## remove

+ `list.remove(x)`

```python
li = [36, -7, 0, 145, 3, 137, -45, 0, 1]
print(li)

li.remove(0) # Supprime le premier zéro de la liste
print(li)
```

## clear

+ `list.clear()`

```python
li = list("Evoluoob")
print(li)

li.clear()
print(li) # Liste vide
```

---

## D'autres méthodes

> [Documentation Python](https://docs.python.org/3/library/stdtypes.html#typesseq-list)
