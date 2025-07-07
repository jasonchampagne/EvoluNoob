# Python - corrigé des exercices (EP8)

## Convertir une température de Celcius à Fahrenheit

```python
celcius_temperature = 31
farenheit_temperature = celcius_temperature * 9 / 5 + 32

print(celcius_temperature, "°C =", farenheit_temperature, "°F")
```

## Calculer le périmètre d'un cercle

```python
PI = 3.14
radius = 15
circle_perimeter = 2 * PI * radius

print("Périmètre d'un cercle de rayon", radius, ":", circle_perimeter)
```

## Comparer deux nombres entiers

```python
n1 = input("Saisir un premier nombre : ")
n2 = input("Saisir un second nombre : ")

result = int(n1) < int(n2)

print("n1 < n2 ?", result)
```
