# Docker
🎓 J'ai compris et je peux expliquer
En ce qui concerne Docker et Docker Compose, j'ai acquis plusieurs compétences :

La création d'une image Docker : Je sais comment créer une image Docker pour mon application en utilisant un fichier Dockerfile. J'ai compris les différentes étapes impliquées dans le processus de création de l'image, telles que l'installation des dépendances, la copie des fichiers nécessaires, et la définition de l'environnement d'exécution.

L'exécution d'un conteneur : J'ai appris à exécuter un conteneur à partir d'une image Docker en utilisant la commande docker run. Je sais comment spécifier les options et les paramètres nécessaires pour démarrer le conteneur avec les bonnes configurations.

L'orchestration de conteneurs avec Docker Compose : J'ai compris comment utiliser Docker Compose pour orchestrer plusieurs conteneurs en même temps. J'ai appris à définir les services dans le fichier docker-compose.yml, à spécifier les dépendances entre les services, et à démarrer l'ensemble des services en utilisant la commande docker-compose up.

💻 J'utilise
Un exemple personnel commenté ✔️
J'ai récemment travaillé sur un projet où j'ai utilisé Docker pour faciliter le déploiement de mon application. J'ai créé un fichier Dockerfile pour définir les étapes nécessaires à la création de l'image Docker. J'ai ensuite utilisé la commande docker build pour construire l'image à partir de ce Dockerfile.

Une fois l'image créée, j'ai utilisé la commande docker run pour exécuter un conteneur basé sur cette image. J'ai spécifié les options nécessaires, telles que les ports à exposer, les volumes à monter, et les variables d'environnement à définir.

Ensuite, j'ai découvert Docker Compose pour orchestrer plusieurs conteneurs de manière plus simple. J'ai créé un fichier docker-compose.yml dans lequel j'ai défini les services pour chaque conteneur nécessaire à mon application. J'ai également spécifié les dépendances entre les services, afin que Docker Compose puisse démarrer les conteneurs dans le bon ordre.

J'ai utilisé la commande docker-compose up pour lancer tous les services en même temps. Cela m'a permis de démarrer rapidement mon application avec toutes ses dépendances, sans avoir à exécuter chaque conteneur individuellement.

Utilisation dans un projet ✔️
# Utiliser l'image Node.js LTS Alpine comme base
FROM node:lts-alpine

# Installer les dépendances nécessaires pour la construction des paquets Node natifs
RUN apk add make g++ python3 git

# Installer le package node-pre-gyp globalement pour la construction des paquets binaires Node
RUN npm i -g node-pre-gyp

# Définir le répertoire de travail à /app
WORKDIR /app

# Copier les fichiers package.json et package-lock.json dans le répertoire de travail
COPY package.json package.json
COPY package-lock.json package-lock.json

# Installer les dépendances du projet en utilisant npm
RUN npm install

# Copier le fichier tsconfig.json dans le répertoire de travail
COPY tsconfig.json tsconfig.json

# Copier le répertoire src dans le répertoire de travail
COPY src src

# Définir la commande par défaut pour exécuter l'application lors du démarrage du conteneur
CMD npm start
## DOCKER COMPOSE EXEMPLE 
services:
  backend: # Service backend
    build: ./back # Construction du service à partir du répertoire ./back
    ports:
      - 4000:4000 # Exposer le port 4000 du conteneur sur le port 4000 de l'hôte
    volumes:
      - ./back/src:/app/src # Monter le répertoire ./back/src dans le répertoire /app/src du conteneur

  frontend: # Service frontend
    build: ./front # Construction du service à partir du répertoire ./front
    ports:
      - 3000:3000 # Exposer le port 3000 du conteneur sur le port 3000 de l'hôte
    volumes:
      - ./front/src:/app/src # Monter le répertoire ./front/src dans le répertoire /app/src du conteneur

  db: # Service db (base de données PostgreSQL)
    image: postgres # Utiliser l'image Docker PostgreSQL
    restart: always # Redémarrer toujours le conteneur en cas d'échec
    environment:
      POSTGRES_PASSWORD: example # Définir la variable d'environnement POSTGRES_PASSWORD avec la valeur "example" pour définir le mot de passe de la base de données PostgreSQL

  adminer: # Service adminer (outil de gestion de bases de données)
    image: adminer # Utiliser l'image Docker Adminer
    restart: always # Redémarrer toujours le conteneur en cas d'échec
    ports:
      - 8080:8080 # Exposer le port 8080 du conteneur sur le port 8080 de l'hôte pour accéder à l'interface Adminer

Je continue d'utiliser Docker et Docker Compose dans mes projets actuels. Chaque fois que je développe une nouvelle application, je crée un fichier Dockerfile pour définir l'image Docker de mon application. Cela me permet de garder mon environnement de développement propre et de m'assurer que mon application fonctionnera de la même manière dans différents environnements.

J'utilise également Docker Compose pour orchestrer les conteneurs nécessaires à mon application. Cela facilite le processus de développement et de déploiement en regroupant tous les services nécessaires dans un seul fichier de configuration.

Utilisation en production si applicable ✔️
Dans certains projets, j'ai également utilisé Docker pour déployer mon application en production. J'ai créé une image Docker de mon application et l'ai déployée sur un serveur en utilisant Docker.

Docker m'a permis de gérer facilement les dépendances et les configurations de mon application, ce qui a simplifié le processus de déploiement. J'ai également pu utiliser Docker Compose pour orchestrer plusieurs conteneurs sur le serveur, facilitant ainsi le déploiement d'applications multi-services.

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
