Travaillez en sRGB
==================

Si votre graphiste a conscienceusement réglé son poste de travail, il y a fort à parier qu’il ou elle ait calibré son écran. Cette opération génère un profil colorimétrique que les logiciels de manipulation d’image un tant soit peu évolués (PhotoShop, Gimp…) ajoutent aux fichiers qu’ils produisent.

Hormis le poids supplémentaire d’un profil colorimétrique dans un fichier image, le support des profils colorimétriques varie d’un navigateur à l’autre.

Pour s’en convaincre, il suffit d’effectuer le test [Is your system ICC Version 4 ready?](http://www.color.org/version4html.xalter) :

- **Chrome 81** supporte tous les profils colorimétriques,
- **Firefox 75** supporte les profils colorimétriques en version 2 mais pas en version 4 ([cela fait toujours l’objet d’un ticket ouvert il y a 11 ans !](https://bugzilla.mozilla.org/show_bug.cgi?id=488800))

Bref, on a plutôt intérêt à ne pas embarquer de profil colorimétrique dans les ressources d’une page HTML, à la fois pour l’optimisation et le rendu final.

Quand aucun profil colorimétrique n’est embarqué, les navigateurs utilisent le [profil sRGB](https://fr.wikipedia.org/wiki/SRGB) ou IEC 61966-2-1 par défaut depuis les années 1990. C’est également précisé par le W3C dans [CSS Color Module Level 3](https://www.w3.org/TR/css-color-3/).
