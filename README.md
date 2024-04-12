# Docker Development Stack

Ce projet configure une pile de développement basée sur Docker, incluant Portainer, MariaDB, PHP et Caddy, conçue pour faciliter le développement et les tests d'applications web localement.

## Prérequis

Assurez-vous que Docker et Docker Compose sont installés sur votre machine :

- [Installer Docker](https://docs.docker.com/get-docker/)
- [Installer Docker Compose](https://docs.docker.com/compose/install/)

## Installation

Suivez ces étapes pour mettre en place votre environnement de développement :

### Étape 1 : Cloner le dépôt

```bash
git clone https://yourrepositoryurl.com/project.git
cd project
```

### Étape 2 : Build and run the containers
Démarrez tous les services en utilisant Docker Compose :
```bash
docker-compose up -d
```

### Étape 3 : Access the services
- 'Portainer:' http://localhost:9000 - Manage Docker containers.
- 'Caddy:' http://localhost - Access your PHP application.

### Étape 4 : Configuration

#### - Services
- 'portainer:' Interface utilisateur pour la gestion de Docker, fonctionnant sur le port 9000.
- 'mariadb:' Serveur de base de données MariaDB, accessible en interne.
- 'php:' Environnement PHP configuré avec les extensions nécessaires.
- 'caddy:' Serveur web Caddy qui distribue votre contenu PHP.



### Utilisation : 

#### Gestion de la base de données
Connectez-vous à MariaDB en utilisant les identifiants par défaut suivants :

- 'Hôte' : mariadb
- 'Nom d'utilisateur :' Admin
- 'Mot de passe :' rootpassword
- 'Base de données :' docker_tp

### Modifier PHP
Pour personnaliser l'environnement PHP, modifiez les paramètres dans le Dockerfile. Reconstruisez l'image avec :
```bash
docker-compose up -d
```


