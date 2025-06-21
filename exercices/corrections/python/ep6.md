# Python - corrigé des exercices (EP6)

## Afficher un texte en respectant son formatage

```python
print("---------- EvoluNoob ----------")
print("J'apprends à programmer en :")
print("\t- Python")
print("-------------------------------")
```

## Afficher un texte en mémorisant des données dans des variables

```python
city_name = "Paris"
temperature = 34

print("Aujourd'hui à", city_name, "il fait", temperature, "degrés.")
```

## Afficher des animaux par ordre croissant de taille

```python
a1 = "chat"
a2 = "ours"
a3 = "baleine"
a4 = "fourmi"
a5 = "moineau"

# Afficher sous la forme : fourmi < moineau < chat ...
print(a4, a5, a1, a2, a3, sep = ' < ')
```
