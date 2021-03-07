---
title: "Questions débutant Java"
date: 2021-03-06T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - untagged
---





# [Quelle est la différence entre : « Double » et « double » pour un attribut ? Quand mettre l'un ou l'autre ?]{.ul}

Le constructeur **Double** permet de définir un objet **Double** à
partir d'une variable **double** :

public Double(double value);

# [Qu'est-ce qu'un constructeur ?]{.ul} 

Pour instancier une classe, c\'est-à-dire créer un objet à partir d\'une
classe, il s\'agit d\'utiliser l\'opérateur *new*.\
En réalité l\'opérateur *new*, lorsqu\'il est utilisé, fait appel à une
méthode spéciale de la classe: le **constructeur**.

Le rôle du constructeur est de déclarer et de permettre d\'initialiser
les données membres de la classe, ainsi que de permettre différentes
actions (définies par le concepteur de la classe) lors de
l\'instanciation.

Un constructeur se définit comme une méthode standard, mais ne renvoie
aucune valeur.\
Ainsi, le constructeur d\'un objet porte le même nom que la classe et ne
possède aucune valeur de retour (même pas *void*).

+----------------------------------+----------------------------------+
| ![https://web.m                  | -   un constructeur porte le     |
| aths.unsw.edu.au/\~lafaye/CCM/im |     > même nom que la classe     |
| ages/warning.gif](media/image1.g |     > dans laquelle il est       |
| if){width="0.4479166666666667in" |     > défini                     |
| height="0.4791666666666667in"}   |                                  |
|                                  | -   un constructeur n\'a pas de  |
|                                  |     > type de retour (même       |
|                                  |     > pas *void*)                |
|                                  |                                  |
|                                  | -   un constructeur peut avoir   |
|                                  |     > des arguments              |
|                                  |                                  |
|                                  | -   la définition d\'un          |
|                                  |     > constructeur n\'est pas    |
|                                  |     > obligatoire lorsqu\'il     |
|                                  |     > n\'est pas nécessaire      |
+----------------------------------+----------------------------------+

La définition de cette fonction membre spéciale n\'est pas obligatoire
(si vous ne souhaitez pas initialiser les données membres par exemple)
dans la mesure où un *constructeur par défaut* (appelé
parfois *constructeur sans argument*) est défini par le compilateur Java
si la classe n\'en possède pas.

Voyons sur un exemple comment se déclare un constructeur :

class Toto{

int age;

char sexe;

float taille;

Toto(int age, char sexe, float taille){

this.age = age;

this.sexe = sexe;

this.taille = taille;

  }

}

# Retour : The method init() in the type Patient is not applicable for the arguments (double, double) ? 

### Comment créer un boucle avec un boolean ? 

## Comment caster un double en int ? 

Il y a une différence entre Double et Integer, il n'y a donc pas de
possibilité de les caster. Il y aurait la méthode IntValue.

## Conversion de type de données (casting)

