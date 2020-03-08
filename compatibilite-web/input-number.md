Recueillez des valeurs numériques correctement
==============================================

Utilisez `<input type="number">` uniquement pour des nombres
------------------------------------------------------------

Un champ `<input type="number">` est conçu uniquement pour recevoir des nombres et pas des numéros.

Il n’est donc pas le bon choix pour récolter :

- un code PIN,
- un numéro de sécurité sociale,
- un identifiant comportant uniquement des chiffres,
- un numéro de rue,
- etc.

En règle générale, si vous ne pouvez pas faire d’addition avec votre valeur, c’est qu’elle n’est pas adaptée à `<input type="number">`.

Utilisez les attributs `inputmode` et `pattern`
-----------------------------------------------

L’attribut `inputmode` indique aux navigateurs mobiles le [type de clavier le plus adapté pour la saisie du champ](https://developer.mozilla.org/fr/docs/Web/HTML/Attributs_universels/inputmode).

L’attribut `pattern` indique aux navigateurs l’[expression rationnelle à laquelle doit répondre toute saisie dans un champ](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern). Une saisie ne correspondant pas à l’expression rationnelle placera le champ en état d’invalidité. Il peut alors être stylé avec la pseudo-classe `:invalid`.