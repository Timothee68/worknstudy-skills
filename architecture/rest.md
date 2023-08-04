# REST API

✔️ Auto validation par l'étudiant

🎓 J'ai compris et je peux expliquer

les verbes HTTP ✔️ : Les verbes HTTP sont les méthodes utilisées dans les requêtes HTTP pour spécifier l'action que l'on souhaite effectuer sur une ressource. Les principaux verbes HTTP sont GET (pour récupérer des données), POST (pour créer de nouvelles données), PUT (pour mettre à jour des données existantes), DELETE (pour supprimer des données) et PATCH (pour mettre à jour partiellement des données).

les statuts HTTP ✔️ : Les statuts HTTP sont des codes numériques renvoyés par le serveur en réponse à une requête HTTP. Ils indiquent le résultat de la requête et permettent au client de savoir si la requête a été traitée avec succès ou s'il y a eu une erreur. Par exemple, le code 200 indique que la requête a été traitée avec succès, le code 404 indique que la ressource demandée n'a pas été trouvée, le code 500 indique une erreur interne du serveur, etc.

les endpoints ✔️ : Les endpoints sont les URL spécifiques auxquelles les requêtes HTTP sont envoyées pour interagir avec une API. Chaque endpoint correspond à une action spécifique sur une ressource, telle que récupérer des données, créer une nouvelle ressource, mettre à jour des données, etc.

CORS ✔️ : CORS (Cross-Origin Resource Sharing) est un mécanisme de sécurité mis en place par les navigateurs pour empêcher les requêtes HTTP d'être effectuées depuis un domaine différent de celui de l'application web. Cela permet de limiter les risques de sécurité en empêchant les requêtes non autorisées depuis des sources externes.

la nomenclature recommandée pour les routes ✔️ : La nomenclature recommandée pour les routes d'une API suit généralement des conventions de nommage claires et cohérentes. Par exemple, pour récupérer une liste d'utilisateurs, l'endpoint pourrait être /users, pour récupérer un utilisateur spécifique, l'endpoint pourrait être /users/:id, pour créer un nouvel utilisateur, l'endpoint pourrait être /users, etc. Il est important d'utiliser des noms descriptifs et compréhensibles pour les routes afin de rendre l'API facile à utiliser et à comprendre.

## 💻 J'utilise

### Un exemple personnel commenté ✔️
// Importation des modules nécessaires
import { Request, Response } from 'express';
import bcrypt from 'bcrypt';
import UserModel from './models/UserModel'; // Supposons que UserModel est un modèle de base de données pour les utilisateurs
import { Error401 } from './errors'; // Supposons qu'Error401 est une classe personnalisée pour les erreurs 401

// Fonction de connexion
async function login(req: Request<any, Response, User>, res: Response): Promise<Response> {
  try {
    // Récupération du pseudo et du mot de passe depuis le corps de la requête
    const { pseudo, password } = req.body;

    // Recherche de l'utilisateur dans la base de données en fonction du pseudo
    const user = await UserModel.findUser({ pseudo: pseudo });

    // Vérification si l'utilisateur existe dans la base de données
    if (!user) {
      throw new Error401('Incorrect pseudo or password');
    }

    // Vérification si le mot de passe fourni correspond au mot de passe de l'utilisateur dans la base de données
    const isPasswordOK = await bcrypt.compare(password, user.password);

    // Si le mot de passe est incorrect, lance une erreur 401 (Unauthorized)
    if (!isPasswordOK) {
      throw new Error401('Incorrect pseudo or password');
    }

    // Génération d'un token d'authentification en utilisant les informations de l'utilisateur et l'adresse IP de la requête
    const token = generateToken({ ...user, ip: req.ip });

    // Renvoie une réponse JSON contenant le token d'authentification, le pseudo de l'utilisateur et l'ID de l'utilisateur
    return res.status(200).json({ token, pseudo: user.pseudo, id: user.id });
  } catch (error) {
    // En cas d'erreur, renvoie une réponse avec un code HTTP 401 (Unauthorized) et un message d'erreur
    return res.status(401).json({ error: error.message });
  }
}

// Autres fonctions/utilitaires nécessaires

// Supposons que generateToken est une fonction qui génère un token d'authentification en utilisant les informations fournies
function generateToken(userData: any): string {
  // Implémentation de la génération de token (à définir)
  // ...
  // Supposons que la fonction renvoie une chaîne représentant le token d'authentification
  return 'sampleAuthToken';
}

// Exportation de la fonction de connexion
export default login;


router
  .route('/login')
  /**
   * POST /users/login
   * @summary Authenticate a user
   * @return {string} JSON Web Token - 200 - Success response - application/json
   * @return {ApiError} 400 - Bad request response - application/json
   * @return {ApiError} 401 - Incorrect pseudo or password response - application/json
   */
  .post(validate('body', loginSchema), wrapper(controller.login));
router.route('/login'): Définit une route pour l'endpoint /login qui gère les requêtes HTTP pour l'authentification d'un utilisateur.

POST /users/login: Description de l'endpoint. Il indique qu'il s'agit d'une requête POST sur l'endpoint /users/login.

@summary Authenticate a user: Résumé de l'endpoint, indiquant qu'il s'agit de l'authentification d'un utilisateur.

@return {string} JSON Web Token - 200 - Success response - application/json: Indique que la réponse attendue pour une requête réussie est un JSON Web Token (JWT) avec un code HTTP 200 (Success) et un type de contenu application/json.

@return {ApiError} 400 - Bad request response - application/json: Indique qu'en cas de requête malformée (erreur 400), une réponse de type ApiError en format JSON est retournée avec un code HTTP 400 (Bad Request) et un type de contenu application/json.

@return {ApiError} 401 - Incorrect pseudo or password response - application/json: Indique qu'en cas d'échec de l'authentification en raison d'un pseudo ou d'un mot de passe incorrect, une réponse de type ApiError en format JSON est retournée avec un code HTTP 401 (Unauthorized) et un type de contenu application/json.

.post(validate('body', loginSchema), wrapper(controller.login)): Définit que cette route gère les requêtes POST et spécifie deux middlewares à exécuter avant d'appeler le contrôleur de l'authentification :

validate('body', loginSchema): Un middleware qui valide le corps de la requête en utilisant le schéma loginSchema. Cela garantit que les données requises (pseudo et mot de passe) sont présentes dans le corps de la requête et qu'elles sont conformes au schéma défini.

wrapper(controller.login): Un middleware qui enveloppe la fonction de contrôleur login dans un gestionnaire d'erreurs global. Cela permet de capturer les erreurs potentielles dans le contrôleur et de les gérer uniformément au niveau de l'application.

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
