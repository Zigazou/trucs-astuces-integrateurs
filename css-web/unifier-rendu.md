Unifiez le rendu entre navigateurs avec CSS reset ou Normalize.css
==================================================================

Chaque navigateur embarque une feuille de style par défaut qui, bien sûr, n’est pas identique d’un navigateur à l’autre.

**CSS reset** et **Normalize.css** existent pour corriger les incohérences entre navigateurs.

Grâce à eux on se soucie un peu moins des différences de rendu entre navigateurs.

[CSS reset](https://meyerweb.com/eric/tools/css/reset/) fait en sorte que tous éléments se comportent de la même façon (aucune marge interne/externe, pas de graisse, même taille de caractères…)

[Normalize.css](https://necolas.github.io/normalize.css/) garantit que chaque élément se comporte de la même façon d’un navigateur à un autre.

Dans un souci d’optimisation, il faut garder en tête que CSS reset occupe moins de 800 octets une fois minimisé tandis que Normalize.css nécessite environ 1700 octets.
