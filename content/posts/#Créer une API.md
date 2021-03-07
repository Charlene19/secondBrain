---
title: "API : VertX"
date: 2020-12-06T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - programming
  - API
---




# #Créer une API 



[toc]







## ##Qu'est-ce qu'une API 

"Application Programming Interface " : permet d'accèder à des données ou des fonctions d'une application.

## ##API REST

>  **REpresentative State Transfer**

### #Les critères d'une API REST 

- Sans état : Le serveur ne fait aucune relation entre les différents appels d'un même client 
- Cacheable : Le client doit être capable de garder nos données en cache pour optimiser les transactions 
- Orienté client-serveur 
- Avec une interface uniforme 
- Avec un système de couche 

### #Création d'une API REST 

> - **GET** sera exclusivement utilisé pour **lire des données**
> - **POST** servira uniquement à **créer des données**
> - **PUT** servira uniquement à **mettre à jour des données**
> - **DELETE** sera réservé à la **suppression de données**

[ Tuto pour créer une API en Java avec VertX](https://thierry-leriche-dessirier.developpez.com/tutoriels/java/creer-api-rest-vertx-5-minutes/)   

### #Les API Asynchrones 

> On peut vouloir faire des traitements asynchrones pour différentes raisons. Si on s’en tient au développement web, la principale raison est de répondre plus vite aux requêtes des visiteurs, en exécutant certaines actions de manière différée. L’exemple classique est lorsqu’une action sur votre site doit déclencher un appel sur l’API d’un service tiers : Cet appel d’API peut prendre plusieurs secondes, et il peut même échouer en cas de problème momentané du service en question ; dans ce cas, plutôt que de faire attendre notre internaute, il vaut mieux lui répondre immédiatement et traiter cet appel d’API de manière asynchrone. Pareil pour des envois d’emails (même si les serveurs SMTP opèrent déjà de cette manière), des traitements sur des fichiers audio/vidéo, des calculs lourds, etc.









