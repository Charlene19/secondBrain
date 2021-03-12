+++
title = "Introduction Machine Learning Python"
author = ["cha"]
tags = ["machinelearning"]
draft = false
date = 2021-02-01T19:47:46+01:00
+++


J'ai installé : sklearn et jupyter sur PyCharm

Un ****processus stochastique**** ou processus aléatoire (voir Calcul stochastique) ou fonction aléatoire (voir Probabilité) représente une évolution, discrète ou à temps continu, d'une variable aléatoire. Celle-ci intervient dans le calcul classique des probabilités, où elle mesure chaque résultat possible (ou réalisation) d'une épreuve.

Cette notion se généralise à plusieurs dimensions. Un cas particulier important, le champ aléatoire de Markov, est utilisé en analyse spatiale.

**champ aléatoire de Markov** : est un ensemble de variables aléatoires vérifiant une propriété de Markov relativement à un graphe non orienté. C'est un modèle graphique.

**variable aléatoire** : est une application définie sur l'ensemble des
 éventualités, c'est-à-dire l'ensemble des résultats possibles d'une
 expérience aléatoire. Ce furent les jeux de hasard qui amenèrent à
 concevoir les variables aléatoires, en associant à une éventualité
 (résultat du lancer d'un ou plusieurs dés, d'un tirage à pile ou
 face, d'une roulette, etc.) un gain. Cette association
 éventualité-gain a donné lieu par la suite à la conception d'une
 fonction de portée plus générale. Le développement des variables
 aléatoires est associé à la théorie de la mesure.

**quartet d'Anscombe** :

<a id="orgc688cae"></a>

{{< figure src="/ox-hugo/quartetAnscombe.png" caption="Figure 1: quartet d'Anscomb" >}}

**Instance** ou observation sont des entrées dans un jeu de données.

**supervised learning et unsupervised learning** : Dans le cas des
 supervisés les données ont un label et sontclassés. Dans l'autre
 c'est à l'outils de trouver des similarités et d'effectuer ce
 classement.

Technique un peu moins utilisé : le semi-supervised learning, qui prend en entrée certaines données annotées et d'autres non. Ce sont des méthodes très intéressantes qui tirent parti des deux mondes (supervised et unsupervised), mais bien sûr apportent leur lot de difficultés.

le reinforcement learning, qui se base sur un cycle d'expérience /
 récompense et améliore les performances à chaque itération. Une
 analogie souvent citée est celle du cycle de dopamine : une "bonne"
 expérience
 augmente la dopamine et donc augmente la probabilité que l'agent
 répète l'expérience.


## La régression\* : Valeur continue un nombre {#la-régression-valeur-continue-un-nombre}


## La classification \* : Une valeur discrète (une catégorie) {#la-classification-une-valeur-discrète--une-catégorie}

\`
Il existe aussi un autre type de prédiction possible qui est de
sortir plusieurs labels de manière ordonnée (machine-learned ranking
en anglais). Par exemple, l'algorithme PageRank de Google retourne
des résultats de recherche dans l'ordre, du plus pertinent au moins
pertinent.
\`

**scoring** : Traduit la probabilité d'une réaction d'un individu à un
stimuli.

**CPC** (coût par clic) : le coût d'un clic sur une publicité

**CPM** (coût pour mille) : le coût pour mille impressions d'une publicité

**outlier** : évenement rare ou anomalies

**collaborative filtering** : qui se base sur des similarités entre
 utilisateurs, ou bien des similarités entre produits.

**clustering** : désigne les méthodes de regroupement automatique de
 données qui se ressemblent le plus en un ensemble de "nuages",
 appelés clusters.

**dataset unidimensionnel** : Les observations dépendent uniquement d'une variable.

**régression linéaire** : est un modèle de régression qui cherche à établir une relation linéaire entre une variable, dite expliquée, et une ou plusieurs variables, dites explicatives.
