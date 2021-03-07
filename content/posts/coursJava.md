---
title: "Prise de notes Java"
date: 2019-11-01T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - programming
---


[Vidéos : Encapsulation et abstraction : étude de cas
1](#vidéos-encapsulation-et-abstraction-étude-de-cas)

[Jeu de morpion 1](#jeu-de-morpion)

# Vidéos : Encapsulation et abstraction : étude de cas 

## Jeu de morpion

![](media/image1.png){width="4.510416666666667in"
height="2.3333333333333335in"}Mauvaise grille.

Déclaration de la classe ; déclaration des attributs.

Méthode initialise() pour déclarer le nombre d'éléments au tableau.

2^ème^ méthode getGrille

## Private ou public : 

Private permet d'interdire l'accès d'une autre classe. Permet d'éviter
les modifications malvenues.

De manière générale, lorsqu'un attribut est un objet offrir un accès à
cet attribut via un getter revient exactement au même qu'offrir un accès
direct à l'attribut.

![](media/image2.png){width="4.520833333333333in"
height="2.5416666666666665in"}

![](media/image3.png){width="4.833333333333333in" height="2.5in"}

![](media/image4.png){width="5.666666666666667in"
height="2.9270833333333335in"}

# Classe et Instances, Types et Variables

La classe définit un nouveau type, qui permet de créer 3
variables (instances ou objet).

## Déclaration des attributs 

Simplement mettre le type et le nom de l'attribut.

L'accès aux valeurs des attributs d'une instance de nom *nom_instance*
se fait comme pour accéder aux champs d'une structure :

*nom_instance.nom_attribut*

## Déclaration des méthodes 

Une méthode se déclare avec le *type_retour nom_méthode (type_param1
nom_param1,...){*

*//corps de la méthode}*

Les méthodes sont mises dans la classe elle-même. Il n'y a donc pas de
besoin de réécrire les attributs si ceux-ci sont déjà mentionnés dans la
classe elle-même. Puisque les méthodes ont accès à ses attributs. On
appelle cela une **portée de classe**.

[Il ne faut pas passer les attributs comme arguments aux méthodes de la
classe.]{.ul}

Les méthodes peuvent avoir des paramètres : ceux qui sont nécessaires
(et donc extérieurs à l'instance) pour exécuter la méthode en question.

Dans ce cas la cas, il faut mettre le paramètre extérieur dans la
méthode.

## Appels aux méthodes

![](media/image5.png){width="4.25in" height="2.6458333333333335in"}

## Créer des boucles 

Avec : **while** pour une seule condition *while
(condition){instruction}*

Avec **do...while** : *do{instruction ;}while(condition) ;*

Va exécuter au moins une fois l'instruction.

![](media/image6.png){width="4.708333333333333in"
height="2.8229166666666665in"}

## If... Else 

**If** Spécifie au code d'être exécuté si la condition est vraie.

if (20 \> 18) {

System.out.println(\"20 is greater than 18\");

}

**Else** si la condition est fausse.

if (*condition*) {

*// block of code to be executed if the condition is true*

} else {

*// block of code to be executed if the condition is false*

}

## Les variables 

Il y a trois grands types de variables.

-   Les variables d'instance : ce sont elles qui définissent les
    variables de notre objet.

-   Les variables de classe : elles sont communes à toutes les instances
    de notre classe.

-   Les variables locales : ce sont des variables utiisées pour
    travailler dans l'objet.

## La méthode toString()

# Constructeurs (Introduction)

## Initialisation des attributs

C'est pas sécure de laisser l'utilisateur d'initialiser les attributs.

Une solution est d'offrir une méthode d'initialisation pour initialiser
les attributs.

![](media/image7.png){width="2.9375in" height="1.6979166666666667in"}

C'est ce qu'on appelle un constructeurs.

Un constructeur est une méthode :

-   Invoquée systématiquement lors de la déclaration d'un objet

-   Chargée d'effectuer toutes les opérations requises en début de vie
    de l'objet (dont l'initialisation des attributs)

Ce sont des méthodes comme les autres, seulement elles n'ont pas de
retour (même pas void). Ils ont les mêmes noms que la classe. Et ils
sont invoqués à chaque fois qu'une instance est créée.

Les constructeurs peuvent être surchargés donc avoir plusieurs
paramétres.

## Initialisation par constructeur 

## Constructeur par défaut 

C'est un constructeur sans paramétre. On parle de constructeur par
défaut par défaut. Il va initialiser tous les attributs avec des valeurs
par défaut (0 ; 0.0 ; false ; null).

Le constructeur par défaut disparaît dès qu'au moins un constructeur a
été spécifié.

![](media/image8.png){width="3.6145833333333335in"
height="2.3229166666666665in"}

Trois modèles de constructeurs.

A.  Quand il n'y a pas de constructeur, il y a un constructeur par
    défaut par defaut.

B.  Il y a un constructeur par défaut.

C.  Il y a un constructeur explicite donc il n'y a pas de constructeur
    par défaut par défaut. Donc il faudra initialiser les objets avec
    les paramétres donnés par le constructeur.

## Appel au constructeur

Java autorise les constructeurs d'une classe à appeler n'importe quel
autre constructeur de cette même classe en utilisant **this.** Lorsqu'on
utilise this on ne doit mettre aucun autre instruction avant d'y faire
appel.

On peut aussi attribuer des valeurs aux attributs sans faire appel aux
constructeurs. Ceci se fait au moment de la déclaration des attributs.

![](media/image9.png){width="2.6145833333333335in"
height="1.6458333333333333in"}

Il est préferable d'initialiser les valeurs dans les constructeurs.

## Constructeur de copie

Avec Java il est possible de créer des copies.

![](media/image10.png){width="1.78125in" height="1.1458333333333333in"}

public Rectangle (Rectangle autreRectangle){

hauteur = autreRectangle.hauteur ;

largeur = autreRectangle.largeur ; }

La méthode clône **clone()**

# Fin de vie, affectation, affichage et comparaison d\'objets

Garbage collection (ramasse-miettes) récupère la mémoire occupée par les
objets qui ne sont plus utilisés. Il est lancé automatiquement.

Affecation et copie d'objets

La méthode toString : permet de donner une représentation des valeurs.

## Comparaison d'objets 

L'opérateur == compare les références aux objets. Pour comparer les
objets il faut utiliser .equals()

Il y a la classe **boolean equals()**

# Héritage 

L'héritage permet la relation « est-un ». Cela permet d'éviter la
duplication de méthode.

On parlera de super classe dont les sous-classe vont hérités.

Les sous-classes vont hérités de tous les attributs et toutes les
méthodes sauf les constructeurs.

Enrichissement : des attributs ou des méthodes peuvent être définies
sous C1

Spécialisation : des méthodes héritées de C peuvent être redéfinies sous
C1

## La transitivité de l'héritage 

L'héritage crée un réseau de dépendances entre classes. Qui est organisé
en structure arborescente cela crée une **hiérarchie de classes**.

En pratique :

Un héritage s'obtient avec le mot-clé ***extends NomSuper classe*** puis
en déclarant les attributs et méthodes de la sous-classe

# Héritage : droit d'accès protected

Il y a différents types d'accès : public : accessible à l'intérieur et à
l'extérieur de la classe. Une privé : visible uniquement à l'intérieur
de la classe. Par défaut : visible depuis toutes les classes du même
paquetage.

Le droit d'accès « protected » permet un accès aux attributs de tous les
membres d'une classe de sa descendance. Et du même paquetage.

Le droit d'accès par défaut est un peu plus restrictif car il même
l'accès aux atributs que dans le même packetage.

Pour résumer une sous classe n'a pas accès aux membres privés d'une
classe. Pour y avoir accès elle foit utiliser des getter/setters prévus
dans la super classe.

![](media/image11.png){width="4.166666666666667in" height="2.40625in"}

## Héritage : masquage : 

-   Rédefinition (overriding) : une méthode de la superclasse est
    redéfinit

-   Masquage = pour les variables (shadowing)

On dit que la méthode héritée est la **méthode par défaut**. Et la
méthode redéfinit de la méthode héritée est la **méthode spécialisée**.

Le terme super. Permet d'utiliser la méthode par défaut de la super
classe.

Constructeurs et héritage :

# Polymorphisme 

La résolution statique des liens : le type apparent de la variable qui
est choisit pour déterminer la variable qui va être appliquée. Ce n'est
pas ce qui est choisit par java.

La résolution dynamique des liens : C'est le type effectif donc le type
effectivement stocké à l'intérieur de la variable qui va être
prépondérant : c'est cette résolution qui est effective en Java.

Pour avoir un polymorphisme il faut avoir : de l'héritage et de la
résolution dynamique des liens.

Méthodes abstraites : Elle force les sous-classe à redéfinir la méthode

Elle s'écrit en la déclarant abstract et se finit par : ; Elle doit être
contenue dans une classe abstraite.

On peut utiliser une méthode abstraite.

Les sous-classes d'une classe abstraite restent abstraites tant que
toutes les méthodes abstraite héritées ne sont pas redéfinies.

Toutes les classes qui n'héritent pas d'autres classes, héritent de la
classe Object.

![](media/image12.png){width="5.364583333333333in"
height="3.2708333333333335in"}

![](media/image13.png){width="5.239583333333333in"
height="2.4479166666666665in"}

## Le modificateur final 

Le modificateur final peut s'appliquer à des classes pour dire qu'elles
ne peuvent pas être étendues. A des méthodes pour dire qu'elles ne
peuvent pas être redéfinies et à des variables pour dire qu'elles ne
peuvent pas être modifiées.

Les méthodes finales : doit être introduit par le mot : final
