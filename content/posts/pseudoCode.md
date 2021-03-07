---
title: "Pseudo code"
date: 2020-03-06T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - algorithmie
---




14. Créer une chaîne de caractères de 50 '-'

DEBUT

CHAR cara = "-" ENTIER cpt = 50 ENTIER i = 0

    POUR i à cpt -1 
        AFFICHE cara 
    FINPOUR 

FIN

15. Inverser une chaîne de caractères (sans supprimer l'originale).

CHAINE a \<- "Random" CHAINE b ENTIER i, j, longueur

longueur \<- a.longueur j \<- 0

    TANTQUE i > 0 

        POUR i <- longueur à i > 0 

        b AJOUTE a(i) 
        i <- i -1 
        FINPOUR 
    FINTANTQUE

FIN

19. Afficher la présence d'une lettre dans une chaîne (si oui, en
    afficher le nombre (quantité, si non, afficher "absent").

DEBUT

CHAINE r \<- "random" CHAR \<- 'r' ENTIER i, j ENTIER i \<- 0

    POUR i à r.longueur 

        SI  r[i] == 'r' 

        ALORS j <- j+1 

        FINSI 

AFFICHE

    SI j >= 1 

        "Il y a" + j + "fois, le caractère" 

    FINSI 

        SI j == 0 

        AFFICHE "Absent" 

        FINSI 

FIN

20. Compter le nombre d'occurrences de chaque lettre dans une chaine.

DEBUT

CHAINE r \<- "random" CHAR \<- 'r' ENTIER i, j ENTIER i \<- 0

    POUR i à r.longueur 

        SI  r[i] == 'r' 

        ALORS j <- j+1 

        FINSI 

AFFICHE

        j 

FIN

21. Remplacer les double-espace (ou +) dans une chaîne de caractères par
    un espace.

DEBUT

CHAINE r \<- "random" CHAR \<- 'r' ENTIER i ENTIER i \<- 0

    POUR i à r.longueur 

        SI  c[i] == SPACE && c[i+1] == SPACE 

            ALORS c[i] <- c[i+1] 

        FINSI 

            SI c[i] == '+' && c[i+1] == '+' 

                ALORS c[i+1] <- ' ' && c[i] <- c[i+1] 

            FINSI 
    FINPOUR 

FIN

22. Découper une chaîne de caractères en mots avec l'espace comme
    séparateur et les compter.

23. Inverser les mots d'une phrase.

DEBUT

CHAINE exo \<- "Ici, il y a du soleil" ENTIER i, start, fin CHAINE
rewrite \<- 1, 2, 3, 4 ,5, 6

start \<- exo \[0\]

    POUR i à exo.longueur

        SI exo [i] == SPACE 

            ALORS rewrite(1) <- [start à i] 
            i <- i +1
            rewrite <- +1   

        FINSI 

    FINPOUR 

AFFICHE rewrite 6, 5, 4, 3, 2, 1 FIN
