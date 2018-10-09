+++
title = "Machine Learning : concepte de base"
description = "Etude de differents types d'apprentissage/de classification"
date = 2018-09-04
tags = ["SIBA,ML,Machine Learning, Weka"]
author = "Damien Narbais"
+++

# Machine Learning

## * Les valeurs

Tout d'abord, on peut retrouver deux types de **valeur** :
- les **continues** : numériques (13,-71...)
- les **discrètes** : nominales (ensoleillé,gris...)

## * Différents conceptes

- **la classification** *(supervisée)* qui consiste à classifier des nouvelles données, en ayant auparavant, eu des exemples.
- **la prediction numérique** *(supervisée)* qui prédit un nombre selon les attributs de la nouvelle données
- **le regroupement** *(non supervisé)* qui classe les données en différentes catégories
- **selection/transformation d'attribut** *( (non) supervisé)*
- **association** *(supervisé)* ici, le système apprend les relations entre les attributs

## * Les types de classification

Il en existe beaucoup, et je vais d'abord vous parler des plus basiques.   
*parfois les plus basiques sont les meilleurs ...*

### Zero-Rule / 0-R / A priori :
C'est le plus simple. Il regarde seulement le résultat final qu'il y a dans les données, et non leurs attributs.  
Par exemple, s'il y a 20 cas "oui" et 10 cas "non", l'algoritme dira toujours "oui". Ici le taux de réussitte est de 66%.  

Il permet d'avoir une base sur le pourcentage d'erreur que l'on peut obtenir avec du machine learning.

### 1-R :
Il choisit le meilleur attribut, i.e. celui qui fait le moins d'erreurs.  
S'il il manque une donnée, il la remplace par "missing".  

Si il s'agit de données numériques :   
1- il commence par trié les données dans l'ordre croissant    

| 64  | 65  | 68  | 69  | 70  | 72  | 75  | 75  | 80  |81   | 83  | 92  |
|:-:|:-:|:-:|---|---|---|---|---|---|---|---|---|
| oui  |  non | oui  |  oui | oui  | non  | non  | oui  | oui  | oui  | non  | oui  |





### Naïve Bayes :

### Les arbres :
