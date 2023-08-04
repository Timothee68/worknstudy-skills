Tester son application
✔️ Auto validation par l'étudiant

🎓 J'ai compris et je peux expliquer
En ce qui concerne les tests, je suis familier avec plusieurs concepts :

Les tests unitaires : Ce sont des tests visant à vérifier le bon fonctionnement d'une unité de code, généralement une fonction ou une méthode, de manière isolée. J'ai une bonne compréhension de leur utilité et de leur mise en œuvre.

Les mocks : Je sais comment utiliser des mocks pour simuler le comportement de dépendances externes lors de l'exécution des tests unitaires. Cela permet de tester l'unité de code de manière indépendante de ses dépendances réelles.

Les tests d'intégration : J'ai compris comment les tests d'intégration vérifient le bon fonctionnement de plusieurs composants ou modules de l'application lorsqu'ils sont combinés. Ces tests permettent de s'assurer que les différents éléments fonctionnent bien ensemble.

Les tests de bout en bout (end to end) : Je sais comment réaliser des tests de bout en bout pour vérifier le bon fonctionnement de l'application dans son ensemble, en simulant les interactions réelles de l'utilisateur avec l'interface.

Le TDD (Test-Driven Development) : Je comprends le concept du TDD, qui consiste à écrire les tests avant le code lui-même. Cela permet de concevoir un code plus fiable et de s'assurer qu'il remplit les exigences spécifiées par les tests.

Les tests par snapshot : J'ai une compréhension des tests par snapshot, qui permettent de capturer la sortie attendue d'une unité de code et de la comparer automatiquement avec les résultats futurs pour détecter toute variation inattendue.

💻 J'utilise
Un exemple personnel commenté ✔️

import { createTestContext, TestContext } from './test-utils'; // Importer la fonction createTestContext depuis les utilitaires de test (e.g., test-utils.ts)

describe('User Resolver', () => {
  let testContext: TestContext;

  beforeAll(async () => {
    testContext = await createTestContext(); // Créer le contexte de test avant tous les tests
  });

  afterAll(async () => {
    await testContext.closeDatabase(); // Fermer la connexion à la base de données après tous les tests
  });

  describe('createUser', () => {
    it('should create a new user', async () => {
      const user = await testContext.resolver.createUser(
        'JohnDoe', 'john.doe@example.com', 'password123'
      );

      expect(user).toBeDefined();
      expect(user.pseudo).toBe('JohnDoe');
      expect(user.email).toBe('john.doe@example.com');
      // Vous pouvez ajouter d'autres assertions en fonction des propriétés de votre User
    });

    it('should throw an error if required fields are missing', async () => {
      // Vous pouvez utiliser try-catch pour capturer l'erreur
      try {
        await testContext.resolver.createUser('', '', '');
        fail('Should have thrown an error');
      } catch (error) {
        // Vérifiez si l'erreur est bien celle que vous attendez
        expect(error.message).toBe('One of the following fields is missing : pseudo, password, email');
      }
    });
  });

  // Ajoutez les autres tests pour les fonctions restantes de votre Resolver
  // updateUser, deleteUser, getUser, getAllUsers, login
});

J'ai créé un exemple personnel de test dans mon projet "Wild Carbon". Dans ce projet, j'ai développé un Resolver GraphQL pour gérer les utilisateurs. J'ai écrit des tests unitaires pour les fonctions du Resolver, notamment pour la création d'un utilisateur et la mise à jour de ses informations. J'ai également utilisé des mocks pour simuler les dépendances externes lors de l'exécution des tests.

Utilisation dans un projet ✔️
Mon projet "Wild Carbon" est disponible sur GitHub. Il contient des exemples de tests unitaires et d'intégration pour différentes parties de l'application. J'ai également utilisé des tests de bout en bout pour vérifier le bon fonctionnement de l'interface utilisateur.

GitHub - Wild Carbon

Utilisation en production si applicable ✔️
Dans ce projet, j'ai également utilisé des tests en production pour m'assurer que l'application fonctionne correctement dans un environnement de production. Ces tests sont exécutés automatiquement avant chaque déploiement pour détecter les éventuels problèmes avant qu'ils n'affectent les utilisateurs.

🌐 J'utilise des ressources
JEST
https://jestjs.io/fr/

Playwright 
https://playwright.dev/

📽️ J'en fais la démonstration
J'ai écrit un tutoriel ❌ / ✔️
J'ai fait une présentation ❌ / ✔️
(Note: Les parties ❌ / ✔️ devraient être complétées avec les informations appropriées pour indiquer si les étapes ont été réalisées ou non)
