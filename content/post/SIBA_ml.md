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

**[A TERMINER]**



### Naïve Bayes :

On va utiliser tous les attributs.
Pour cela, on suppose ici que tous les attributs sont indépendants.
**[FORMULE]**  
Ensuite à l'aide de formule de probabilité, dont le likelihood, on détermine le résultat que l'on devrai obtenir.

S'il manque un attribut, ce n'est pas important car on le prendra pas en compte dans la formule, ce qui ne change rien.   
Par contre, si un attribut a une valeur de 0, cela pose un problème car dans nos calculs, on va retrouver un 0.   
Pour remedier à cela, on ajoute +1 à tous les attributs (technique appelé estimateur de Laplace). Ou simplement, on exige d'avoir un exemple pour chaque cas.

Quand les données sont numériques, on utilise une gaussienne, qui nous permet de calculer ce fameux likelihood.

En général, il faut auparavant, bien filtrer les attributs.

### Les arbres :

Les arbres essayent de reproduire le chemin général que prennent les données, en commençant par les attributs qui sont les plus révélateurs.   
Pour cela, on a besoin de 5 calculs, pour chaque attribut. Ainsi, on détermine lequel a le plus d'impact, et le plus susceptible de déterminer la classe du nouvel objet.

1. Le Gain  **[FORMULE]**. Plus il est grand mieux c'est.
2. L'info[], qui se calcul grâce à l'entropie. **[FORMULE]** Le plus proche de 0 possible.
3.  Le split info **[FORMULE]**
4. Gain ratio **[FORMULE]**. On prend le plus haut taux.

*Remarque : si le gain est important, alors l'info sera petit*

### Regression linéale :

On essaie de minimiser l'erreur quadratique. (On peut utiliser des matrices).   
On peut aussi utiliser le processus de Stocastic gradient decent.


### Classification linéale :

Se base sur la regression linéale
