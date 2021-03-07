---
title: "Bézier Courbe en ReactJs"
date: 2021-03-06T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - untagged
---



Un tracé est d\'abord initialisé par la méthode beginPath(). Le point de
référence de début du tracé est désigné avec moveTo(x,y). Il s\'agit en
quelque sorte de décider à partir de quel emplacement le pinceau va être
posé. Puis vient le tracé de la ligne elle-même avec la
méthode lineTo(x,y) qui va ajouter un segment au chemin qui fut débuté
par beginPath(). On peut ajouter autant de segments que l\'on veut, puis
éventuellement \"fermer\" la forme pour revenir automatiquement au point
de départ avec closePath() .

<https://www.alsacreations.com/tuto/lire/1511-canvas-html5.html>

![](media/image1.png){width="6.21875in" height="4.947916666666667in"}

<https://www.w3schools.com/tags/canvas_beziercurveto.asp>

La liste des evenements écoutés par la fonction 'addEventListener ' :

<https://developer.mozilla.org/fr/docs/Web/Events>

keycode js :

Fleche haut = 38

Fleche bas = 40

Fleche gauche = 37

Fleche droite = 39

Pour avoir tous les keycode = <https://keycode.info/>

[React js :]{.ul}

extension React Devtools : outils qui permet de voir l'arborescence de
react et les statuts de chaque élément
