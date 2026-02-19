# Méthodes pour les dictionnaires (dict)

> **SOMMAIRE**
> + [Supprimer tous les éléments](#clear)
> + [Copier un dictionnaire](#copy)
> + [Récupérer la valeur d'une clé](#get)
> + [Récupérer une nouvelle vue de tous les éléments](#items)
> + [Récupérer une nouvelle vue de toutes les clés](#keys)
> + [Supprimer un élément et renvoyer sa valeur](#pop)
> + [Supprimer et renvoyer la dernière paire ajoutée](#popitem)
> + [Renvoyer un itérateur inversé sur les clés](#reversed)
> + [Récupérer la valeur d'une clé, sinon ajouter l'élément](#setdefault)
> + [Met à jour un dictionnaire](#update)
> + [Récupérer une nouvelle vue de toutes les valeurs](#values)
> + [Autres méthodes...](#autres-méthodes)

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

## items

+ `dict.items()`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di.items()) # dict_items([('warrior', 'Guerrier'), ('warlock', 'Démoniste')])

for k,v in di.items():
    print(f"{k} -> {v}")
```

## keys

+ `dict.keys()`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di.keys()) # dict_keys(['warrior', 'warlock'])

for k in di.keys():
    print(k)
```

## pop

+ `dict.pop(key)`
+ `dict.pop(key, default)`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di) # {'warrior': 'Guerrier', 'warlock': 'Démoniste'}

try:
    di.pop("warlock")
    di.pop("priest")
except KeyError as key:
    print(f"ERREUR : la clé {key} n'existe pas")
```

## popitem

+ `dict.popitem()`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di) # {'warrior': 'Guerrier', 'warlock': 'Démoniste'}

try:
    removed_pair = di.popitem()
    print(di)
    print(f"Élément retiré -> {removed_pair}")
except KeyError:
    print("Dictionnaire vide")
```

## reversed

+ `reversed(dict)`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")

for key in reversed(di):
    print(key)
```

## setdefault

+ `dict.setdefault(key, default = None)`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di) # {'warrior': 'Guerrier', 'warlock': 'Démoniste'}

print(di.setdefault("warrior")) # Guerrier
print(di.setdefault("priest", "Prêtre")) # Prêtre
print(di) # {'warrior': 'Guerrier', 'warlock': 'Démoniste', 'priest': 'Prêtre'}
```

## update

+ `dict.update(**kwargs)`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di) # {'warrior': 'Guerrier', 'warlock': 'Démoniste'}

di.update(hunter = "Chasseur", warrior = "Combattant")
print(di) # {'warrior': 'Combattant', 'warlock': 'Démoniste', 'hunter': 'Chasseur'}
```

## values

+ `dict.values()`

```python
di = dict(warrior = "Guerrier", warlock = "Démoniste")
print(di.values()) # dict_values(['Guerrier', 'Démoniste'])

for v in di.values():
    print(v)
```

---

## Autres méthodes

> [Documentation Python](https://docs.python.org/fr/3.14/library/stdtypes.html#mapping-types-dict)
