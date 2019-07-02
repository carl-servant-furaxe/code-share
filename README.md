# Code de partage
Ce bout de code permet le partage via le javascript

## Requis
- Jquery 1.10.x ou plus (si gabarit Radio-Canada, il est inclus dans le app.js)
- FontAwesome 4.7.x
- Google Analytics (optionel)

## Fonctionnement
Au moment de cliquer sur un des boutons, le code javascript génèrera un url permettant le partage via un popup.
Ce code est composé des informations des meta données OG.

```
<meta property="og:title" content="CONCOURS Mission Lune | ICI Explora | ICI Radio-Canada." />
<meta property="og:url" content="https://ici.radio-canada.ca/edition/" />
<meta property="og:image" content="https://ici.radio-canada.ca/edition/share.png" />
<meta property="og:description" content="Concours Mission Lune! Remportez une des trois expériences d’astronomie ainsi que l’un des 10 livres Objectif Lune sur Apollo11." />
```

## Alternative
Vous pouvez egalement appliquer les valeurs directements au bouton, ce qui force le code à utiliser ces valeurs plutôt que celle des métas.
Cela est très utile lors d'appel ajax.

```
<li><button type="button" data-type="facebook" title="Partager sur Facebook" data-url="[1]" data-title="[2]" data-description="[3]" data-image="[4]">&#xf09a;</button></li>
```

| Data-Type | Description | Meta par defaut |
| :-------- | :---------- | :-------------- |
| data-url  | Url de partage | og:url |
| data-title | Titre du partage | og:title |
| data-description | Court texte descriptif | og:description |
| data-image | Image de partage | og:image |
