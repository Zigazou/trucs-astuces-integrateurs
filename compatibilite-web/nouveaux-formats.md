Utilisez `<picture>` pour les images, les résolutions et les vieux navigateurs
==============================================================================

Voici un casse-tête auquel un intégrateur est rapidement confronté :

- afficher une image adaptée à la densité de l’écran,
- la plus légère possible pour économiser les ressources,
- et rester compatible avec tous les navigateurs.

Avant HTML5, la solution consistait à utiliser des hacks (CSS ou navigateur) et du JavaScript.

Aujourd’hui, [la balise `<picture>`](https://html.spec.whatwg.org/multipage/embedded-content.html#the-picture-element) répond à toutes ces problématiques.

Attention : **la balise `<picture>` ne remplace pas la balise `<img>` !**

Voici un exemple :

    <picture>
        <source srcset="large.webp" type="image/webp" media="(min-width: 800px)">
        <source srcset="small.webp" type="image/webp" media="(max-width: 800px)">
        <source srcset="large.png" type="image/apng" media="(min-width: 800px)">
        <source srcset="small.png" type="image/apng" media="(max-width: 800px)">

        <img src="fallback.gif" alt="Alt attribute" width="640" height="480" />
    </picture>

Voici comment un navigateur supportant la balise `<picture>` va l’interpréter :

    SI supporte(image/webp) ET résolution > 800px ALORS
        <img src="large.webp" alt="Alt attribute" width="640" height="480" />
    SINON SI supporte(image/webp) ET résolution < 800px ALORS
        <img src="small.webp" alt="Alt attribute" width="640" height="480" />
    SINON SI supporte(image/apng) ET résolution > 800px ALORS
        <img src="large.png" alt="Alt attribute" width="640" height="480" />
    SINON SI supporte(image/apng) ET résolution < 800px ALORS
        <img src="small.png" alt="Alt attribute" width="640" height="480" />
    SINON
        <img src="fallback.gif" alt="Alt attribute" width="640" height="480" />

Voici comment un navigateur ne supportant pas la balise `<picture>` va/devrait l’interpréter :

    <img src="fallback.gif" alt="Alt attribute" width="640" height="480" />

Notes :

- la balise `<img>` est obligatoire dans la balise `<picture>`,
- l’attribut `<media>` contient une Media Query [[Media Queries Level 4](https://drafts.csswg.org/mediaqueries/)]
- le suppport des anciens navigateurs fonctionne dès l’instant où ceux-ci ignorent simplement les balises qu’ils ne connaissent pas,
- la balise picture ne gère pas les éventuelles erreurs 404, elle ne passera pas à la source suivante si une image n’est pas disponible (le navigateur affichera alors le contenu de l’attribut `alt`),
- il n’est pas possible de tester le support d’une particularité du format d’une source autrement que par le type MIME ; s’il est possible de différencier l’APNG (image/apng) du PNG (image/png), il est impossible de différencier un JPEG à encodage Huffman d’un JPEG à encodage arithmétique.
