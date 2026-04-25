# Méthodes pour les ensembles (set, frozenset)

> **SOMMAIRE**
> + [Copier (superficiellement) un ensemble](#copy)
> + [Ajouter un élément à un ensemble](#add)
> + [Supprimer un élément d'un ensemble](#remove)
> + [Supprimer un élément d'un ensemble, s'il existe](#discard)
> + [Supprimer un élément (arbitraire) et le renvoyer](#pop)
> + [Supprimer tous les éléments d'un ensemble](#clear)
> + [Récupérer les éléments communs à un ensemble et aux autres](#intersection)
> + [Récupérer les éléments d'un ensemble et des autres](#union)
> + [Récupérer les éléments d'un ensemble qui ne sont dans aucun des autres](#difference)
> + [Récupérer les éléments d'un ensemble, ou d'un autre, mais pas des deux](#symmetric_difference)
> + [Vérifier si un ensemble n'a aucun élément en commun avec un autre](#isdisjoint)
> + [Vérifier si tous les éléments d'un ensemble sont dans un autre](#issubset)
> + [Vérifier si tous les éléments d'un autre ensemble sont dans un premier ensemble](#issuperset)
> + [Mettre à jour un ensemble en ne gardant que les éléments trouvés dans d'autres](#intersection_update)
> + [Mettre à jour un ensemble en ajoutant les éléments des autres](#update)
> + [Mettre à jour un ensemble en retirant les éléments trouvés dans d'autres](#difference_update)
> + [Mettre à jour un ensemble en ne gardant que les éléments trouvés dans un des deux, mais pas dans les deux](#symmetric_difference_update)
> + [Autres méthodes...](#autres-méthodes)

---

## copy

+ `set.copy()`
+ `frozenset.copy()`

```python
sA = set("abcdef")
sB = sA.copy()

print(sA) # {'f', 'c', 'a', 'b', 'd', 'e'}
print(sB) # {'f', 'c', 'a', 'b', 'e', 'd'}

sB.add("g")

print(sA) # {'f', 'c', 'a', 'b', 'd', 'e'}
print(sB) # {'f', 'c', 'a', 'g', 'b', 'e', 'd'}
```

## add

+ `set.add(elem)`

```python
se = set("abc")

print(se) # {'c', 'a', 'b'}
se.add("d")
print(se) # {'b', 'd', 'c', 'a'}
```

## remove

+ `set.remove(elem)`

```python
se = set("abc")

print(se) # {'c', 'a', 'b'}

try:
    se.remove("b")
    se.remove("d")
except KeyError:
    print("Élément non trouvé.", file = sys.stderr)

print(se) # {'c', 'a'}
```

## discard

+ `set.discard(elem)`

```python
se = set("abc")

print(se) # {'a', 'c', 'b'}

se.discard("b")
se.discard("a")

print(se) # {'c'}
```

## pop

+ `set.pop()`

```python
se = set("ab")

print(se) # {'a', 'b'}

try:
    element = se.pop()
    se.pop()
    se.pop()
except KeyError:
    print("Rien à supprimer, l'ensemble est vide.", file = sys.stderr)

print(se) # {}
print(element) # a (mais ça aurait pu être « b »)
```

## clear

+ `set.clear()`

```python
se = set("abc")

print(se) # {'c', 'a', 'b'}
se.clear()
print(se) # {}
```

## intersection

+ `set.intersection(*others)`
+ `frozenset.intersection(*others)`

```python
sA = set("abc")
sB = set("def")
sC = set("arbre")

print(sA.intersection(sB)) # {}
print(sA.intersection(sC)) # {'b', 'a'}
```

## union

+ `set.union(*others)`
+ `frozenset.union(*others)`

```python
sA = set("abc")
sB = set("def")

print(sA.union(sB)) # {'b', 'e', 'f', 'd', 'c', 'a'}
```

## difference

+ `set.difference(*others)`
+ `frozenset.difference(*others)`

```python
sA = set("abc")
sB = set("def")
sC = set("arbre")

print(sA.difference(sB)) # {'b', 'a', 'c'}
print(sA.difference(sC)) # {'c'}
```

## symmetric_difference

+ `set.symmetric_difference(*others)`
+ `frozenset.symmetric_difference(*others)`

```python
sA = set("abc")
sB = set("def")
sC = set("arbre")

print(sA.symmetric_difference(sB)) # {'b', 'd', 'c', 'a', 'f', 'e'}
print(sA.symmetric_difference(sC)) # {'r', 'c', 'e'}
```

## isdisjoint

+ `set.isdisjoint(other)`
+ `frozenset.isdisjoint(other)`

```python
sA = set("EvoluNoob")
sB = set("FormationVidéo")
sC = set("DtktMjja")

# Est-ce que l'intersection des deux ensembles est un ensemble vide {} ?
print(sA.isdisjoint(sB)) # False
print(sA.isdisjoint(sC)) # True
```

## issubset

+ `set.issubset(other)`
+ `frozenset.issubset(other)`

```python
sA = set("EvoluNoob")
sB = set("FormationVidéo")
sC = set("Noob")

# Est-ce que le premier est un sous-ensemble du second ?
print(sA.issubset(sB)) # False
print(sC.issubset(sA)) # True
```

## issuperset

+ `set.issuperset(other)`
+ `frozenset.issuperset(other)`

```python
sA = set("EvoluNoob")
sB = set("FormationVidéo")
sC = set("Noob")

# Est-ce que le premier est un sur-ensemble du second ?
print(sA.issuperset(sB)) # False
print(sC.issuperset(sA)) # False
```

## intersection_update

+ `set.intersection_update(*others)`

```python
sA = set("abc")
sB = set("def")

print(sA) # {'c', 'b', 'a'}

# Mise à jour de sA, en ne gardant que les éléments trouvés dans sB
sA.intersection_update(sB)

print(sA) # {}
```

## update

+ `set.update(*others)`

```python
sA = set("abc")
sB = set("def")

print(sA) # {'c', 'b', 'a'}

# Mise à jour de sA, en ajoutant les éléments de sB
sA.update(sB)

print(sA) # {'d', 'c', 'b', 'a', 'f', 'e'}
```

## difference_update

+ `set.difference_update(*others)`

```python
sA = set("abc")
sB = set("def")

print(sA) # {'c', 'a', 'b'}

# Mise à jour de sA, en retirant les éléments trouvés dans sB
sA.difference_update(sB)

print(sA) # {'c', 'a', 'b'}
```

## symmetric_difference_update

+ `set.symmetric_difference_update(*others)`

```python
sA = set("abc")
sB = set("def")

print(sA) # {'c', 'b', 'a'}

# Mise à jour de sA, en ne gardant que les éléments trouvés dans sA ou sB, mais pas les deux
sA.symmetric_difference_update(sB)

print(sA) # {'f', 'a', 'c', 'b', 'd', 'e'}
```

---

## Autres méthodes

> [Documentation Python](https://docs.python.org/3/library/stdtypes.html#types-set)
