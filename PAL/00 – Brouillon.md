Le HTML - généralités

• Hypertext Markup Language (HTML)
• Langage de balises qui permet de structurer des pages
• Différentes versions depuis 1989
• Aujourd’hui :
– XHTML (2000 – 2006)
– HTML5

• W3C : World Wide Web Consortium (1994)
– TBLee, fondateur du W3C et inventeur du HTML
– Chargé de promouvoir la compatibilité des technologies dans les navigateurs
– 378 entreprises membres qui peuvent faire des propositions
(Microsoft, Apple, Mozilla, Opera, Adobe, etc.)
– Proposent un validateur http://validator.w3.org/

• WHATWG : Web Hypertext Application Technology Working Group (2004)
– Collaboration non officielle de développeurs de navigateurs
– Tentative de réponse à la lenteur des standards du W3C
– Mozilla Foundation, Opera, Apple, etc.

Blocnote ou TextEdit, si vous n’avez rien d’autre sous la main :

• Pas de coloration syntaxique
• Nécessite de connaître tout le langage

La syntaxe HTML : balises, éléments et attributs

Le principe de balise

• Les balises structurent le contenu de la page (texte, images, etc.)
• Chaque balise a un rôle et donne du sens au contenu présenté

• On peut imbriquer les balises (on y reviendra) les unes dans les autres

<p>	Hooo un bloc  !! </p>
<div>
<p>	Et un joli paragraphe </p>

<p> Et autre un joli paragraphe </p> </div>

Touche < du clavier pour ouvrir :

Touche maj + < pour fermer : >

• Le nom des balises est prédéfini dans les spécifications HTML, on ne peut donc PAS en inventer !
• Quelques exemples : <html>, <body>, <img>, <p>, <div>, <a>, etc.

• Par convention et pour faciliter la lecture du code, toute balise ouverte doit être fermée (sauf exception).
• Certaines balises bien particulières n’ont pas besoin d’être fermées, on les dit « auto-fermantes » , elles n’ont ni contenu ni balise fermante.
• Note : je mets le / final par convention, mais pas obligatoire.

<img  src="monimage.png"/>

\## Qu'est-ce qu'un fichier Markdown ?

## La syntaxe HTML

\### Titres

\### Paragraphes

Attributs et valeurs

• Certaines balises peuvent être complétées par des attributs précisant certains paramètres (l'adresse des liens, source d'une image à afficher, etc)
• Une balise peut contenir plusieurs attributs

● Les attributs sont des éléments prédéfinis dans le HTML on ne peut en « inventer »
● Un peut les mettre entre simple quote, double quote ou rien. Par convention nous choisissons les doubles quotes "

<div id="kittens"> // <div id=kittens>"Les

attributs sont toujours dans la balise ouvrante

● src=" " : donner la source (d’une image par exemple)
– <img src="monimage.png" width="400" height="250" alt="image de chatons" />

● href=" " : donner la destination d’un lien
– <a href="http://www.google.fr"> Texte du lien </a>

● id=" " : donner un identifiant à l’élément que l’on pourra utiliser en CSS.
Les Ids doivent être uniques par page
– <p id="monid"> contenu </p>

● class=" " : donner une classe à l’élément que l’on pourra utiliser en CSS.
Les classes peuvent être dupliquées sur la page
– <p class="maclasse"> contenu </p>

Doctype, html, body : structure d'un document valide

Structure d’un document HTML simplifié
Décomposons balise par balise !

La notion de doctype

• Permet au navigateur de savoir quelle version de HTML (ou XHTML) est utilisée sur la page
• Obligatoire pour valider une page (validateur W3C)
• Pas de doctype = « Quirks » mode : le navigateur fait ce qu’il peut avec ce qu’il trouve, en mode rétro-compatibilité => peut expliquer certains bugs sur IE

<!doctype html>

Le doctype HTML5
• Plus simple , plus concis
• «Future proof» : autant commencer aujourd’hui !
• <!doctype html>
• Vous pourrez utiliser des éléments HTML5 qui sont finalisés

La balise <html>

• Tout document HTML commence par la balise <html> qui se ferme en fin de document : </html>
• La balise <html> contient nécessairement deux balises définissant l'entête (<head>) et le corps (<body>) du document.

L'attribut lang

• Permet de spécifier la langue de traitement du document global
– Indexation dans la bonne langue par les moteurs de recherche
– Synthèse vocale
– Vérification orthographique des formulaires

<html lang="fr">

La balise <head>

Détermine l’entête du document et contient les méta-informations

La balise <title>

• On y trouve la balise <title> qui sera le titre du document
– Sert en référencement (repris dans les résultats de recherche)

– Affichée dans l’onglet du navigateur

La balise <head> : les balises meta

• On y ajoutera également les appels pour les feuilles de style CSS et certains JavaScripts
• On peut y trouver des balises « meta » parmi lesquelles
– <meta charset="UTF-8"/> : permet de définir l’encodage de caractère de la page (à mettre directement sous le <head>)

– <meta name="description" content="description pour le

référencement"/> affiché dans les résultats de recherche

La balise <body>

● Délimite le contenu de la page
● Le contenu est constitué de texte, images et autres éléments qui seront affichés

En résumé

<!doctype html> <html lang="fr"> <head>
  <meta charset="UTF-8">
<title> Titre de ma page </title>
  </head>
<body>
Contenu de la page
</body>
</html>

C’est valide !

La validation reste un outil et non une fin en soi, mais un code non valide a des chances de poser des soucis plus tard
