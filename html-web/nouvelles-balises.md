Utilisez les « nouvelles » balises de HTML5
===========================================

## Limitez votre usage de `div` et `span`

HTML5 dispose de nombreuses balises supplémentaires avec une sémantique forte. Cependant beaucoup d’intégrateurs continuent d’utiliser des `<div class="">` ou des `<span class="">`.

`Div` et `span` n’ont aucune valeur sémantique hormis que `div` est un bloc et `span` est du texte en-ligne.

## Connaissez les « nouvelles » balises

Balises de regroupement / mise en page :

- `<article>` contenu autonome et indépendant,
- `<aside>`	contenu mis sur le côté,
- `<footer>` pied de page d’un document ou d’un article,
- `<header>` introduction, en-tête ou groupe d’éléments de navigation,
- `<nav>` menu, liens de navigation
- `<section>` section dans un document,

Ces balises fonctionnent exactement comme `<div>` (pas de marge interne/externe, pas de bordure, taille de caractère inchangée…) sauf qu’elles sont sémantiquement marquées.

L’inconvénient de ces balises est qu’il n’est pas facile de savoir comment les imbriquer. L’article [HTML5 : Nouveaux éléments de section, article, header, footer, aside, nav](https://www.alsacreations.com/article/lire/1376-html5-section-article-nav-header-footer-aside.html) d’Alsacréations répond à cette question.

Balises 

- `<details>`, `<summary>` bloc collapsible
- `<figure>`, `<figcaption>` illustration, diagramme, photo, liste de codes…
- `<mark>` surlignage,
- `<meter>`	Définit une mesure scalaire dans une gamme connue (une jauge)
- `<progress>` barre de progression,
- `<time>` date / heure,
- `<wbr>` placée à l’intérieur d’un mot elle indique au navigateur l’endroit au ce mot peut être scindé au besoin.

## N’utilisez plus les balises obsolètes

Elles étaient déjà peu utilisées mais mieux vaut prévenir que guérir.

Votre code HTML ne doit pas contenir les balises suivantes : 

`<acronym>`, `<applet>`, `<basefont>`, `<bgsound>`, `<big>`, `<blink>`, `<center>`, `<command>`, `<dir>`, `<font>`, `<frame>`, `<frameset>`, `<hgroup>`, `<isindex>`, `<listing>`, `<marquee>`, `<multicol>`, `<nextid>`, `<nobr>`, `<noembed>`, `<noframes>`, `<plaintext>`, `<spacer>`, `<strike>`, `<tt>` et `<xmp>`.