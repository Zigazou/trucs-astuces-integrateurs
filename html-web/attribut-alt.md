Mettez un attribut `alt` à toutes les images !
==============================================

La règle est on ne peut plus simple : quelle que soit l’image, quel que soit le contenu de l’attribut, mettez toujours un attribut alt à chaque image.

L’attribut alt :

- est ignoré par les logiciels d’assistance s’il est vide (`<img alt="">`),
- est utilisé par les logiciels d’assistance s’il est rempli,
- est affiché lorsque l’image n’a pas encore pu être chargée (ou que son URL est erronée).

Cela entraîne la question : comment remplir l’attribut alt pour être accessible ?

La Web Accessibility Initiative du W3C a un document très complet à ce sujet qui passe en revue toutes les catégories d’image que vous serez amenés à rencontrer et comment remplir l’attribut alt en conséquence : [Web Accessibility Tutorials, Guidance on how to create websites that meet WCAG, Images](https://www.w3.org/WAI/tutorials/images/).

Si vous cherchez à faire apparaître un texte lorsque le curseur souris survole une image, c’est l’**attribut `title`** qu’il vous faut.
