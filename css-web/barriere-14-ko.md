Restez en dessous de 14 Ko
==========================

## Limitez la taille des fichiers CSS

Si vous prenez la version minifiée de Bootstrap (bootstrap.min.css), vous vous retrouvez avec un CSS de 160 Ko. En activant la compression GZip sur le serveur web, ce fichier sera au mieux réduit à 23 Ko lors de son voyage à travers le réseau.

C’est peu mais ça reste problématique :

- si le serveur ne dispose pas de mise en cache, le fichier sera **compressé à chaque envoi**,
- le navigateur **interprètera et gérera** 160 Ko de CSS,
- on reste au-dessus de la **barrière des 14 Ko**.

Lorsqu’on fait son intégration en local, difficile de se rendre compte à quel point tout ceci est lourd à gérer même en considérant la puissance des processeurs et l’optimisation des navigateurs.

## Mieux, restez en dessous de 14 Ko

D’où vient cette barrière des 14 Ko ?

Il faut savoir que chaque nouvelle connexion TCP ne peut utiliser immédiatement toute la bande passante disponible. Elle doit passer par un démarrage lent pour éviter de surcharger la connexion. Dans ce processus, le serveur débute le transfert avec une petite quantité de données et, si cette quantité de données parvient correctement à destination, il double la quantité lors du prochain aller-retour.

Pour la plupart des serveurs, 14 Ko (soit 10 paquets) est le maximum transférable lors du premier aller-retour. [[Extract Critical CSS](https://web.dev/extract-critical-css/)]

Il faut donc chercher à garder une feuille de styles minifiée et compressée en dessous de ces 14 Ko.

Bien que cela soit valable pour les autres ressources d’une page, la feuille de style est critique car, si elle n’est pas chargée complètement à temps, elle force le navigateur à tenter plusieurs rendus de la même page.
