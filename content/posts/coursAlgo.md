---
title: "Algorithmie cours"
date: 2019-11-01T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - untagged
---

Quatre algorithme étudié :

L'invariant de boucle : Invariant qui est vraie avant et après chaque
répétition.

Définition de la notation *Θ* (grand thêta) : étant donnée une
fonction *f(n)*, *Θ(f(n))* est l\'ensemble des fonctions *g(n)* telles
qu\'il existe une constante positive réelle *c*, une constante positive
réelle *d*, et un entier non négatif *N* tel que pour tout *n\>N*, *c×
f(n) ≤ g(n) ≤ d × f(n)*.

En d\'autres mots : *Θ(f(n))=Ω(f(n))∩O(f(n))*

Procdure Recherche- Linéaire

*Procédure* R ECHERC HE- LI NÉAIRE *( A , n, X)*

*Entrées:*

• *A* : un tableau.

• *n* : le nombre d \'éléments de *A* à examine r.

• *x* : la valeur recherchée.

*Sortie :* Soit l\'indice *i* pour lequel *A\[i\]* = *x,* soit l a
valeur s péciale

NoN-TRouvÉ, qui peut correspondre à n\'importe quel indice invalide

pour Je tableau, comme 0 ou un entier négatif.


1\. Fixer *réponse* à NoN-TRouvÉ.

2\. Pour chaque indice *i,* en allant de 1 à *n,* dan s l\'ordre:

A. Si *A\[i\]* = *x,* alors fixer *réponse* à la valeur de *i.*

3\. Retourne r la valeur de *réponse* en tant que sortie.

Meilleur- Recherche- Linéaire

*Procédure* MEILLEURE-RECHERCHE-LIN ÉA IR E(A , n, x)

*En trées et sortie:* identiques à celles de R EC HERCHE- LI NÉA IR E .

1\. Pour *i* = l à *n* :

A. Si A\[i\] = *x,* alor s retourner l a valeur de *i* comme sortie.

2\. Retourner NoN-TRouvÉ comme sortie.

Recherche --Linéaire --Sentinelle

*Procédure* RECHERCHE-LINÉAIRE -SENTIN ELL E( *A , n , X)*

*Entrées et sortie:* identiques à celles de RECH ERCHE- LI NÉA IR E.

1\. S auvegarde r *A\[n\]* dans *dernier* et p l acer *x* dans *A\[n\].*

2\. Fixe r *i* à 1.

3\. Tant que *A\[i\] \* x,* faire l a chose suivante :

A . Incré menter *i.*

4\. Restaurer *A\[n\]* à partir de *dernier.*

5\. Si *i* \< *n* ou *A\[n\]* = *x,* alors retourner la valeur de *i*
comme sortie.

6\. Sinon retourner NoN-TRouvÉ comme sortie.

