# Configuration Docker pour Symfony avec phpMyAdmin et MailHog

Cette configuration Docker permet de démarrer rapidement un environnement de développement pour un projet Symfony, incluant une base de données MySQL, phpMyAdmin, et un service de faux emails (MailHog).

## Fichiers nécessaires
- compose.yaml
- Dockerfile
- nginx.conf

## Utilisation
- Placez ces fichiers à la racine de votre projet Symfony.
- Lancez les conteneurs : docker compose -f compose.yaml up -d
- Accéder au shell du conteneur PHP : docker compose exec php bash
- Installer Symfony : composer create-project symfony/skeleton:"7.1.*" .
- Si besoin d'installer la version web app : composer require webapp
