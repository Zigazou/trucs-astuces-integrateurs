Organisez votre code HTML
=========================

Voici un squelette HTML5 minimum orienté mobile :

    <!doctype html>
    <html>
      <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, user-scalable=no">
        <title>Hello, World!</title>
        <link href="style.css" rel="stylesheet" media="screen">
      </head>
      <body>
        <p>Hello, World!</p>
        <script src="script.js"></script>
      </body>
    </html>

Notes :

- la balise `<meta charset="utf-8">` doit apparaître dans les 1024 premiers octets du code HTML [[Declaring character encodings in HTML](https://www.w3.org/International/questions/qa-html-encoding-declarations)],
- la balise `<meta name="viewport">` indique aux navigateurs mobiles que le contenu de la page est prévu pour eux
- les feuilles de styles sont indiquées de préférence le plus tôt possible dans le code,
- les scripts sont indiqués de préférence le plus tard possible dans le code.