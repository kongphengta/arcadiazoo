# Site Arcadia Zoo
## Environnement de travail

- PC Windows10
- Visual Studio Code
- Composer version 2.6.6
- PHP 8.3
- Symfony7
- Bootstrap 5.3
  
## Installation de Symfony7
On a plusieurs manières d'installer Symfony7, j'ai choisi la manière plus simple via composer.
```
composer create-project symfony/skeleton:"7.1.*" arcadiazoo
cd arcadiazoo
composer require webapp
```
Maintenant le projet "arcadiazoo" est créé, j'ouvre ce projet avec Visual Studio Code, puis afficher la page de bienvenue de Symfony7, j'ouvre le terminal puis lance la commande "symfony server:start"
pour afficher cette dernière.

![image](public/images/bienvenueSymfony.JPG)

La page de bienvenue de Symfony est bien affichée mais je voulais créer ma page d'accueil complète en utilisant le Framework Bootstrap, pour ce faire je dois créer un contrôleur associé à cette page. On a plusieurs manières pour créer un contrôleur je vais utiliser la plus simple le terminal via maker-bundle, pour pouvoir l'utiliser il faut qu'il soit installé je vais vérifier dans "composer.json".
![image](public/images/makerBundle.JPG)

```
php bin/console make:controller HomeController
```
