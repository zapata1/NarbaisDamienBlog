+++
title = "Faire et heberger un site web gratuit avec hugo et git"
description = "Créer un site web en quelques étapes"
date = 2018-03-20T02:13:50Z
author = "Damien Narbais"
+++

# Introduction

Bonjour à toutes et à tous !

Dans cet article, nous allons voir comment créer son site web en seulement 10 étapes. C’est accessible à tout le monde (que vous ayez déjà fait ou non de l’informatique). Cela dure environ 1h00 et vous pouvez le faire en plusieurs fois donc : lancez-vous !

# Etape 0 : Les outils utilisés
Avant de débuter, je voulais vous présenter rapidement les outils que nous allons utiliser. Il s’agit de Github et Hugo.  

Github est un site de partage de code. C’est une sorte de google doc/drive mais pour le code. On va s’en servir pour mettre notre code dessus et héberger notre site.
Je vous préviens de suite : l’hébergement du site web est gratuit, par contre, vous ne pourrez pas lui donner l’url que vous voulez (www.monBlog.com). Et oui, en contre partie, vous aurez une adresse de la forme :    
https://zapata1.github.io/NarbaisDamienBlog/ ou https://zapata1.github.io/NarbaisDamienBlog/

Hugo est la structure de notre site web que nous allons utiliser. Nous avons choisi celui la car le principe d’utilisation est simple (nous allons voir ça dans l’étape XX) et qu’il existe déjà beaucoup de thèmes déjà fait qui pourront correspondre (au moins en partie) à ce que vous voulez obtenir comme site web.

Il vous faudra un environnement Linux. Pour windows, soyez patient, ça arrive bientot.


# Etape 1 : GitHub : Inscription
Tout d’abord, il vous faudra un compte github (https://github.com/).  
Dans notre cas, nous en avons un qui s’appelle beParrots.


TODO
# Etape 2 : Hugo : Installation de l’environnement
Vous allez maintenant devoir faire quelque commande pour installer l’environnement de travaille.
TODO

# Etape 3 : Hugo : Principe
Bon, maintenant que tout est en place, c’est bien beau mais qu’est ce que c’est Hugo ? Si vous le savez déjà, vous pouvez passer à l’étape suivante. Sinon, il est nécessaire de comprendre comment est organisé notre site.   
Hugo est un framework qui va gérer la structure de notre site web.  
Il va le décomposer en 6 dossiers, qui ont chacun une  :   https://gohugo.io/getting-started/directory-structure/
- archétypes
  - permet de créer la structure de nos fichiers (nous verrons cela plus en détail dans la partie XX).  
Par exemple, on aura un archétype tutoriel, un autre blog et un autre article.
- content
    - contient tous les fichiers textes que nous allons créer.  
Dans l’exemple précédent, on aura 3 sous dossiers : 1 qui contiendra les tutoriels, un autre les blogs, et le dernier les articles.
- layout
    - contient les fichiers qui permettent l’affichage.  
Par exemple, on aura un fichier pour l'entête de la page, un autre pour afficher les tutoriels, un autre pour les articles...
- thème
    - Ou se trouvera la base de notre thème
- static
    - Qui stocke tout ce qui est statique : les images, les fichiers CSS (fichiers qui permettent de définir le design, les couleurs.. de votre site), les fichiers JS (qui permettent de faire un peu d’animation comme : surligner un titre quand on passe la souris dessus…)

# Etape 4 : Hugo : Choisir un thème
Maintenant que vous avez pris connaissance des bases de hugo, il va falloir choisir un thème pour commencer à écrire nos articles comme on le souhaite.  

Vous vous dites peut être : “Quoi ? Mais je voulais faire mon site comme je veux !”. Pas de panique, choisir un thème ne veut pas dire que vous ne pourrez pas le modifier. Cependant, je vous conseille de partir d’un thème qui vous plaît. On verra par la suite comment le personnaliser.  

Libre à vous de choisir ce qui vous correspond en allant ici :   https://themes.gohugo.io/.  
L’avantage c’est que l’on peut tester la plupart des thèmes avant de les choisir. Il suffit de cliquer sur l’image d’un thème, puis de cliquer sur ‘Demo’.  

Dans notre exemple, nous allons utiliser le thème : Min_night   (https://themes.gohugo.io/min_night/).

# Etape 5 : Hugo : Mise en marche en local

Ce thème est bien car la documentation est assez bien faite.  
Il vous faut donc suivre les étapes pour avoir une mise en production locale.  


Aller dans le répertoire que vous voulez. Ouvrez un terminal et tapez les commandes suivantes :

`hugo new site monSite`    
`cd monSite`  
`git init`  
`git submodule add https://github.com/nathancday/min_night.git themes/min_night`  
`cp -r themes/min_night/exampleSite/* .`  ATTENTION il manque l'étoile (\*) dans la  
documentation et sans elle vous ne verrez rien

On va, ici, faire fonctionner notre site web mais en local. C’est à dire que vous seul, sur votre ordinateur, pourra le voir.

`hugo server -D`  
Allez à l’adresse : http://localhost:1313/.  

Si vous visualisez le thème que vous avez choisi c’est bon parfait. Dans le cas contraire,, n’hésitez pas à nous mettre en commentaire votre problème. Nous pouvons vous aider.  

# Etape 6 : Github : création du dépot Git
Maintenant que votre site marche en local, ça veut dire que nous allons pouvoir le faire marcher sur internet, enfin !

Si le titre vous fais peur, n’ayez crainte ! On va simplement mettre tous nos fichiers sur Git (la sorte de google doc/drive mais pour le code).

Pour cela il faut ...

# Etape 7 : Github : Activer le serveur

Faire la génération du ‘docs’  
choisir dans les parametres le docs  
choisir un nom de domaine  
Tester  

# Etape 8 : Hugo : Votre site
Il ne reste plus qu’a écrire vos articles dans la section aproprié./ modifer le theme/ le changer ...
Puis pusher tout ça sur Git
Le serveur est mis a jour