Recherche dichotomique ou recherche binaire a pour avantage un temps
d'exécution O(lg n). Ce temps est dû aux multiples séparations en 2.
Illustration : On recherche le livre (lié à une alvéole) par la clé de
tri( nom de l'auteur) qui commence par S. Nous allons à la moitié de la
bibliothèque et identifions la clé de tri. Si c'est L, toutes la partie
à gauche est donc éliminé. La partie de droite de (la moitié à n) est
maintenant le terrain d'analyse. Nous nous postionnons à la moitié,
selon la clé de tri nous pourrons : ou tomber sur l'objet recherché, ou
éliminer à nouveau une moitié.

*Procédure* R ECHERCH E- DICHOTOMIQU E *(A, n, x)*

*Entrées et sortie:* Identiques à R ECHERCH E- LI NÉA IR E.

l\. Fixer *p* à **l** et *r* à *n.*

2\. Ta nt que *p* \~ *r,* faire la chose s uivante :

A. Fixe r *q* à L(p + *r)* / 2J.

B . Si *A\[q\]* = *x,* alors retourner *q.*

C. Sinon *(A\[q\] \* x)* si *A\[q\]* \> *x,* alors fixer *r* à *q* - 1.

D. Sinon *( A\[q\]* \< *x)* fixer *p* à *q* + 1.

3\. Retourner NoN-ThouvÉ.

Les tri de recherche : tri par sélection, tri par insertion, tri par
fusion, tri rapide.

8 (n2 ) : moins avantageux

ou *8(nlgn) : plus rapide.*

Clé de tri :

Données satellites : information associée à la clé de tri et qui doivent
être transportés avec la clef lorsqu'elle est déplacée.

Recherche dichotomique récursive (page 43)

![](media/image1.png){width="6.270833333333333in"
height="3.0416666666666665in"}

pour que lle v aleur d e *x,*

*2x* atteint-il *n* ? Si *n* est une puissance exacte de 2, n ous avons
v u à la

page 7 que la réponse es t lg *n.*

La rapidité de O (lgn) est due au fait que chaque itération n'a pas son
temps impacté par n. Elle ne dépend pas du tableau examiné.

Asymptote : qui tend vers l'infini.

Tri par sélection

*Procédure* TR1- S ÉLECTION ( A , *n)*

*Entrées:*

• *A* : un tableau.

• *n* : le nombre d \'élé me nts du tableau *A* à trier.

**Tri pa r sé lection**

*R ésultat :* L es éléments de *A* s ont triés par ordre crois sant.

1\. Pour *i* = 1 à *n* - **1** :

A. Fixer *minimum* à l\'indice du plus petit é l é ment du sous-tableau

*A\[i .. n\].*

B. Échanger *A\[i\]* et *A\[minimum\].*

Pour trouver le plus petit élément :

*Procédure* TR1- S ÉLECTION(A, *n)*

*Entrées et résultat:* identiques aux précédents .

1\. Pour *i* = 1 à *n* - 1 :

A. Fixer *minimum* à 1.

B. Pour *j* = *i* + l à n:

i\. Si *A\[j\]* \< *A\[ minimum\],* alors fixer *minimum* à *j.*

C. Échanger *A\[i\]* et *A\[minimum\]*

La justification pour dire que le tri de recherche est *Θ(n2)* est selon
la propriété : *k* + (k - 1) + (k - 2) + \... + 2 + 1 = *k(k* + l)/2 qui
vient rejoindre le chemin de notre boucle d'itérations :

(n-1)+(n-2)+(n-3)...3+2+1

En remplaçant *k* par *n* - 1, nous voyons que le nombre total d \'
itérations

de l a boucle interne est égal à *(n* - l )n / 2 , c\'est-à-dire *(n 2*
- *n)* / 2.

S ervons-nous d e la notation asymptotique pour retirer le terme
d\'ordre

inférie ur *( - n)* et le facteur constant (1 / 2). Nous pouvons a lors
dire que le

nombre total d\'itérations de la boucle interne est 0(n2 ). Le temps
d\'exécution

d e TRI -SÉLECTION est par conséquent 0(n2 ). Notez qu\'i l s\'ag it d
\' une

déclaration générale qui couvre tou s les cas. Que ll es que soient les
valeurs

réelles des éléments, la boucle interne s\'exécute à 0(n2 ) re prises.

On dit alors que le tri de recherche est asymptotique *Θ(n2)* .

Le tri par insertion :

*Procédure* TRI -INSERTION *(A,n)*

*Entrées et résultat :* Identiques à ceux de TRI-SÉLECTION.

1\. Pour *i* = 2 à *n* :

A. Fixer *clé* à *A\[i\]* etj à *i* - 1.

Tri par insertion

B. Tant que *j* \> 0 et *A\[j\]* \> *clé ,* faire la chose suivante:

i\. Fixer *A\[j* + 1\] à *A \[ j \].*

