N’oubliez pas de configurer `robots.txt` lors du développement
==============================================================

Si vous ne voulez pas que le site sur lequel vous travaillez soit indexé par les moteurs de recherche, **il faut le dire explicitement à leurs robots**. Dans le cas contraire, vous pourriez bien retrouver votre site indexé avec une URL de développement ou des lorem ipsum.

Ces robots tentent de lire tout ce qu’il est possible de lire et, ce, sans même que vous ayez eu besoin de soumettre votre site à leurs bons soins. Google, pour ne citer que lui, a une mémoire un rien persistante.

N’oubliez jamais de [configurer correctement votre fichier **robots.txt**](http://robots-txt.com/) !

Pour un site en cours de développement, le robots.txt a juste besoin de contenir les deux lignes suivantes :

    User-agent: *
    Disallow: /

Gardez en mémoire les points suivants :

- n’oubliez pas de le reconfigurer pour la mise en production du site, sinon votre site ne sera jamais indexé,
- l’**absence de fichier robots.txt** est considéré par les moteurs de recherche comme une autorisation ipso facto à indexer tout votre site.

En cas de besoins spécifiques, vous disposez également des [balises &lt;meta name="robots" content="…"&gt;](https://viaprestige-agency.com/comment-utiliser-les-balises-meta-pour-empecher-lindexation-dune-page-web/). Elles offrent la particularité de pouvoir laisser les robots crawler vos pages sans pour autant les indexer.
