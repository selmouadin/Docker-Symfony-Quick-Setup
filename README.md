# Configuration Docker pour Symfony avec phpMyAdmin et MailPit

Cette configuration Docker permet de démarrer rapidement un environnement de développement pour un projet Symfony, incluant une base de données MySQL, phpMyAdmin, et un service de faux emails (MailPit).

## Fichiers nécessaires
- compose.yaml
- Dockerfile
- nginx.conf

## Utilisation
- Placez ces fichiers à la racine de votre projet Symfony.
- Lancez les conteneurs : `docker compose -f compose.yaml up -d`
- Accéder au shell du conteneur PHP : `docker compose exec php bash`
- Installer Symfony : `composer create-project symfony/skeleton:"7.1.*" .`
- Si besoin d'installer la version web app : `composer require webapp`
- Editer le fichier .env pour activer l'accès à la bdd mysql et configurer le mailer ``` DATABASE_URL="mysql://symfony:symfony@database:3306/symfony?serverVersion=8.0&charset=utf8mb4" \n MAILER_DSN=smtp://mailpit:1025 ```

## Accédez à votre application
- Application Symfony : http://localhost:8080
- phpMyAdmin : http://localhost:8081
- MailPit : http://localhost:8025