On appelle *conversion de type de données*,
parfois *transtypage* (traduction de l\'anglais *casting*), le fait de
modifier le type d\'une donnée en une autre.

-   **conversion implicite**: une conversion implicite consiste en une
    > modification du type de donnée effectuée automatiquement par le
    > compilateur. Cela signifie que lorsque l\'on va stocker un type de
    > donnée dans une variable déclarée avec un autre type, le
    > compilateur ne retournera pas d\'erreur mais effectuera une
    > conversion *implicite* de la donnée avant de l\'affecter à la
    > variable. Par exemple la conversion d\'un type primitif vers son
    > Wrapper est implicite.

int n = 8;\
Integer m = n;

-   **conversion explicite**: une conversion explicite (appelée
    > aussi *opération de cast*) consiste en une modification du type de
    > donnée forcée. Cela signifie que l\'on utilise un opérateur
    > dit *de cast* pour spécifier la conversion. L\'opérateur de cast
    > est tout simplement le type de donnée, dans lequel on désire
    > convertir une variable, entre des parenthèses précédant la
    > variable.

double x = 8.324;\
int n = (int) x;

x contiendra après affectation la valeur 8.

(à creuser)

## Quelle est la différence entre Double et double, et Integer et int ? 

Double est un objet alors que double est un type primitif.

La classe Double peut être nulle.

## Comment fermer le scanner ? 

sc.close(); après la méthode où il a été utilisé.

## Comment choisir le type de retour dans une méthode ?

## Comment utiliser un getters ?

Un getter permet de retourner une valeur. Un setter permet de modifier
une valeur.

public class Person {

private String name; // private = restricted access

// Getter

public String getName() {

return name;

}

// Setter

public void setName(String newName) {

this.name = newName;

}

}

## Comment mettre un int en RuntimeException ? 

## Comment s'utilise le this ? 

Par exemple, si dans une méthode, on a un paramètre ayant le même nom
qu\'un attribut de la classe dont la méthode fait partie, on peut
désigner explicitement l\'attribut grâce à *this* :

**public** **class** **Calculateur**

{

**protected** int valeur;

**public** void calcule(int valeur)

{

**this**.valeur = **this**.valeur + valeur;

}

}

Dans le cas de classes imbriquées, c\'est-à-dire qu\'une classe interne
utilise l\'instance de la classe externe, le mot-clé this préfixé du nom
de la classe externe permet de désigner l\'instance de la classe
externe. S\'il n\'est pas préfixé, il désigne l\'instance de la classe
interne.

Exemple :

**public** **class** **Livre**

{

String titre = \"Le livre\";

**class** **Chapitre**

{

String titre = \"Chapitre 1\";

**public** String toString()

{

**return**

Livre.this.titre + *// \"Le livre\"*

\"/\" +

**this**.titre ; *// \"Chapitre 1\"*

*// ou Chapitre.this.titre ; // \"Chapitre 1\"*

}

*// -\> \"Le livre/Chapitre 1\"*

}

}

## Qu'est-ce qu'une classe nested ? 

C'est une classe dans une autre classe. Il suffit de la déclarer. Il
faut peut-être la déclarer static : c'est à vérifier.

## Comment utiliser une classe boolean ? 

Il y a plusieurs utilisations de boolean.

Avec une variable : un objet peut etre boolean.

Boolean peut être un constructeur : ***public Boolean(boolean value)***

La méthode ***booleanValue()*** : retourne la valeur booléenne d'un
objet booléen.

La méthode getBoolean() : renvoie la valeur d'une propriété boolean
**public static boolean getBolean(String name)**

**toString()**

La méthode **toString()** convertit un objet **Character** en un
objet **String**.

public String toString();

Exemple :

Boolean B = new Boolean(false);

String S = B.toString();

La première instruction définit l'objet Boolean **B** et lui affecte la
valeur **false** :

Boolean B = new Boolean(false);

La seconde instruction définit l'objet String **S** et lui affecte la
valeur convertie en String de **B** :

String S = B.toString();

## Pourquoi j'ai ça : « The method main cannot be declared static; static methods can only be declared in a static or top level type " ?

J'avais déclaré une autre classe souris.java par erreur.

## Comment convertir un boolean en toSting() ? 

Il y a deux méthodes ; une première String.valueOf(boolean b) :

Une deuxième Boolean.toString() ;

## Comment faire une ArrayList ? 

Initialisation ArrayList nomArray = new ArrayListe() ;

nomArray.add : permet d'ajouter.

## Pourquoi ma variable string str a un += ? 

## Comment ajouter dans un ArrayList ? 

Il y a deux méthodes une avec un type et l'objet (E e) et une autre avec
le 2 types et2 objets (int index, E element.

## Que veut dire : « l'héritage est transitif » ? 

## Que signifie InstanceOf ?

L\'opérateur *instanceof* s\'applique aux références d\'objets mais ne
sert pas à comparer deux objets entre eux mais simplement à
en **déterminer la classe d\'instanciation ou l\'interface
d\'implémentation**.

## Que mettre en paramètre d\'une méthode java ? 

Il faut y mettre les types avec les attributs qui y seront retournés.

## Vaut-il mieux mettre une méthode getter pour retourner un objet ou l'objet lui-même ? 

## Qu'est-ce qu'une classe abstract ? 

C'est une classe qui ne peut instancier d'objet. Il permet de fournir
des méthodes qui sont vides (abstraite)

## Que veut dire Overide dans Java ? 

## Qu'est-ce qu'une instance courante ? 

C'est l'objet concerné. On peut le désigner avec (this). Il s\'agit de
la référence de l\'objet sur lequel s\'applique la méthode.

## Qu'est-ce qu'une instanceOF ?

C'est un opérateur qui est utilisé pour testé qu'un objet est une
instance d'un certain type. Il fait aussi des comparaison entre le type
d'instance. Il retourne une boolean ou nul si la valeur est nulle.

## Quelle est la différence entre .size() et .length() ? 

ArrayList ne dispose pas de .length. mais a .size() qui permet de
fournir le nombre d'objets dans un collection.

##  
