# 0. Environnement et Plan de travail
Nous allons nous assurer d'avoir le parfait environnement de travail pour coder proprement notre page Web.
### Éditeur de Texte + Navigateur Web
1. Installez l'éditeur de texte : [Atom](https://atom.io/) (éditeur de texte pour développeurs).
2. Ouvrez l'éditeur et allez psonnaliser deux petits paramètres de l'application : Menu "Atom" > "Parameters" (ou Settings sur PC) > "Editor" > Cochez les options "Show Indent Guide" & "Show Invisibles".(ceci va nous aider à indenter proprement : cf. suite). Fermez ensuite tous les onglets présents de façon à avoir :
3. Récupérez le dossier "landing" avec les images et le présent pdf. Glissez/déposez le dossier dans l'éditeur de texte. (#DragAndDrop)
4. Sur l'arbre de navigation de gauche, dans le dossier "landing":
    - clic droit : New file. Le sauvegarder sous le nom `index.html`.
    - faire la même chose pour `style.css`.
5. Sur le Finder, double cliquez sur le fichier `index.html` : le fichier s'ouvre automatiquement sur votre navigateur par défaut. Cf :
![Image of Finder](images-instructions/finder.png)
6. Pour faciliter les choses pour la suite : partagez votre plan de travail en deux : éditeur de texte à gauche et navigateur à droite. Cf :
![Image of Plan de travail](images-instructions/plan_travail.png)
7. Votre plan de travail de parfait développeur est là : vous êtes prêts pour la suite !

