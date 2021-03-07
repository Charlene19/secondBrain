---
title: "Angular"
date: 2020-03-07T19:47:46+01:00
draft: false
toc: false
images:
tags: 
  - untagged
---

# Angular

## Installation

Permet d'installer le module de node.js dans le projet

```Node.js
npm install -g npm@latest
```

Puis, cela pour installer le CLI d'Angular 

```
npm install -g @angular/cli
```

Si le projet est importé ou déjà créer, il faut juste lancer le server : 

```
ng serve
```

Sinon, on peut créer le projet au travers d'une ligne de code 

```
ng new mon-premier-projet
```

La commande 

```
npm install
```

permet de télécharger des modules nécessaire. Exemple bootstrap. 

Pour ajouter les modules télécharger il faut se rendre dans le fichier : angular.json puis mettre en lien la localisation des modules installés. 

```
"styles": [
  "node_modules\\bootstrap\\dist\\css\\bootstrap.css",
  "src\\styles.css"
]
```
<!--more--> 

## Création de l'application : 

Angular CLI génere une architecture de programe.

![](C:\Users\Charlène\Desktop\Memo\image-20201101141705710.png)

Pour créer un nouveau composant : 

```
ng generate component [nomComposant]
```

Il est important de bien se positionner dans le dossier où doit être générer le composant. 

L'appel des composants se fait dans l'app principal : "app.component.html" dans notre architecture. 

```
<app-appareil></app-appareil>
```

Les fichiers "app.nomComposant".ts enferment les élements qui permettent de déployer les pages. 

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
 isAuth = false;

  appareilOne = 'Machine à laver';
  appareilTwo = 'Frigo';
  appareilThree = 'Ordinateur';

  constructor() {
    setTimeout(
      () => {
        this.isAuth = true;
      }, 4000
    );
  }

  onAllumer(){
    console.log("on allume tout");
  }
}
```

> - `selector` : il s'agit du nom qu'on utilisera comme balise HTML pour afficher ce component, comme vous l'avez vu avec  `<app-root>` . Ce nom doit être unique et ne doit pas être un nom réservé HTML de type  `<div>` ,  `<body>` etc. On utilisera donc très souvent un préfixe comme  `app` , par exemple ;
> - `templateUrl` : le chemin vers le code HTML à injecter ;
> - `styleUrls` : un array contenant un ou plusieurs chemins vers les feuilles de styles qui concernent ce component ;

## Module 

Le module : app.module.ts se met à jour à chaque géneration de composant. 

 

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';


import { AppComponent } from './app.component';
import { MonPremierComponent } from './mon-premier/mon-premier.component';


@NgModule({
  declarations: [
    AppComponent,
    MonPremierComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

## Gestion des DOM

Liaison ou DataBinding : c'est la communication entre le code TypeScript et le template HTML. 

> - les informations venant de votre code qui doivent être affichées dans le navigateur, comme par exemple des informations que votre code a calculé ou récupéré sur un serveur.  Les deux principales méthodes pour cela sont le "string interpolation" et le "property binding" ;
> - les informations venant du template qui doivent être gérées par le code : l'utilisateur a rempli un formulaire ou cliqué sur un bouton, et il faut réagir et gérer ces événements.  On parlera de "event binding" pour cela.

### L'interpolation

```typescript
<li class="list-group-item">
  <h4>Appareil : {{ appareilName }}</h4>
</li>
```

Les {{ }} permettent de mettre l'objet TypeScript dans le HTML de manière dynamique. 

Pour notre exemple, dans le fichier appareil.component.ts, voilà comment nous allons définir l'objet ts. 

```typescript
export class AppareilComponent implements OnInit {
  
  appareilName: string = 'Machine à laver';

