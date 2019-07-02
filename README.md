# Code de partage
Ce bout de code permet le partage de lien vers les differents reseaux sociaux via le javascript

## Requis
- Jquery 1.10.x ou plus (si gabarit Radio-Canada, il est inclus dans le app.js)
- FontAwesome 4.7.x
- Google Analytics (optionel)

## Code
```
<!-- share -->
<div class="share">
	<div class="share-title">Partagez</div>
	<div class="share-container">
		<ul>
			<li><button type="button" data-type="delicious" title="Partager sur Delicious">&#xf1a5;</button></li>
			<li><button type="button" data-type="digg" title="Partager sur Digg">&#xf1a6;</button></li>
			<li><button type="button" data-type="facebook" title="Partager sur Facebook">&#xf09a;</button></li>
			<li><button type="button" data-type="googleplus" title="Partager sur Google+">&#xf0d5;</button></li>
			<li><button type="button" data-type="linkedin" title="Partager sur LinkedIn">&#xf0e1;</button></li>
			<li><button type="button" data-type="mailto" title="Partager par Courriel">&#xf0e0;</button></li>
			<li><button type="button" data-type="pinterest" title="Partager sur Pinterest">&#xf231;</button></li>
			<li><button type="button" data-type="reddit" title="Partager sur Reddit">&#xf281;</button></li>
			<li><button type="button" data-type="radiocanada" title="Partager par Courriel">&#xf0e0;</button></li>
			<li><button type="button" data-type="stumbleupon" title="Partager sur StumbleUpon">&#xf1a4;</button></li>
			<li><button type="button" data-type="tumblr" title="Partager sur Tumblr">&#xf173;</button></li>
			<li><button type="button" data-type="twitter" title="Partager sur Twitter">&#xf099;</button></li>

		</ul>
	</div>
</div>
<!-- /share -->
```

## Fonctionnement
Au moment de cliquer sur un des boutons, le code javascript génèrera un url permettant le partage via un popup.
Ce url est composé des informations provenant des meta données OG.

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

| # | Data-Type | Description | Meta par defaut |
| - | :-------- | :---------- | :-------------- |
| [1] | data-url  | Url de partage | og:url |
| [2] | data-title | Titre du partage | og:title |
| [3] | data-description | Court texte descriptif | og:description |
| [4} | data-image | Image de partage | og:image |
