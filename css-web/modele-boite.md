Maîtrisez le modèle de boîte
============================

Les éléments d’une page HTML sont divisés en 2 catégories :

- éléments en ligne,
- éléments bloc.

Utilisez le bon modèle de boîte
-------------------------------

Tous les éléments bloc d’une page HTML sont soumis à un modèle de boîte. Il en existe deux.

### Modèle de boîte standard `content-box`

<img src="content-box.svg" alt="Modèle de boîte standard">

### Modèle de boîte alternatif `border-box`

<img src="border-box.svg" alt="Modèle de boîte alternatif">

Domptez la marge extérieure `margin`
------------------------------------

La marge extérieure a un comportement déroutant quand on ne comprend pas son mode de fonctionnement.

Elle est très différente de la marge intérieure `padding` :

- elle est obligatoirement transparente,
- elle peut être négative,
- elle indique un espace minimum à réserver autour de la boîte.

Cette dernière différence est importante : la marge extérieure ne fait pas partie de la boîte.

Un nouveau contexte de formatage de bloc est déclenché à l’intérieur d’un élément bloc par l’une des déclarations suivantes:

- float: left/right,
- position: absolute,
- display: inline-block/table-cell/table-caption,
- overflow: auto/hidden/scroll,
- overflow-x: auto/hidden/scroll,
- overflow-y: auto/hidden/scroll.