# 1. Construisons et structurons notre page HTML !
* Dans votre document `"index.html"`, tapez `html` et taper sur la touche `Tab` de votre clavier (Raccourci clavier suite à la suggestion d'Atom)
* Que de temps gagné ! Comme par miracle, tout le squelette standard d'une page HTML apparaît :
    - la doctype de votre document : `<!DOCTYPE html>`
    - les balises `<html>`, `<head>` et `<body>`
    - les balises `<meta charset="UTF-8">` (pour les caractères spéciaux) et `<title>` dans le `<head>`


* Les balises d'une page HTML peuvent être pensées comme des poupées russes : ```<title>``` est dans le ```<head>``` qui est lui-même dans le ```<html>```. Pour bien visualiser cette image de poupées russes, on fera attention à indenter proprement le code afin d'avoir un code lisible rapidement. Une indentation se fait avec `Tab` (ce qui correspond à deux espaces)

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1> </h1>
    <p> </p>
  </body>
</html>
```
au lieu de

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title></title>
</head>
<body>
<h1> </h1>
<p> </p>
</body>
</html>
```

* Attention : une balise qui est ouverte à l'intérieur d'une autre balise doit être fermée à l'intérieur. Il faut faire attention à ce que les balises ne s'entremêlent pas !

* Copiez collez le contenu ci-dessous dans le `<body>` :

```html
<!-- Texte à copier-coller dans le body et à mettre en forme -->
MuffinMe - Savourez votre muffin, maintenant !

Savourez les meilleurs muffins

Maintenant, tout de suite

Commandez


Les meilleurs muffins ...
Choisissez parmi nos 1000 muffins préparés avec passion par les meilleurs chefs pâtissiers de Paris !

Livrés chez vous ...
L'application vous géolocalise automatiquement et vous indique le temps d'attente estimé !

En moins de 30 min ...
Un livreur vous apporte dans les 30 mins vos muffins à peine sortis du four et prêts à être dégustés !

Payés avec votre moyen de paiement préféré !
Nous prenons tous les services de paiement possibles : liquide, cartes bancaires, chèques, bitcoins, etc.


Suivez-nous sur les réseaux sociaux :
Facebook
Twitter
Instagram
Youtube

Contact · MuffinMe est une compagnie fictive 2017
```

* En sauvegardant le fichier HTML (le point bleu disparait), rechargez la page de votre navigateur, vous devriez avoir :

![Contenu brut](images-instructions/contenu_brut.png)
* Replacez bien le titre de la page entre les balises `title` pour avoir :

![Contenu brut](images-instructions/contenu_brut_title.png)
* Structurez le tout avec les balises `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>, <p>, <ul> & <li>` (/!\ Ne pas oublier les balises fermantes à chaque fois !) pour avoir :

![Contenu brut](images-instructions/contenu_balisé.png)

* Ajoutez y les liens (balise `<a>` avec l'attribut `href` pour spécifier l'URL du lien) afin d'être redirigé vers le réseau social approprié en cliquant dessus. (à noter si vous rajouter l'attribut facultatif `target="_blank"`, la page s'ouvrira dans un nouvel onglet.)
```html
<!-- Code à copier-coller au bon endroit -->
<a href="https://www.facebook.com/muffinme" target="_blank"> Facebook </a>
<a href="https://www.twitter.com/muffinme"> Twitter </a>
<a href="https://www.instagram.com/muffinme"> Instagram </a>
<a href="https://youtube.com/muffinme"> Youtube </a>
```
* Ajoutez y les images/icônes au dessus de chaque caractéristique : balise orpheline `<img>` (/!\ exception : pas de balise fermante `</img>`!!) avec l'attribut `src` pour signifier la source et indiquer où se trouve l'image que l'on veut insérer et `alt` pour spécifier le texte alternatif affiché si mauvais téléchargement de l'image et qui est important pour le référencement


```html
<!-- Code à copier-coller au bon endroit -->
<img src="images/muffin.png" alt="Muffin au chocolat" width="35">
<img src="images/geolocalization.png" alt="Géolicalisation pour livraison à domicile" width="35">
<img src="images/delivery.png" alt="Livraison rapide" width="35">
<img src="images/payment.png" alt="Paiments divers possibles" width="35">
```
A ce stade, on est parvenu à une page Web structurée et lisible bien qu'un peu archaïque. En fait, les premières pages Web ressemblaient à ça et en particulier celles du [premier site Web](http://info.cern.ch/hypertext/WWW/TheProject.html) . Vous êtes donc au niveau des meilleurs chercheurs scientifiques du monde ... des années 90 !

![Contenu brut](images-instructions/contenu_balisé_liens_images.png)

# 2. Stylisons notre page avec le CSS !

Evidemment les pages Web d'aujourd'hui ne ressemblent pas à ça grâce au CSS qui permet de styliser les différents élements de la page HTML et d'avoir des pages beaucoup plus agréables à consulter !


## 2.1. Importons notre feuille de style CSS dans notre feuille HTML

Relions le fichier CSS (`style.css` créé au début) à la page HTML (`index.html`) dans le `<head>` grâce a la balise `<link>`.
```html
<!-- Code à copier-coller au bon endroit -->

<head>
  [...]
  <link href='style.css' rel='stylesheet'>
</head>
```

## 2.2. Couleurs et polices changées
Complétons notre feuille de style maintenant qu'elle est reliée au fichier HTML.

```css
/*Code à copier-coller au bon endroit*/

body {
  color: #555;
  text-align: center;
}

h4 {
  color: black
}
```

Rajoutons des polices plus sympathiques que le Times New Roman. Pour éviter la situation où le client ne va pas visualiser la bonne police de la page Web (faute de l'avoir installée sur son ordinateur si la police souhaitée est disons exotique!), on va pré-télécharger dans le `<head>` grâce au service Google Font les polices que nous allons utiliser dans notre feuille de style : comme ça tout le monde visualisera la page avec les bonnes polices quelquesoit son ordinateur !
```html
<!-- Code à copier-coller au bon endroit -->

<head>
  [...]
  <link href="https://fonts.googleapis.com/css?family=Montserrat|Open+Sans:300,400,700" rel="stylesheet">
  <link href='style.css' rel='stylesheet'>
</head>
```
avant de les spécifier dans la feuille de style.
```css
/*Code à copier-coller au bon endroit*/

body {
  font-family: "Open Sans", sans-serif;
  color: #555;
  text-align: center;
}

h1, h2, h3, h4 {
  font-family: "Montserrat", sans-serif;
}

h4 {
  color: black
}
```

## 2.3 Structurons notre page avec des div

En fait, les éléments balisés d'une page Web sont rassemblés dans des blocs eux-mêmes balisés : on pousse encore plus loin l'image des "poupées russes". Ainsi, la page d'accueil d'Apple est constituée de blocs dans lesquels il y a d'autres sous-blocs où on retrouve des sous-sous-blocs ...(ainsi de suite)... jusqu'à ce qu'on trouve les balises HTML traditionnelles (`h1, p, a, ul, li...`) :
Pour baliser un bloc, on utilise les balises  ```<div class="">``` (ouvrante) et ```</div>``` (fermante).

On remarque l'attribut facultatif ```class="nom_de_classe_du_bloc"``` de la balise ouvrante qui va servir de selecteur dans le `.css` auquel on va attribuer des règles de styles qui s'appliqueront à tout les div de classe `"nom_de_classe_du_bloc"`.

On va baliser notre page de la façon suivante avec 6 div associées à 3 classes différentes :


```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title> MuffinMe - Savourez votre muffin, maintenant !</title>
    <link href="https://fonts.googleapis.com/css?family=Montserrat|Open+Sans:300,400,700" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
  </head>
  <body>

    <div class="wrapper">
      <!-- code HTML du haut de page -->
    </div>

    <div class="asset">
      <!-- code HTML de la 1ère caractéristique du service MuffinMe-->
    </div>

    <div class="asset">
      <!-- code HTML de la 2ème caractéristique du service MuffinMe-->
    </div>

    <div class="asset">
      <!-- code HTML de la 3ème caractéristique du service MuffinMe-->
    </div>

    <div class="asset">
      <!-- code HTML de la 4ème caractéristique du service MuffinMe-->
    </div>

    <div class="footer">
      <!-- code HTML du bas de page-->
    </div>
  </body>
</html>

```

## 2.3. Ajoutez Fontawesome
On va prétélécharger dans le `head` une bibliothèque d'icônes [Fontawesome](http://fontawesome.io/icons/)

Le `head` de notre page HTML devient donc :
```html

<!-- s'assurer que votre head correspond à celui-ci en copiant collant le code -->
<head>
  <meta charset="utf-8">
  <title> MuffinMe - Savourez votre muffin, maintenant !</title>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css">
  <link href="https://fonts.googleapis.com/css?family=Montserrat|Open+Sans:300,400,700" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
```
Aussi, on va remplacer le nom de chaque réseau social par l'icône associée avec les balises ``` <i class=""></i>```
```html
<div class="footer">
  <ul>
    <li>
      <a href="https://twitter.com/iceme">
        <i class="fa fa-twitter"></i>
      </a>
    </li>
    <li>
      <a href="https://facebook.com/iceme">
        <i class="fa fa-facebook"></i>
      </a>
    </li>
    <li>
      <a href="https://instagram.com/iceme">
        <i class="fa fa-instagram"></i>
      </a>
    </li>
    <li>
      <a href="https://youtube.com/iceme">
        <i class="fa fa-youtube"></i>
      </a>
    </li>
  </ul>
</div>
```

## 2.4 Bootstrap
On va prétélécharger dans le head un framework CSS [Bootstrap](http://getbootstrap.com/css/) clé en main qui a été developpée par Twitter et dont on va utiliser les classes de CSS préfabriquées sans les écrire dans notre feuille de style .css . On va gagner un petit peu de temps !

On va donc utiliser la class list-inline de Bootstrap pour rendre la liste horizontale et enlever les puces, et ajouter une classe "social" que l'on codera après dans notre feuille de style .css .

```html
<div class="footer">
  <ul class="list-inline social">
```
Aussi copiez-collez dans style.css les selecteurs correspondant aux classes (attention au point précisant qu'on selectionne une classe et pas une balise traditionnelle)  :

```css
.footer {
  text-align: center;
	background-color: #333;
	color: #aaaaaa;
	padding-top: 30px;
  padding-bottom: 20px;
  margin-top: 40px;
}
.footer a {
	color: #aaaaaa;
}

.footer a:hover {
	color: #dddddd;
}
.social a  {
	font-size: 24px;
}
```

Aussi, on va utiliser le bouton Bootstrap pour avoir le CallToAction "Commandez". Pour cela on transforme notre titre h2 en bouton avec un style spécifique de notre framework CSS
```html
<button type="button" class="btn btn-primary btn-lg">Commandez</button>
```

## 2.5 Fignoler le css

```css
/*règles de style concernant le haut de page*/
.wrapper {
	background-image: linear-gradient(-225deg, rgba(0,101,168,0.6) 0%, rgba(0,36,61,0.6) 50%), url("images/muffins1.jpg");
  background-size: cover;
  height: 550px;
  color:white;
	text-align: center;
	padding-top: 150px;
  margin-bottom: 50px;
}

.wrapper h1 {
	font-size: 72px;
}

.wrapper h2 {
	font-size: 18px;
	margin-bottom: 1em;
}

/*règles de style concernant les 4 assets de MuffinMe */

.asset {
  text-align: center;
  margin-bottom: 50px;
}

.asset p {
	font-weight: 300;
	letter-spacing: 1px;
}

.asset img {
	margin-bottom: 10px;
}
```

La page commence à être sympathique !


**_Pour aller plus loin :_**
- Liste des balises HTML https://developer.mozilla.org/fr/docs/Web/HTML/Element
- Liste des propriétés CSS https://developer.mozilla.org/fr/docs/Web/CSS/Reference
- Web Design in 4 minutes : http://jgthms.com/web-design-in-4-minutes/
- Leanr more about HTML/CSS : http://marksheet.io/


## BONUS : lier la page d'accueil à une page de contact

Dupliquez la page index.html et la nommer contact.html .

Supprimer les div class="asset" et ajouter une div class="contact" dans lequel vous copiez-collez le texte ci-dessous et le mettez en forme comme vous le souhaitez avec les balises h4, p, etc.

```html
<!-- Texte à copier coller dans la page contact.html -->

Contactez-nous !
5 Rue du Chocolat 75000 Paris

Tél : 01 00 00 00 00

Email : contact@muffinme.com
```

Enfin, pour naviguer entre les deux pages, rajoutez un lien href dans le bas de page :

```html
<!-- code HTML à copier-coller en bas de page de index.html -->
<p>
  <a href="contact.html"> Contact </a>
  · MuffinMe est une compagnie fictive 2017
</p>
```

```html
<!-- code HTML à copier-coller en bas de page de contact.html -->
<p>
  <a href="index.html"> Accueil </a>
  · MuffinMe est une compagnie fictive 2017
</p>
```

Ca y est ! Vous pouvez naviguer entre les différentes pages Web statiques de votre site Web MuffinMe ! ;)

## BONUS 2 : rendre la page Responsive

Nous allons souhaitez créer une grille responsive avec Bootstrap qui va dépendre de la largeur de la page