  constructor() { }
```

L'interpolation fonctionne aussi avec des méthodes. 

```typescript
getStatus() {
    return this.appareilStatus;
  }
```

### Property binding

Permet de modifier dynamiquement les propriétés d'un élément du DOM en fonction de données dans le fichier TypeScript.

Dans le fichier app.component.ts on ajoute la propriété isAuth de type booléen. 

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
  isAuth = false;
}
```

Pour lier cette propriété au template, il faut la mettre dans le template HTML ici : app.component.html. Pour lier l'action à la propriété il faut mettre l'action entre crochets : [ ]. Ceci lit l'action à la propriété du component. Ici le bouton est disabled si isAuth n'est  pas true. 

```typescript
<button class="btn btn-success" [disabled]="!isAuth">Tout allume</button>
```

### Event binding

Permet de communiquer de l'HTML vers le code ts. 

```typescript
<div class="container">
  <div class="row">
    <div class="col-xs-12">
      <h2>Mes appareils</h2>
      <ul class="list-group">
        <app-appareil></app-appareil>
        <app-appareil></app-appareil>
        <app-appareil></app-appareil>
      </ul>
      <button class="btn btn-success" 
              [disabled]="!isAuth" 
              (click)="onAllumer()">Tout allumer</button>
    </div>
  </div>
</div>
```

Il ne nous reste plus qu'à créer la méthode : onAllumer() dans notre fichier ts : app.component.ts. 

### Two-way binding

> La liaison à double sens (ou two-way binding) utilise la liaison par propriété et la liaison par événement en même temps ; on l'utilise, par exemple, pour les formulaires, afin de pouvoir déclarer et de récupérer le contenu des champs, entre autres.

Il faudra penser à importer le FormsModule dans le app.module.ts : 

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';


import { AppComponent } from './app.component';
import { MonPremierComponent } from './mon-premier/mon-premier.component';
import { AppareilComponent } from './appareil/appareil.component';
import { FormsModule } from '@angular/forms';


@NgModule({
  declarations: [
    AppComponent,
    MonPremierComponent,
    AppareilComponent
  ],
  imports: [
    BrowserModule,
    FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Le two-way binding se matériale comme ça : [( )]

 

```
<li class="list-group-item">
  <h4>Appareil : {{ appareilName }} -- Statut : {{ getStatus() }}</h4>
  <input type="text" class="form-control" [(ngModel)]="appareilName">
</li>
```

<u>ngModel</u> : Il va récuperer le string appareilName définit dans le app.appareil.ts

### Propriétés personnalisées

Les décorateurs sont comme des notation. Ex @Input

## Les directives 

On peut utiliser des directives natives ou en créer. 

### Les directives structurelles

```typescript
<li class="list-group-item">
  <div style="width:20px;height:20px;background-color:red;" 
       *ngIf="appareilStatus === 'éteint'"></div>
  <h4>Appareil : {{ appareilName }} -- Statut : {{ getStatus() }}</h4>
  <input type="text" class="form-control" [(ngModel)]="appareilName">
</li>
```

<u> *ngIf :</u> fonctionne comme if en java

```typescript
 <app-appareil  *ngFor="let appareil of appareils"
                       [appareilName]="appareil.name"
                       [appareilStatus]="appareil.status"></app-appareil>
```

<u> *ngFor : </u> fonctionne comme une boucle. "appareils" est un tableau qui est une propriété de notre app.appareil

### Les directives par attribut 

> À la différence des directives structurelles, les directives par attribut modifient le comportement d'un objet déjà existant. 

<u>ngModel</u> : qui permettait de modifier une valeur grâce à une propriété

<u>ngStyle</u> : 

```
<h4 [ngStyle]="{color: getColor()}">Appareil : {{ appareilName }} -- Statut : {{ getStatus() }}</h4>
```

```typescript
getColor() {
    if(this.appareilStatus === 'allumé') {
      return 'green';
    } else if(this.appareilStatus === 'éteint') {
      return 'red';
    }
}
```

<u>ngClass</u> : Une classe est ajouté. 

```typescript
<li [ngClass]="{'list-group-item': true,
                'list-group-item-success': appareilStatus === 'allumé',
                'list-group-item-danger': appareilStatus === 'éteint'}">
  <div style="width:20px;height:20px;background-color:red;"
       *ngIf="appareilStatus === 'éteint'"></div>
  <h4 [ngStyle]="{color: getColor()}">Appareil : {{ appareilName }} -- Statut : {{ getStatus() }}</h4>
  <input type="text" class="form-control" [(ngModel)]="appareilName">
</li>
```

## Les pipes

> Les pipes (/pʌɪp/) prennent des données en input, les transforment, et puis affichent les données modifiées dans le DOM. Il y a des pipes fournis avec Angular, et vous pouvez également créer vos propres pipes si vous en avez besoin. 

Le caractère : | permet d'influer sur l'objet sans en modifier sa nature. 

```typescript
lastUpdate = new Date();
<p>Mis à jour : {{ lastUpdate }}</p>
<p>Mis à jour : {{ lastUpdate | date }}</p>
<p>Mis à jour : {{ lastUpdate | date: 'short' }}</p>
```

### Utilisez une chaîne de Pipes

> Le pipe  `async` est un cas particulier mais extrêmement utile dans les applications Web, car il permet de gérer des données asynchrones, par exemple des données que l'application doit récupérer sur un serveur. 

Le pipe a en constructeur new Promise((resolve, reject)) : 

```typescript
lastUpdate = new Promise((resolve, reject) => {
    const date = new Date();
    setTimeout(
      () => {
        resolve(date);
      }, 2000
    );
  });
```

## Les services 

### La portée

Un service est un composant qui permet de provoquer une action. Celui-ci, selon sa localisation, va pouvoir étendre ou restreindre sa portée. 

Pour créer un service, la convention indique qu'il faut créer un dossier sous App : service. Dans ce dossier, on créé notre service: app.service.ts. 

> export class AppareilService {}

va nous permettre d'exporter notre service. 

Pour exporter notre service, il va falloir l'importer dans nos composant, si l'on veut une portée local ou dans app.module.ts pour une portée globale aux modules. Pour une simple portée aux composants du module, on peut placer notre service dans app.component.ts.

```typescript
import {AppareilService} from './service/appareil.service';
```

En plus de l'import, il faut aussi déclarer notre service dans le constructeur : 

```typescript
constructor(private appareilService: AppareilService ) {
    setTimeout(
      () => {
        this.isAuth = true;
      }, 4000
    );
  }
```

Et indiquer dans l'app.module.ts que AppareilService sera un providers : 

```typescript
  providers: [
    AppareilService
  ],
```



### L'import de propriété d'autres composants 

Prenons l'exemple d'une liste présente dans le ts de notre classe : appareil.component : 

```typescript
appareils = [
  {
    name: 'Machine à  laver',
    status: 'allumé'
  },
  {
    name: 'Télevision', status: 'allumé'
  },
  {
    name: 'Ordinateur', status: 'éteint'
  }
];
```

Afin de pouvoir l'utiliser dans le template de : app.component.html qui est notre app-root, dans le app.component.ts nous allons y faire référence comme ceci : 

```typescript
  appareils: any[];
```

### L'utilisation individuelle des services 

L'utilisation d'un index sous la forme number, permet de provoquer une action sur le composant cible. 

Dans le appareil.component.ts : 

```typescript
export class AppareilComponent implements OnInit {
  @Input() appareilName: string;
  @Input() appareilStatus: string;
  @Input() index: number;

```

Ajout de la propriété index. 

Puis dans le module du même composant, l'AppareilService est introduit comme paramètre du constructeur. 

 Le module root : app.component pourra donc faire explicitement appel à un des composants via cette variable : 

```typescript
<ul class="list-group">
        <app-appareil  *ngFor="let appareil of appareils; let i = index"
                       [appareilName]="appareil.name"
                       [appareilStatus]="appareil.status"  [index]="i"></app-appareil>
      </ul>
```

