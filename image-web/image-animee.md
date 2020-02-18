Choisissez WEBP ou APNG pour les images animées plutôt que GIF
==============================================================

## Image animée ou vidéo, ne vous trompez pas

Une image animée présente les caractéristiques suivantes :

- des **animations courtes** car il n’y a pas de système de contrôle de l’animation,
- en **boucle** pour la même raison,
- nécessitant la **transparence**,
- pour des images **peu complexes**.

Pour de courtes séquences (ex. meme) souvent tirées de films, un format vidéo comme MP4 ou WEBM est préférable.

Et contrairement à la plupart des formats vidéo, [WEBM supporte la transparence alpha](https://simpl.info/videoalpha/) et cette fonctionnalité est supportée par Chrome et Firefox mais pas Safari.

La difficulté repose sur la création d’une telle animation. En termes de simplicité, le GIF est plus simple à produire que l’APNG, lui-même plus simple à produire que le WEBM transparent.

## Préférez APNG et WEBP à GIF

![Balle rebondissante](bouncing-ball.png)

[L’APNG a longtemps été boudé par les navigateurs](https://caniuse.com/#feat=apng) à l’exception de Firefox, mais il est bien supporté par Chrome (depuis 2017) et Safari.

[Le WEBP n’est pas encore supporté par Safari](https://caniuse.com/#feat=webp) mais l’est pas Firefox et Chrome.

Comment choisir :

- GIF présente le support le plus large possible, tant en visualisation qu’en création,
- APNG fonctionne sur tous les navigateurs modernes, dispose de la transparence alpha et de meilleurs taux de compression que GIF,
- WEBP disose de la transparence alpha et des meilleurs taux de compression.

## Palliez le manque de support de WEBP

HTML5 a introduit les balises `<picture>` et `<source>`. Elle permet de pallier au manque de support d’un format d’image. Cerise sur le gâteau, elle permet même de fournir au navigateur l’image la plus appropriée :

    <picture>
        <source srcset="animation-large.webp" media="(min-width: 800px)">
        <source srcset="animation-small.webp" media="(max-width: 800px)">
        <source srcset="animation-large.png" media="(min-width: 800px)">
        <source srcset="animation-small.png" media="(max-width: 800px)">
        <img src="animation.gif" />
    </picture>
