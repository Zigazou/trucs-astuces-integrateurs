Ayez une pensée pour l’accessibilité
====================================

Faites-vous une bonne idée de l’accessibilité
---------------------------------------------

[97,6% des lecteurs d’écran fonctionnent avec JavaScript](https://a11yproject.com/posts/people-who-use-screen-readers-dont-use-javascript/).

[L’accessibilité n’est pas réservée aux aveugles](https://a11yproject.com/posts/people-who-use-screen-readers-dont-use-javascript/), elle adresse une variété de handicaps visuels, auditifs, moteurs, cognitifs, permanents ou temporaires.

Il n’est pas possible d’automatiser complètement les tests d’accessibilité.

Faites au moins le minimum
--------------------------

Sans entrer dans les détails, l’accessibilité étant un domaine très vaste, assurez-vous que :

- tous les contrastes sont suffisants [[Contrast checker](https://contrastchecker.com/)],
- toutes les informations sont disponibles en texte brut (images légendées, vidéos sous-titrées…),
- vous utilisez des composants JavaScript accessibles [[Vanilla accessibility](https://van11y.net/)],
- vous bannissez les liens du type « cliquez ici » ou « en savoir plus »,
- vous utilisez une taille de police suffisamment grande(*).

Si, déjà, vous respectez ces quelques règles, vous aurez fait le gros du travail.

(*) Oui, vous êtes jeunes, vous n’avez aucun problème pour lire des petits caractères à 3 mètres de votre écran. Profitez-en, ça ne durera pas ;-)

Faites attention aux faux-amis
------------------------------

[Comme le signale Dave Rupert dans son article HTML: The Inaccessible Parts](https://daverupert.com/2020/02/html-the-inaccessible-parts/), on aurait tendance à imaginer que les balises HTML n’ont pas de défaut en matière d’accessibilité.

Si c’est globalement vrai, ce n’est pourtant pas toujours le cas.

L’auteur recommande donc de tester en situation réelle les balises et attributs suivants :

- `<input type="number">`, voir aussi [What to use instead of number inputs](https://css-tricks.com/what-to-use-instead-of-number-inputs/),
- `<input type="date">`,
- `<input type="search">`,
- `<select multiple>`,
- `<progress>`,
- `<meter>`,
- `<dialog>`,
- `<details><summary>`,
- `<video>`,
- `<div onclick>`,
- `<div aria-label>`,
- `<a href><div>Block Links</div></a>`,
- `aria-controls`,
- `role="tablist"`.

L’article recense toutes les pages pointant des problèmes d’accessibilité.