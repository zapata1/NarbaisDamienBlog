+++
title = "TP - Créer et gérer des machines virtuelles, Linux (VM)"
description = "Compétition de Robotique"
date = 2018-10-3
tags = ["CDPS,VM,Linux"]
author = "Damien Narbais"
+++

## Objectif du TP

Prise en main, compréhension et comparaison de différents types de machines virtuelles.
- Connaitre les principes de base de la virtualisation Linux, avec KVM et LXC
- Gerer des machines virtuelles en utilisant une interface graphique et la ligne de commande


## 1 - Gestion de VM KVM avec une interface graphique

On a commencé par créer des VM au format *raw*.  

On a ensuite utilise le format *QCOW2*.
Ce format est tres pratique car a partir d'une image "mere" (>2Go), on peut creer des VM images beaucoup plus légères (-[400Mo ; 800M0]). Ce qui est tres pratique quand on a beaucoup de VM.

## 2 - Gestion de VM KVM avec l'interface libvirt + Fichier *xml*

Tout d'abord, pour la virtualisation KVM, on a utilisé l'interface libvirt. Nous avons créé une VM à partir d'une image au format *qcow2*.   
Ensuite, pour créer la deuxième machine virtuelle avec virsh, nous avons eu besoin de 2 éléments :
- une nouvelle image,
- un fichier de configuration *xml*

### Le fichier *xml*

Pour avoir la structure du format *xml*, nous avons extrait le fichier *xml* de la première machine virtuelle. Nous avons modifié certains paramètres (nom de la machine, nom de l'image utilisée, l'identifiant unique uuid et l'identifiant MAC).

&nbsp;&nbsp;&nbsp;&nbsp; On va maintenant présenter et analyser la structure du fichier *xml*.  
Ce fichier a une hiérarchie. Dans la balise de *domaine*, il y en a d'autres dont le *name*, *uuid*, *memory*, *vcpu*, *os*...    
Certaines balises en contiennent d'autres. Chacune d'elle contient des éléments spcécifique (voir tableau).




| Nom de la balise  | Signification  | Exemple : Contenu pour notre TP |
|:-:|:-:|:-:|
| name  |   |   |
| uuid  |   |   |
| memory  |   |   |
| currentMemory  |   |   |
| vcpu  |   |   |
| ressource  |   |   |
| os  |   |   |
| festures  |   |   |
| cpu  |   |   |
| devices  |   |   |
*Toutes les balises non pas été expliquées dans ce tableau*
