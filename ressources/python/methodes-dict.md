# Méthodes pour les dictionnaires (dict)

> **SOMMAIRE**
> + [Copier un dictionnaire](#copy)
> + [Récupérer la valeur d'une clé](#get)
> + [Supprimer tous les éléments](#clear)

---

## clear

+ `dict.clear()`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di) # {'warrior': 'Guerrier', 'warlock': 'Démoniste'}

di.clear()
print(di) # {}
```

## copy

+ `dict.copy()`

```python
d1 = {1: [10, 20, 30]}
d2 = d1.copy() # copie (superficielle)

print(d1) # {1: [10, 20, 30]}
print(d2) # {1: [10, 20, 30]}

d1[1].append(35)

print(d1) # {1: [10, 20, 30, 35]}
print(d2) # {1: [10, 20, 30, 35]}
```

## get

+ `dict.get(key, default = None)`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")

val1 = di.get("warrior")
print(val1)

val2 = di.get("priest", "Pas de valeur trouvée...")
print(val2)
```
