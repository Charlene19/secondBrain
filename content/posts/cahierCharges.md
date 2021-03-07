---
title: "Cahier des Charges Prjet Front et Back-end"
date: 2020-12-01T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - untagged
---


## Projet Groupe

# Contenu {#contenu .TOC-Heading}

[Projet Groupe 1](#projet-groupe)

[Modalités 2](#_Toc56694768)

[Objectif du site 2](#_Toc56694769)

[Définition en méthodologie Scrum :
2](#définition-en-méthodologie-scrum)

[La conception du MCD : 4](#la-conception-du-mcd)

[Base de données : 4](#base-de-données)

[Choix de l'architecture (nouveauté)  :
6](#choix-de-larchitecture-nouveauté)

[La modularité des fonctionnalités du site :
7](#la-modularité-des-fonctionnalités-du-site)

[Les technos 8](#_Toc56694775)

[Back-end (nouveauté): 8](#back-end-nouveauté)

[L'architecture du back (nouveauté) :
8](#larchitecture-du-back-nouveauté)

[Les fonctionnalités du Back-End 9](#_Toc56694778)

[Les API's 11](#_Toc56694779)

[Front-end (nouveauté)  : 11](#front-end-nouveauté)

[L'architecture du front (nouveauté) 12](#_Toc56694781)

[Les API : 13](#les-api)

[Planning : 13](#planning)

[Avant le 9/11 14](#_Toc56694784)

[Semaine du 9 14](#_Toc56694785)

[Semaine du 16 14](#_Toc56694786)

[Semaine du 23 14](#_Toc56694787)

[Semaine du 30 15](#_Toc56694788)

[Du 30 au 2 : 15](#du-30-au-2)

[Du 3 au 4 15](#_Toc56694790)

[Semaine du 7 15](#_Toc56694791)

[Du 7 au 9 : 15](#du-7-au-9)

[10 : 15](#section)

[11 : 15](#section-1)

[]{#_Toc56694768 .anchor}**Modalités** : Concevoir un site internet et
une application de support type back-end réservé à l'administration du
site.

[]{#_Toc56694769 .anchor}**Objectif du site** : Réseau social permettant
l'échange entre utilisateurs.

Données échangées : Fichier multimédia, texte.

Type d'échange possible :

\- Public : toutes personnes présentes sur le site

\- Semi-Privé : une personne à un groupe

\- Privé : Une personne partage un évènement pour elle-même ou pour une
personne autorisée. \[tchat 1 vs 1 : optionnel\]

Type d'accès au site : Système de connexion sécurisée. Fonctionnalités
pour utilisateur non-connecté à définir.

### Définition en méthodologie Scrum : 

#### Backlog pour le côté admin: 

User Stories (US) 1 : En tant qu'administrateur je dois valider
l'inscription d'un client avec les informations qu'il aura fournies
soit :

-   Un email

-   Un nom d'utilisateur

-   Un mot de passe

US 2 : En tant qu'administrateur je dois pouvoir ajouter des
fonctionnalités au site web,tel que des API, des fonts, des
fonctionnalités.

US 3 : En tant qu'administrateur je dois pouvoir autoriser les
modifications d'un utilisateur sur ses données personnelles comme son
mail ou son mot de passe.

US 4 : En tant qu'administrateur je dois pouvoir supprimer le compte
d'un utilisateur de la base de données.

US 5 : En tant qu'administrateur je dois pouvoir accéder à tous les
utilisateurs.

US 6 : En tant qu'administrateur je dois pouvoir consulter tous les
groupes constitués sur le site.

US 7 : En tant qu'administrateur je dois pouvoir liés des thèmes à des
fonctionnalités \[sous forme d'ID\]

US 8 : En tant qu'administrateur je dois pouvoir supprimer les messages
malveillants qui m'auront été signalés via le bouton de signalement.
Cela au travers des règles qui auront été éditées sur le site.

US 9 : En tant qu'administrateur je dois pouvoir me logger pour accéder
au back-end.

US 10 : En tant qu'administrateur je dois pouvoir envoyer des emails aux
clients sanctionnées, ou qui souhaitent modifier des informations de
log.

####  Backlog pour le côté utilisateur :

User Stories (US) 1 : En tant qu'utilisateur, je dois pouvoir consulter
le site soit en étant logger ou en ne l'étant pas.

US 2 : En tant qu'utilisateur, je dois pouvoir me créer un compte en
fournissant un nom d'utilisateur unique, un email n'ayant jamais servie
sur le site et un mot de passe sécurisé.

US 3 : En tant qu'utilisateur, je dois pouvoir modifier mon compte, le
consulter et le supprimer.

US 4 : En tant qu'utilisateur, je dois pouvoir consulter des évènements
auquel l'accès m'ait autorisé. En les sélectionnant par intérêt : thème,
date ou créateur de l'évènement.

US 5 : En tant qu'utilisateur, je dois pouvoir créer des évènements en
fournissant un titre, un contenu.

US 6 : En tant qu'utilisateur, modifier des évènements que j'ai créés.

US 7 : En tant qu'utilisateur, je peux consulter des évènements auquel
j'ai le droit d'accès.

US 8 : En tant qu'utilisateur, je peux supprimer des évènements que j'ai
créés.

US 9 : En tant qu'utilisateur, je dois choisir qui j'autorise à
consulter et participer aux évènements que j'ai créés.

US 10 : En tant qu'utilisateur, je peux participer à des évènements en
ajoutant des évènements à un évènement.

US 11 : En tant qu'utilisateur, je dois pouvoir signaler un message que
je considère bafouer les règles du site.

US 12 : En tant qu'utilisateur, je peux consulter tous les évènements
que j'ai postés.

US 13 : En tant qu'utilisateur, je peux consulter tous les évènements
que j'ai postés ainsi que les réponses y apporter \[Répondre à un
évènement fait que les participants à cet évènement sont par défaut
autorisés à consulter l'évènement\].

US 14 : En tant qu'utilisateur, je peux choisir les thèmes qui
m'intéressent (à défaut thème imposé)

US 15 : En tant qu'utilisateur, je peux choisir les fonctionnalités que
je veux avoir sur ma page (à défaut fonctionnalités basiques)

US 16 : En tant qu'utilisateur, je peux me connecter et me déconnecter.

LES ressources :

[Backlog
scrum](https://www.nutcache.com/fr/blog/quest-ce-quun-backlog-scrum/)

### La conception du MCD : 

[Outils utilisés]{.ul} : Power AMC et Power Designer

Le MCD a été pensé avec au centre le membre du site. Des pôles se sont
dégagés :

-   L'administration du site

-   Les évènements

-   Les groupes

La conception du MCD a permis en plus de faire ressortir des pôles, de
définir les fonctionnalités de notre application.

Nous avons choisi d'étendre notre application sur deux serveurs. Ce
choix a aussi impacté notre conception du MCD.

### Base de données : 

[Microsoft SQL Server :]{.ul}

Base de données SQL et relationnelle, nous permet d'avoir une gestion
par entité. Ce qui nous semble essentiel pour la gestion des clients
(répétition des modèles : login/mot de passe) et a démontré son
efficacité en terme de sécurité.

Nous avons aussi choisi de positionner tous les éléments liés au site
web dans notre base de données SQL. En plus d'offrir une gestion
dynamique de notre application, cela permet une atteinte plus rapide de
nos éléments, sans besoin de plus de contrôle.

[Mongo DB :]{.ul}

La BDD Mongo DB semble la plus adaptée au projet. Notre application
étant un réseau social avec gestion de médias et échanges. La rapidité
d'accès aux éléments stockés dans la base, et la souplesse des données à
pouvoir stocker dans MongoDB nous a convaincu de choisir cette base de
données.

MongoDB bénéficie de passerelles avec Spring Boot que nous avons décidé
d'utiliser. La gestion Base de données -- métier en est ainsi facilitée.

#### Schéma MongoDB  :

User Document (\[

{ \_id : \<Object_id\>,

Username : \<Caractère\>}\])

Event Document(\[

{\_id : \<Object_id\>,

User_id\<Object_id\>,

Content :\<Object/string\>,

Type : \<Caractère\>,

Date :\<Date\>,

Titre :\<String\>}\])

Comment Document(\[

{\_id : \<Object_Id\>,

User_id : \<Object_Id\>,

Event_id : \<Object_Id\>,

Content : \<String\>}\])

Group Document(\[

{\_id :\<Object_Id\>,

Members : (\[

{ User Document (\[

{ \_id : \<Object_id\>,

Username : \<Caractère\>}\])

}\])

Description : \<String\>}\])

LES ressources :

[Maîtrisez les bases de données
NoSQL](https://openclassrooms.com/fr/courses/4462426-maitrisez-les-bases-de-donnees-nosql/4474601-decouvrez-le-fonctionnement-de-mongodb)

#### La gestion de deux bases de données : 

Nous avons dû rechercher la fiabilité de cette pratique. Cela nous a été
confirmé par des professionnels du métier. Grâce aux fichiers de
configuration que nous allons éditer dans notre création de projet
s'appuyant sur Maven, le mappage vers deux bases de données est
grandement facilitée.

LES ressources :

[tutoriel-spring-boot-et-mongodb](https://o7planning.org/fr/11773/tutoriel-spring-boot-et-mongodb)

### Choix de l'architecture (nouveauté)  : 

Packages-by-feature : Organisation en couche métiers. Moins répandue
mais plus adaptée à la conception en micro-services. (notion à définir).

![](media/image1.png){width="2.7399660979877516in"
height="4.7194083552056in"}

Modèle MVC : Très répandue. Modèle connue est facile à déployer.
Particulièrement intéressant pour la duplication.

![](media/image2.png){width="3.021255468066492in"
height="4.7194083552056in"}

#### L'architecture de l'application web Angular (nouveauté)  : 

Est nativement organisé par package by features. Chaque page (ou
application language Angular) est indépendante.

#### L'architecture du front Spring -- JPA --JavaFX  (nouveauté) : 

Gagne en simplicité à être déployé en package MVC.

LES ressources :

[Informations sur
l\'architecture](https://dzone.com/articles/project-package-organization)

### La modularité des fonctionnalités du site : 

Modularité adaptative selon les requêtes des utilisateurs connectés.

Liste non-exhaustive des possibles :

-   Choix du font

-   Choix des API déployées selon les intérêts

-   Choix du chiffrage durant le chat

-   Choix de la conservation des données (persistance des messages par
    exemple. Ou suppression des évènements à une durée définie)

-   Choix des implémentations : fbook, google, etc...

[]{#_Toc56694775 .anchor}**Les technos** :

Nous aurons deux sets de techno. Une pour le back-end et une autre pour
le front.

### Back-end (nouveauté):

Réservé à l'administration du site.

Le Back-end en JavaFX . Les problèmes de comptabilité sont pour
l'instant un frein à la conception avec IntelliJ et à l'intégration par
SpringBoot -- Maven.

Retour donc sur Java 8 et IntelliJ.

L'utilisation de Java 8 permet d'exploiter Spring.

L'articulation Java Fx et Spring a représenté un vrai défi. Le mélange
de deux technologie avec des starters propres s'est révélé assez
complexe.

De plus, les tests unitaires se sont montrés indispensable. Nous
utilisons JUnit inclut de base grâce à Spring.

### L'architecture du back (nouveauté) :

![](media/image3.png){width="3.9479166666666665in"
height="6.572916666666667in"}

[]{#_Toc56694778 .anchor}**Les fonctionnalités du Back-End** :

[Administration système]{.ul} :

1.  -- Compte personnel :

\- Le mot de passe doit pouvoir être modifié

\- Affichage en label du nom de l'administrateur.

\- Sous forme de ComboBox : les WebContent en gestion : jsp ce que c'est

2 -- Configuration rôle administrateur

-Liste des administrateurs sous forme de tableau

\- Liste des rôles possible

3 -- Etat du système

-A définir quand le site sera en place

4- Les logs

Faire un renvoi vers le fichier des logs. Hyperlien simple

[Gestion des utilisateurs et des groupes]{.ul} :

[Utilisateur]{.ul} :

Espace recherche d'un utilisateur : par son login, par ses évènements,
par son statut.

Tableau scrollable avec tous les utilisateurs.

Espace modération d'un utilisateur :

A définir

[Groupe]{.ul} :

Espace recherche d'un groupe : par son nom, par son nombre de
participants, par son id, par ses mots-clef

Espace modération d'un groupe :

A définir

[En attente de validation]{.ul} :

Espace modération Evènement : tableau

Espace modération Commentaires : tableau

Espace modération Client : tableau (méthode à définir)

Validation création de compte

[Gestion de l'application web :]{.ul}

Liste des API en Combo Box : quand sélectionner affichage dans un
tableau avec Id/Nom/Description

Liste des Fonts en Combo Box : quand sélectionner affichage dans un
tableau avec Id/Nom/Description

Liste des Images en Combo Box : quand sélectionner affichage dans un
tableau avec Id/Nom/Description

Liste des pages du site en Combo Box : quand sélectionner affichage dans
un tableau avec Id/Nom/Description

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

Liste des préférences avec un système d'association : Voir avec le
système de tree enfant/parent

LES ressources :

[Tuto Java FX Les teachers du net](https://youtu.be/kUwo3dTv75s)

[Pas à pas Java
FX](https://o7planning.org/fr/11533/ouvrir-une-nouvelle-fenetre-window-dans-javafx)

[Tutoriel JPA](https://koor.fr/Java/TutorialJEE/jee_jpa_introduction.wp)

Permet de gérer : les utilisateurs et leurs logs, les administrateurs et
leurs logs, les fonctionnalités du site, les images du site. En résumé
tout ce qui concerne l'architecture du site web.

[]{#_Toc56694779 .anchor}**Les API's** :

Ce sont elles qui vont nous permettre de faire le lien entre notre back
(et ses méthodes) et notre front.

Plusieurs particularités :

Nous avons une double base de données et donc une répartition
idiopathique de nos ressources. Nous voulons éviter au maximum la
duplication de code.

**Les Rest Controller** :

Nous avons été confronté à l'aspect difficilement compréhensible du
retour d'erreur. Nous avons donc utilisé ce tuto afin d'offrir une
verbosité plus adaptée à nos retour d'erreur.

https://www.toptal.com/java/spring-boot-rest-api-error-handling

### Front-end (nouveauté)  : 

Plusieurs choix : Déployer le site avec Symfony qui permet d'accéder à
des fonctionnalités complètes et avoir un site clef en main. Mais notre
formation orientée vers la conception d'applications, nous demande de
pouvoir penser et créer un site de A à Z.

Nous avons donc choisi de nous orienter vers Angular et [Spring]{.ul}
Boot.

Pour le choix d'Angular, nous avons fait un vote car les frameworks JS
sont nombreuses et amènent leurs lots d'avantages et d'inconvénients.

Angular est un framework décrit comme solide et ayant une grande
communauté. C'est pour cela que nous l'avons choisi. De plus son
déploiement avec Spring Boot est parfaitement optimisé.

Nous avons choisi de faire un : Site en SPA (Single Page), conception
plus dynamique et moderne.

[]{#_Toc56694781 .anchor}**L'architecture du front (nouveauté)** :

Un choix d'architecture :

![https://media.discordapp.net/attachments/768871458151333929/773842376812658688/unknown.png](media/image4.png){width="4.947916666666667in"
height="6.010416666666667in"}

LES ressources :

[Java et Angular Demo](https://github.com/marco76/java-demo)

[tutoriel-sur-creation-application-web-avec-angular7-et-spring-boot-2/](https://gkemayo.developpez.com/tutoriels/java/tutoriel-sur-creation-application-web-avec-angular7-et-spring-boot-2/)

[spring-boot-angular-7-crud-example-tutorial](https://www.javaguides.net/2019/06/spring-boot-angular-7-crud-example-tutorial.html?m=1)

Spring est favorisé à NodeJS car pour l'échange de fichiers multimédia
il est plus adapté. Node n'est pas fait pour les échanges de fichiers
volumineux.

De plus, Spring est plus fiable en termes de sécurité et bénéficie de
librairies de sécurisation.

LES ressources :

[Exemple de SPA Didactique](https://tiddlywiki.com/)

[Qques templates
gratuits](https://www.creative-tim.com/templates/angular-free)

[D\'autres](https://medium.com/akveo-engineering/top-9-free-admin-angular-9-and-bootstrap-4-dashboard-templates-2020-ff9f6d78428)

Des gadgets bootstrap :

[Des outils utiles (gestion date/boutons
etc\...)](http://angular-ui.github.io/bootstrap/)

[évènement en modal avec
Bootstrap](http://nakupanda.github.io/bootstrap3-dialog/)

[Gestion des images/vidéos/inclusion image
rs](http://ashleydw.github.io/lightbox/)

[Boostrap tour du siteWeb](http://bootstraptour.com/)

### Les API : 

C'est grâce à elle que notre site sera modulaire.

LES ressources :

[Cours Intégration
API](https://openclassrooms.com/fr/courses/3306901-creez-des-pages-web-interactives-avec-javascript/3722361-utilisez-des-api-web)

[Liste d\'API publique](https://github.com/public-apis/public-apis)

[Exemple d\'API OpenSource si intérêt
musique](https://z.musictools.live/)

[Pour aller plus loin :
REST](https://blog.bitsrc.io/vs-codes-rest-client-plugin-is-all-you-need-to-make-api-calls-e9e95fcfd85a)

# Planning :

Il serait intéressant de réfléchir à répartir certaines tâches en deux
groupes. Cela nous permettrait de doubler notre temps de travail. Ces
moments sont représentés par la notation (1) et (2) face aux tâches.

[]{#_Toc56694784 .anchor}**Avant le 9/11** :

Front-end (1) - Back-end (2) : Faire MCD -- Diagramme de cas
d'utilisation : optionnel -

Définition architecture du site

[]{#_Toc56694785 .anchor}**Semaine du 9** :

Diagramme de classe : essentiel (Retard. Elaboré le10/11)

(1) Faire le back-end en Spring et Java FX.

Le diagramme de classe aide à définir les actions demandées à
l'administration du site.

***Point groupe*** : remise en question sur les choix concernant la
génération des classes. De plus les validations n'ont pas été faîtes
correctement. Le MCD n'a pas été validé, ce qui a entraîné du retard
pour la génération du script de la base de données.

Le diagramme de classe a été fait une première fois de manière bancale
puisque le MCD n'est pas finale.

Le diagramme de classe a montré les faiblesses du MCD, des données
importantes ne sont pas intégrées.

\(2\) Choix du Bootstrap. Apprentissage Angular et Mongo DB.

[Site de prototypage optionnel mais peut-être
utile](https://www.ganatan.com/tutorials/bootstrap-avec-angular)

[]{#_Toc56694786 .anchor}**Semaine du 16** :

\(1\) Apprentissage Angular et Mongo DB. Regard et modification sur
l'architecture du site

\(2\) Listing des fonctionnalités de bases à implémenter. Apprentissage
du socket Java pour le chat

\-\--

Conception de la BDD Mongo DBB (pour les deux groupes)

[]{#_Toc56694787 .anchor}**Semaine du 23** :

\- BDD Mongo DBB doit être fonctionnelle

\- Architecture du site doit être fixée

\- Répartition des pages à chacun

[]{#_Toc56694788 .anchor}**Semaine du 30** :

### Du 30 au 2 : 

Travail individuel sur ses pages attribuées.

[]{#_Toc56694790 .anchor}**Du 3 au 4** :

Mise en commun des pages. Résolutions des conflits (GIT et au
déploiement).

[]{#_Toc56694791 .anchor}**Semaine du 7** :

### Du 7 au 9 :

La mise en commun de toutes les parties doit permettre d'avoir un site
fonctionnel. Conflits doivent être résolus.

Génération de la Java Doc, plus conception d'un index HTML stylisé avec
CSS (nous pourrons nous servir de l'architecture élaboré la semaine du
9) .

### 10 : 

(1) Fin de la résolution des conflits

(2) Edition du PPT avec Prezi : <https://prezi.com/i/create/slides>

Tout le monde : doit préparer sa présentation orale.

### 11 : 

Réserver à la présentation du projet. Cette journée devra servir à faire
un tour du site en groupe. Puis à faire une sorte d'oral blanc.

Pour la présentation, le temps se répartir de manière égale entre chaque
participant. Durant cet oral blanc, nous établiront l'ordre de passage,
et la partie qui sera présentée.
