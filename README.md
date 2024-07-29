# Site Arcadia Zoo
## Environnement de travail

- PC Windows10
- Visual Studio Code
- Composer version 2.6.6
- PHP 8.3
- Symfony7
- Symfony CLI 5.8.11
- Bootstrap 5.3
  
## Installation de Symfony7
On a plusieurs manières d'installer Symfony7, j'ai choisi la manière plus simple via composer.
```
composer create-project symfony/skeleton:"7.1.*" arcadiazoo
cd arcadiazoo
composer require webapp
```
Maintenant le projet "arcadiazoo" est créé, j'ouvre ce projet avec Visual Studio Code, puis afficher la page de bienvenue de Symfony7, j'ouvre le terminal puis lancer la commande :
```php
symfony server:start
```

pour afficher cette dernière.

![image](public/images/bienvenueSymfony.JPG)

La page de bienvenue de Symfony est bien affichée mais je voulais créer ma page d'accueil en utilisant le Framework de Bootstrap, pour ce faire je dois créer un contrôleur associé à cette page. On a plusieurs manières pour créer un contrôleur je vais utiliser la plus simple le terminal via maker-bundle, pour pouvoir l'utiliser il faut qu'il soit installé dans le système, je vais vérifier dans "composer.json" le maker-bundle est bien installé, je peux maintenant lancer la commande pour créer ce contrôleur.

![image](public/images/makerBundle.JPG)

```
php bin/console make:controller HomeController
```
Le contrôleur "HomeController" est crée dans "src/Controller/HomeController.php" et dans "template/home/index.html.twig" je vais modifier le code de cette page pour faire la page d'accueil de mon projet, je vais d'abord intégrer le Framework de Bootstrap en même occasion j'intègre aussi Bootstrap-icons dans mon projet, je me rend à la documentation de Bootstrap, copier le lien via CDN et coller dans fichier "base.html.twig" entre la balise ouvrante et fermante de "head" comme dans la capture d'écran ci-dessous.

![](public/images/intégrerBootstrap.JPG)

Et le script je l'ai collé avant la balise fermante de body.

![](public/images/scriptBootstrap.JPG)

Avant de commencer à coder ma page d'accueil il me reste une chose important à faire, par rapport à la palette de couleur que j'ai défini dans Charte Graphique de "Figma".  

[Charte Graphique](https://www.figma.com/design/u9WRTomub3dcGjSojmiRNO/Arcadia-Zoo?node-id=18-4&t=y9DscXB5wf2WZbbh-0).  

Pour pouvoir l'utiliser je dois ajouter sass pour Symfony dans mon projet, pour compiler mes fichiers scss j'installe une extension "Live Sass Compiler" sur mon éditeur de texte Visual Studio Code, une fois installé j'ai un bouton "Watch Sass" sur la "Status Bar" qui se trouve en bas de l'éditeur, je dois cliquer sur ce bouton si je veux compiler mes fichiers.

![](public/images/StatusBar.JPG)

Installation sass (le bundle) pour Symfony je lance la commande :  
```php
  composer require symfonycasts/sass-bundle
```
Usage :   
Dans le répertoire "assets/styles" je créé un fichier "app.scss" et son contenu le style de base puis je clique sur le bouton "Watch Sass" qui se trouve sur la barre de status pour générer le fichier "app.scss"
```scss
/* assets/styles/app.scss */

$red: #fc030b;

body {
  background: $red;
}
```  
J'ai maintenant le fichier "app.scss" qui est géneré en "app.css"  

```css
/* assets/styles/app.css */

body {
  background: #fc030b;
}/*# sourceMappingURL=app.css.map */  
```
Ensuite, dans le répertoire "templates/base.html.twig" je créé un lien dans la bolck stylsheets.

```twig  
{# templates/base.html.twig #}

{% block stylesheets %}
    <link rel="stylesheet" href="{{ asset('styles/app.scss') }}">
{% endblock %}

```  
J'actualise la page pour tester.  

![](public/images/pageDeTest.JPG)  

Le fichier "scss" fonctionne bien, je peux maintenant commencer à coder ma page d'accueil, je reviens sur ma "Charte Graphique" sur Figma et copie les codes de couleurs que j'ai défini quatre couleurs "Primary, Secondary, Dark et Blue" et aller mettre sur "app.scss".

[Charte Graphique](https://www.figma.com/design/u9WRTomub3dcGjSojmiRNO/Arcadia-Zoo?node-id=18-4&t=pa22WYHkynkYqYpd-0)  

```scss
/* assets/styles/app.scss */

$primary: #088A29;
$secondary: #0B6121;
$dark: #0B3B17;
$blue: #08088A;

body {
    background: #FFF;
}
```  


 












