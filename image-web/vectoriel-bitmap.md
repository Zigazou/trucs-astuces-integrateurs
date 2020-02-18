Vectoriel ou bitmap, choisissez le plus adapté
==============================================

Il existe deux techniques pour décrire une image :

- le **bitmap** énumère chaque point composant l’image,
- le **vectoriel** énumère chaque élément composant l’image.

## Le bitmap pour les photos et images complexes

Le bitmap est contenu dans des fichiers au format JPEG, PNG, GIF, TIFF etc.

C’est le fonctionnement natif d’un écran d’ordinateur, d’un appareil photo ou d’une imprimante laser.

Sans prendre en compte la compression, le poids d’un bitmap est déterminé par le nombre de points utilisés et les informations de couleur attribuées à chaque point.

Le bitmap présente l’inconvénient d’être pixellisé à mesure que l’on zoome (effets escalier) mais est bien adapté à la représentation d’images naturelles comme les photographies.

Il y a 3 formats bitmap à utiliser sur le web :

- **JPEG**, dans sa version originale (oubliez le [JPEG 2000](https://caniuse.com/#feat=jpeg2000), le [JPEG XR](https://caniuse.com/#feat=jpegxr) ou le JPEG à encodage arithmétique car ils sont très peu supportés par les navigateurs), pour toutes les images « naturelles »
- **PNG**, 
- **APNG**, le [PNG animé](https://caniuse.com/#feat=apng), équivalent du GIF animé pour le PNG avec support de la transparence alpha, est désormais bien supporté dans les navigateurs à l’exception d’Internet Explorer et de Edge avant son passage à Webkit.
- **GIF**,

## Le vectoriel pour les images géométriques et fines

Le vectoriel est contenu dans des fichiers au format SVG ou AI. Ce dernier format étant propriétaire, il n’est pas utilisé pour la visualisation d’images vectorielles.

Sans prendre en compte la compression, le poids d’une image vectorielle est déterminé par le nombre d’éléments utilisés.

Le vectoriel présente l’avantage d’un niveau de qualité constant à mesure que l’on zoome mais n’est pas adapté à la représentation d’images naturelles.

C’est cet avantage qui permet au vectoriel d’avoir le rendu le plus fin possible quel que soit le périphérique de rendu utilisé. Si le moteur de rendu du vectoriel est suffisamment avancé, il peut même profiter des sous-pixels d’un écran pour tripler la résolution horizontale perçue.

Le vectoriel, notamment SVG, a eu un regain d’intérêt ces dernières années pour deux raisons. Tout d’abord SVG est largement supporté que ce soit sur desktop ou sur mobile. Ensuite la grande variété de résolutions d’écran ainsi que l’explosion du nombre de pixels le rendent particulièrement pratique.
