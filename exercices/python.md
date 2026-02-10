# Exercices en Python

> **SOMMAIRE**
> + [EP4 - types de données](#types-de-données---ep4)
> + [EP5 - variables](#variables---ep5)
> + [EP6 - affichage de texte](#affichage-de-texte---ep6)
> + [EP7 - lecture au clavier](#lecture-au-clavier---ep7)
> + [EP8 - opérateurs](#opérateurs---ep8)
> + [EP9 - conditions](#conditions---ep9)
> + [EP10 - boucles](#boucles---ep10)
> + [EP11 - fonctions](#fonctions---ep11)

---

## Types de données - EP4

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep04.md)

1. Choisir un type valide pour manipuler les données suivantes :
    + prénom d'une personne
    + nombre d'articles d'un panier (boutique en ligne)
    + coordonnées d'un point sur un plan en trois dimensions
    + vérifier si l'âge d'une personne est strictement supérieur à zéro
2. Quels sont les types des données suivantes :
    + `"Chuck Norris"`
    + `48.84894381840422`
    + `False`
    + `["épée en fer", "cape d'invisibilité", "potion de soin"]`
    + `{2, 4, 6, 8}`
3. Comment afficher le type de la donnée `{1: "Un", 2: "Deux"}` ?

---

## Variables - EP5

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep05.md)

1. Déclarer autant de variables que nécessaire pour mémoriser les informations suivantes :
   + `Naruto` (le nom d'un ninja devenu célèbre)
   + `20.0` (un taux de TVA, une constante)
   + `True` (pour indiquer qu'un compte est bloqué)
2. Afficher le nom du ninja puis le type de la variable contenant le taux de TVA
3. Le nom du célèbre ninja doit être changé en `Naruto Uzumaki`, comment procéder ?
4. Convertir la variable contenant son nom en une liste

---

## Affichage de texte - EP6

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep06.md)

1. Afficher un texte en respectant son formatage :

```
---------- EvoluNoob ----------
J'apprends à programmer en :
    - Python
-------------------------------
```

2. Afficher un texte en mémorisant des données dans des variables :
    + `Paris` (un nom de ville)
    + `34` (une température en celcius)

```
Aujourd'hui à <nom_de_la_ville> il fait <température> degrés.
```

3. Afficher des animaux par ordre croissant de taille :

```python
a1 = "chat"
a2 = "ours"
a3 = "baleine"
a4 = "fourmi"
a5 = "moineau"

# Afficher sous la forme : fourmi < moineau < chat < ours < baleine
# print()
```

---

## Lecture au clavier - EP7

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep07.md)

1. Demander à l'utilisateur de saisir son prénom, puis l'afficher.
2. Recopier et exécuter un programme, puis expliquer son résultat :

```python
n1 = input("Saisir un premier nombre entier : ")
n2 = input("Saisir un deuxième nombre entier : ")

sum_numbers = n1 + n2
print("La somme de", n1, "+", n2, "est", sum_numbers)
```

---

## Opérateurs - EP8

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep08.md)

1. Convertir une température de Celcius à Fahrenheit :

```python
celcius_temperature = 31
farenheit_temperature =

print(celcius_temperature, "°C =", farenheit_temperature, "°F")
```

2. Calculer le périmètre d'un cercle :

```python
PI = 3.14
radius = 15
circle_perimeter =

print("Périmètre d'un cercle de rayon", radius, ":", circle_perimeter)
```

3. Comparer deux nombres entiers :

```python
n1 = input("Saisir un premier nombre : ")
n2 = input("Saisir un second nombre : ")

result = 

print("n1 < n2 ?", result)
```

---

## Conditions - EP9

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep09.md)

1. Demander à l'utilisateur s'il est abonné à la chaîne EvoluNoob :
    + si l'utilisateur a saisi `oui` ou `o`, le programme affiche `BIEN !`
    + si l'utilisateur a saisi `non` ou `n`, le programme affiche `PAS BIEN !`
    + sinon, le programme affiche `...`
3. Demander à l'utilisateur de saisir un chiffre selon le jour de la semaine (1 = lundi, 7 = dimanche) :
   + afficher le nom du jour correspondant au chiffre saisi
     ex : `Nous sommes mardi`
   + si c'est un jour du week-end (samedi ou dimanche), l'afficher également dans le message
     ex : `Nous sommes samedi, c'est le week-end !`
5. Écrire

---

## Boucles - EP10

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep10.md)

À venir...

---

## Fonctions - EP11

> ➡️ [Voir la correction](https://github.com/jasonchampagne/EvoluNoob/blob/main/exercices/corrections/python/ep11.md)

À venir...
