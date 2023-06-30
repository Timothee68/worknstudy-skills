# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple) ✔️
- 
- J'utilise nodemon pour bénéficier du livereloading lors du développement de mon application. Voici comment je l'utilise :

Tout d'abord, j'installe nodemon en utilisant la commande suivante dans mon terminal : npm install -g nodemon.

Ensuite, je peux exécuter mon application avec nodemon en utilisant la commande nodemon suivie du nom du fichier de démarrage de mon application. Par exemple, si mon fichier de démarrage est app.js, j'exécute la commande nodemon app.js.

À chaque fois que je modifie mon code source, nodemon détecte les changements et relance automatiquement mon application. Cela me permet d'économiser du temps en évitant de devoir redémarrer manuellement mon serveur à chaque modification.

- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple)  ✔️
- 
- Pour la connexion à une base de données, j'utilise MongoDB comme exemple, à la fois sans utiliser d'ORM/ODM et avec Mongoose.

Connexion sans ODM/ORM :
Sans utiliser Mongoose, j'utilise le pilote MongoDB officiel pour Node.js. Voici un exemple de code :

const MongoClient = require('mongodb').MongoClient;

const url = 'mongodb://localhost:27017';
const dbName = 'ma_base_de_donnees';

MongoClient.connect(url, function(err, client) {
  if (err) {
    console.error('Erreur de connexion à la base de données:', err);
    return;
  }

  const db = client.db(dbName);

  // Je peux effectuer des opérations sur la base de données ici...

  client.close();
});

Connexion avec Mongoose :
Mongoose est un ODM pour MongoDB qui simplifie l'interaction avec la base de données. Voici un exemple de code pour la connexion avec Mongoose :

const mongoose = require('mongoose');

const url = 'mongodb://localhost:27017/ma_base_de_donnees';

mongoose.connect(url, { useNewUrlParser: true, useUnifiedTopology: true })
  .then(() => {
    console.log('Connecté à la base de données MongoDB');
    // Je peux effectuer des opérations sur la base de données ici...
  })
  .catch((err) => {
    console.error('Erreur de connexion à la base de données:', err);
  });
  
En utilisant Mongoose, je peux définir des schémas et des modèles pour mes données, ce qui facilite la manipulation et la gestion des documents MongoDB.

- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple)  ✔️

Pour développer une API REST et une API GraphQL, j'utilise les packages express et graphql. Voici comment je les utilise :

API REST avec Express.js :
Express.js est un framework populaire pour la création d'API RESTful. Voici un exemple de code pour définir des routes avec Express :

const express = require('express');
const app = express();

// Définition des routes
app.get('/api/users', (req, res) => {
  // Logique de gestion de la requête GET /api/users
  res.json({ message: 'Récupération de tous les
  
- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ❌ / ✔️
- Le module fs est intégré à Node.js et permet de manipuler les fichiers système. Voici quelques exemples de manipulations courantes :
- const fs = require('fs');

fs.readFile('monFichier.txt', 'utf8', (err, data) => {
  if (err) {
    console.error('Erreur lors de la lecture du fichier :', err);
    return;
  }

  console.log('Contenu du fichier :', data);
});
###
const fs = require('fs');

const contenu = 'Contenu à écrire dans le fichier';

fs.writeFile('monFichier.txt', contenu, (err) => {
  if (err) {
    console.error('Erreur lors de l\'écriture dans le fichier :', err);
    return;
  }

  console.log('Fichier écrit avec succès');
});
###

const fs = require('fs');

fs.unlink('monFichier.txt', (err) => {
  if (err) {
    console.error('Erreur lors de la suppression du fichier :', err);
    return;
  }

  console.log('Fichier supprimé avec succès');
});

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

```javascript
// this function takes a path to a .md file of the host system and write the HTML version of this file
// the .html file is given back
const convertMDFileToHTML = (pathToMDfile) => /* ... path to HTML file */
```

### Utilisation dans un projet ❌ / ✔️

[lien github](...)

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

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