ii\. Décré menter *j* (c\'est-à-dire fixe r *j* à *j* - 1).

C. Fixer *A\[j* + 1\] à *clé.*

.

Tri par fusion :

Il affiche un temps de seulement = *0(grand thêta) (n lgn)*

Le tri par fusion a toutefois deux inconvénients par rapport aux deux

autres algorithmes de tri étudiés. Premièrement, le facteur constant
masqué

par la notation asymptotique est plus élevé que celui des deux premiers
algorithmes.

Toutefois, dès que le tableau est suffisamment grand, cela n\'a pas

vraiment d\'importance. Deuxièmement, le tri par fusion ne travaille pas
sur

le tableau d\'origine : il doit réaliser des copies de l\'intégralité du
tableau d \'entrée.

Cette copie de toutes les entrées est à comparer à l a copie d\' une
seule

entrée du tableau dans les tri s par sélection et par insertion. Si la
quantité de

mémoire utilisée est une contrainte, le tri par fusion pourrait ne pas
convenir.

Le tri rapide :

![](media/image2.png){width="4.479166666666667in"
height="1.4479166666666667in"}

![](media/image3.png){width="3.7916666666666665in"
height="2.8333333333333335in"}

Le tri rapide repose sur le partitionnement. Il faut définir un pivot.
Dans le schéma c'est q. A partir de ce q, plusieurs groupes vont être
constitués. Un groupe des élements avant le q, un groupe d'après et un
groupe indéfini. Les groupes d'avant et après seront triés de fait.
Récursivement, chaque élement du groupe indéfini sera positionné le plus
à droite des groupes car les autres groupes étaient déjà triés (p.53)

![](media/image4.png){width="5.25in" height="2.0416666666666665in"}

![](media/image5.png){width="5.333333333333333in"
height="1.8958333333333333in"}

No us ne sommes pas e n m esure d e ré so udre cette récu rrence e n
util

isant la mé thod e gé né ra le, m ais sa solution est qu e *T(n)* est
8(n2 ). L e

rés ultat n \'es t pas m ei11 eur que p o ur le tri p ar sélec ti on ! D
a ns qu el c a s

pouvons- n o u s avoir une répartition si p eu uniforme ? Si ch aque
pivot est

supérie u r à to us les a utres é léme nts , a lors le tabl eau es t i n
itialement tri é.

Nous rencontrons également cette situation lo r sque le tableau es t tr
ié en

ordre inverse.

**Récap p.58**

![](media/image6.png){width="4.677083333333333in"
height="2.1666666666666665in"}![](media/image7.png){width="4.5in"
height="1.71875in"}

**Chapître 4**

![](media/image8.png){width="5.239583333333333in" height="2.59375in"}

Tri par comparaison :

Minorant existentiel : Cela veut dire qu'il nécessite une entrée : ᾨ
(nlg n ) comparaisons. Tout autre borne inférieur est un minorant
universel.

![](media/image9.png){width="3.9895833333333335in"
height="1.6875in"}![](media/image9.png){width="5.052083333333333in"
height="2.9479166666666665in"}

![](media/image9.png){width="4.677083333333333in"
height="2.6354166666666665in"}

![](media/image10.png){width="3.9270833333333335in" height="2.40625in"}

![](media/image11.png){width="3.6145833333333335in" height="2.1875in"}

Relire le tri par dénombrement

## Tri par base

Relire

## Tri à bulles (Livre Algo et Java)

Les valeurs voisines permutent ce qui fait que les plus élevées
remontent et les plus basses redescendent.

Complexité à O(n²) \[n²2n+1\]

Possibilité de l'optimiser en décrémentant -1 à chaque tour de boucle du
compteur.

Les complexités :

![](media/image12.png){width="4.40625in" height="3.53125in"}

**Type structurés**

DAG plus court chemin

![](media/image13.png){width="5.5in" height="1.1041666666666667in"}

![](media/image14.png){width="4.739583333333333in"
height="3.3541666666666665in"}

Recherche chaîne de caractère avec automate fini :

![](media/image15.png){width="4.21875in" height="3.0in"}
