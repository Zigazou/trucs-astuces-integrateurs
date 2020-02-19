Récupérez proprement les images contenues dans un PDF
=====================================================

Le PDF est un format de fichier complexe qui peut contenir toute sorte d’informations : images bitmap, images vectorielles, polices de caractères, texte etc.

En tant qu’intégrateur, vous pouvez être amené à récupérer des images à partir d’un fichier PDF.

Autant le faire proprement et récupérer les images sans aucune dégradation. Vous pourriez même être surpris de constater que les images embarquées sont en fait tronquées lors du visionnage du PDF. Raison de plus pour utiliser la bonne méthode.

Les manipulations présentées ci-dessous visent la ligne de commande Linux.

## Récupérez les images bitmap

L’utilitaire qui nous intéresse s’appelle **pdfimages** et il est livré avec le paquet **poppler-utils** sous Linux.

Il reste simple d’utilisation même lorsqu’on n’est pas habitué à la ligne de commandes :

  pdfimages -all fichier.pdf image

Notes :

- `-all` force l’extraction des images telles qu’elles sont enregistrées dans le PDF,
- `fichier.pdf` est le nom du fichier PDF dont vous voulez extraire les images,
- `image` est le début du nom de fichier de chaque image produite (le format PDF ne contient pas les noms des fichiers), la commande ci-dessus produira donc les fichiers `image-000.png`, `image-001.jpg`, `image-002.png` etc.

Et voilà !

## Récupérez les images vectorielles

La récupération d’éléments vectoriels d’un PDF est un peu plus difficile que pour les images bitmap. En effet, tout ce qui est géométrique dans un PDF est regroupé par page.

Vous allez devoir réaliser manuellement l’extraction des éléments intéressants.

Le [logiciel de dessin vectoriel **Inkscape**](https://inkscape.org/fr/) est capable de lire directement du PDF.

Le paquet **poppler-utils** sous Linux fournit la commande **pdftocairo** qui vous permet de convertir un PDF en SVG mais ne résout pas le problème du nettoyage du résultat.

Une fois le PDF importé dans Inkscape, vous disposez de tous les outils d’édition pour conserver uniquement les éléments géométriques qui vous intéressent.
