# Python - corrigé des exercices (EP5)

## Déclarer autant de variables que nécessaire pour mémoriser les informations suivantes

+ `Naruto` (le nom d'un ninja devenu célèbre)
```python
ninja_name = "Naruto"
```

+ `20.0` (un montant de TVA, une constante)
```python
VAT_RATE = 20.0 # par convention, le nom est en majuscule pour indiquer qu'il s'agit d'une constante
```

+ `True` (pour indiquer qu'un compte est bloqué)
```python
account_blocked = True
```

## Afficher le nom du ninja puis le type de la variable contenant le taux de TVA

```python
print(ninja_name)
print(type(VAT_RATE))
```

## Le nom du célèbre ninja doit être changé en Naruto Uzumaki, comment procéder ?

```python
ninja_name = "Naruto Uzumaki"
```

## Transformer la variable contenant son nom en une liste

```python
ninja_name = list(ninja_name)
```
