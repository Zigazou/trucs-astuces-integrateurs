Pensez CSP, dégagez tous les « inline »
=======================================

## Anticipez l’évolution

Les [Content Security Policy](https://developer.mozilla.org/fr/docs/Web/HTTP/CSP) imposent de revoir profondément le fonctionnement de beaucoup de pages HTML si on veut profiter du maximum de sécurité qu’ils proposent.

S’il faut retenir quelque chose des CSP, c’est que le contenu « inline » est à bannir. Autrement dit : le HTML dans le HTML, le CSS dans le CSS et le JS dans le JS.

Quelques exemples de contenu « inline » :

- `<div style="color: yellow">`
- `<script>var truc = 42;</script>`
- `<img src="data:image/gif;base64,…" />`

Il est possible de les autoriser quand on fait des règles CSP mais le mot-clé à utiliser n’inspire pas confiance : **unsafe-inline**.

## Vérifiez la compatibilité CSP de vos bibliothèques et framework

Non seulement vous devez faire attention à vos propres pratiques, mais vous devez également faire attention aux différents frameworks et bibliothèques qui, eux, ont gardé des mauvaises habitudes.

C’est le cas par exemple de [la bibliothèque Masonry](https://masonry.desandro.com/) qui va réorganiser le contenu en utilisant des style CSS inline.

Les CSP impliquant des contraintes fortes sont donc à prendre en considération dès les balbutiements de votre projet [[Déployer CSP : une approche en 5 étapes](https://blog.dareboost.com/fr/2018/03/deployer-csp-une-approche-en-5-etapes/)].
