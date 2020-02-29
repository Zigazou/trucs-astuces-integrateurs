
### Convertir du vectoriel en bitmap

Tous les logiciels de dessin vectoriel propose un export en bitmap étant donné que la conversion est simple à réaliser.

Il faut cependant éviter d’y recourrir.

Le moteur de rendu SVG d’un navigateur peut effectuer des optimisations en fonction du matériel utilisé pour l’affichage.

On perd également la capacité du vectoriel à s’adapter à n’importe quel résolution d’écran.

### Convertir du bitmap en vectoriel

L’opération inverse est plus difficile puisqu’elle nécessite que le logiciel devine à quelle forme correspondent une série de pixels.

Mais elle peut être particulièrement utile.

## Optimisez vos images

### Demandez du PNG 24 bits à votre graphiste

Afin de pouvoir optimiser le plus possible une image, il est important de partir de la source la plus pure.

Un JPEG, même quand on met la qualité à 100% lors de l’enregistrement, dégrade toujours les images.

Le PNG est un format sans perte de données qui supporte la transparence alpha.

C’est le format idéal pour la transmission des ressources entre graphiste et intégrateur.

### Supprimez le superflux

Les formats JPEG et PNG peuvent contenir bien plus que l’image principale :

- méta-données **EXIF**  (conditions et paramètres de prise de vue),
- méta-données **IPTC**  (titre, auteur, copyright, description…),
- méta-données **XMP** (norme plus récente englobant IPTC),
- **vignette** (automatiquement ajoutée par les appareils photo),
- données propriétaires,
- profil colorimétrique **ICC**.

Mis à part le profil colorimétrique, les autres données ne sont pas utilisées par les navigateurs et sont donc chargées inutilement.



### Optimisez vos PNG avec TinyPNG

Le format PNG est propice à toutes sortes d’optimisation plus ou moins coûteuses que les logiciels (PhotoShop, Gimp etc.) n’implémentent pas, notamment celles concernant la transparence alpha.

[Le site TinyPNG](https://tinypng.com/) pallie ce manque.

Et, cerise sur le gâteau, TinyPNG gère parfaitement les fichiers APNG !

### Optimisez vos SVG avec SVGOMG!

[SVGO](https://github.com/svg/svgo) est une bibliothèque NodeJS d’optimisation de fichiers SVG et [SVGOMG! ou SVGO Missing Gui](https://jakearchibald.github.io/svgomg/) est son interface utilisateur en ligne.

SVGOMG! va plus loin que la simple minification du code SVG. Il peut supprimer les balises inutiles au rendu, réduire la précision des coordonnées, factoriser des styles etc.

### Optimisez vos JPEG

- compression JPEG
- compression PNG
- images CGI vs images naturelles
- réduction de couleurs
- copie d’écran (avec du texte)

## Favicons

- formats (historique et mobile)
- génération de favicons

## Regrouper des images

- fontes icônes WOFF, WOFF2
- sprites SVG

## Extraire des images

- attention aux copies d’écran

Il est toujours tentant de faire une copie d’écran

- extraction de bitmap d’un PDF
- extraction de vectoriel d’un PDF
- vectorisation d’un bitmap
