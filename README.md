# Serveur Simple avec Docker

Ce projet consiste en la création d'un environnement de développement simple avec Nginx, PHP7 et MySQL.

## Composition

- /nginx : Correspond à la configuration des server blocks de Nginx
- /logs : dossier contenant les logs du serveur
- /public : dossier où mettre les projets

## Configuration

:warning: Lors de la première utilisation, il faut créer les fichier `nginx-access.log` et `nginx-error.log` dans le dossier /logs :warning:

Pour lancer le serveur à la première utilisation : `docker-compose up -d` (construit les containers)

Pour les fois d'après : `docker-compose start`

Le serveur est accessible via http://localhost

PhpMyAdmin est accessible via http://localhost:8183
Le nom du serveur MySQL est : mysql

Il est possible d'accéder au serveur mysql en ligne de commande en passant par docker : `docker-compose exec mysql sh`
On se connecte dans le bash via la commande suivante : `mysql -u root -p` en indiquant le mot de passe défini dans le docker-compose.yml
