Choisissez entre documents et composants
========================================

Lorsqu’on construit une feuille de styles CSS, il existe deux approches principales :

- l’approche orientée **documents**, telle qu’adoptée par CSS Zen Garden,
- l’approche orientée **composants**.

[CSS Zen Garden](http://www.csszengarden.com/) a été une véritable révolution pour les intégrateurs en 2003 : la plateforme démontrait la puissance des feuilles de style CSS à une époque où la mise en page des sites était encore faite à base de balises &lt;table&gt;, de styles en ligne et d’attributs dédiés à la forme.

L’approche orientée documents de CSS Zen Garden imposait que le CSS s’adapte au document. Sans changer la page HTML, de nouveaux thèmes étaient appliqués.

Cette approche impose une dépendance du CSS vis-à-vis du code HTML auquel il s’applique.

L’approche orientée composants est l’exacte opposée : c’est le code HTML qui va dépendre du CSS. Elle permet de réutiliser une feuille de style dans d’autres projets.

Cette approche est adoptée par les nouveaux frameworks tels que

- React,
- Angular,
- Vue
- etc.
