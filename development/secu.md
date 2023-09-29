# Sécurité dans le développement Web

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Le rôle de l'OWASP ❌ / ✔️

  L'OWASP (Open Web Application Security Project) joue un rôle essentiel dans la sécurité des applications web et mobiles. Voici une explication du rôle de l'OWASP :

**✔️ Le rôle de l'OWASP :**

L'OWASP est une organisation à but non lucratif composée de professionnels de la sécurité informatique du monde entier. Son principal objectif est d'améliorer la sécurité des applications web et mobiles en fournissant des ressources, des bonnes pratiques et des outils open source à la communauté du développement et de la sécurité. Voici les points clés de son rôle :

1. **Sensibilisation à la sécurité :** L'OWASP joue un rôle crucial dans la sensibilisation à la sécurité des applications. Elle informe les développeurs, les entreprises et les utilisateurs sur les risques liés à la sécurité des applications web et mobiles.

2. **Documentation et ressources :** L'organisation propose une multitude de ressources, de guides, de listes de contrôle, de documentations techniques, de bonnes pratiques et de rapports de recherche sur les vulnérabilités et les menaces actuelles en matière de sécurité des applications.

3. **Outils open source :** L'OWASP développe et maintient de nombreux outils open source conçus pour aider les développeurs et les testeurs de sécurité à identifier, prévenir et résoudre les vulnérabilités dans les applications. Parmi les outils les plus connus figurent OWASP ZAP (Proxy d'Application Web), OWASP Dependency-Check (analyse des dépendances) et bien d'autres.

4. **Top 10 des risques :** L'OWASP publie régulièrement la liste OWASP Top 10, qui recense les dix principales menaces à la sécurité des applications web. Cette liste sert de référence aux développeurs pour se concentrer sur les problèmes de sécurité les plus courants.

5. **Formation et conférences :** L'organisation organise des formations, des conférences et des événements dans le monde entier pour former les professionnels à la sécurité des applications et favoriser les échanges entre experts en sécurité.

6. **Communauté collaborative :** L'OWASP réunit une communauté de personnes intéressées par la sécurité des applications, favorisant ainsi la collaboration entre les membres, les chercheurs en sécurité et les développeurs.

7. **Validation des pratiques :** Les recommandations de l'OWASP sont largement reconnues dans l'industrie et sont souvent utilisées pour évaluer la sécurité des applications et des systèmes. Les entreprises adoptent souvent les bonnes pratiques de l'OWASP pour renforcer leurs politiques de sécurité.

8. **Veille technologique :** L'OWASP surveille en permanence les nouvelles menaces et vulnérabilités émergentes dans le domaine des applications web et mobiles. Elle met à jour ses ressources pour aider les professionnels à faire face à ces nouveaux défis.

En résumé, l'OWASP joue un rôle central dans la sécurisation des applications en fournissant des ressources, des connaissances et des outils essentiels à la communauté de la sécurité et du développement. Son engagement continu dans la sensibilisation à la sécurité et la recherche de solutions contribue à renforcer la protection des applications contre les menaces et les vulnérabilités.

- Les injections SQL ❌ / ✔️

  **✔️ Les injections SQL :**

Les injections SQL sont une catégorie de vulnérabilités de sécurité courantes dans les applications web et les systèmes informatiques. Elles surviennent lorsque des données non fiables ou malveillantes sont incorporées dans une requête SQL, permettant ainsi à un attaquant d'exécuter des commandes SQL non autorisées. Voici une explication des injections SQL et de leurs implications :

1. **Principe de base :** Les bases de données sont souvent utilisées pour stocker des données sensibles, telles que les informations d'utilisateur, les données financières, et bien plus encore. Les injections SQL se produisent lorsque des données fournies par l'utilisateur, généralement via des formulaires web ou des paramètres d'URL, sont directement incluses dans une requête SQL sans validation ou échappement approprié.

2. **Exploitation par les attaquants :** Un attaquant peut exploiter cette vulnérabilité en fournissant des données malveillantes, telles que des chaînes de caractères spécialement conçues, dans les champs de formulaire. Si l'application ne filtre pas correctement ces données, elles peuvent être interprétées comme des commandes SQL par la base de données.

3. **Risques potentiels :** Les conséquences des injections SQL sont graves. Un attaquant peut exécuter des requêtes SQL malveillantes pour extraire, modifier ou supprimer des données de la base de données, ce qui peut entraîner la perte de données, la divulgation d'informations sensibles ou des perturbations dans le fonctionnement de l'application.

4. **Exemple de vulnérabilité :** Un exemple classique est une requête d'authentification qui vérifie l'existence d'un utilisateur dans la base de données en comparant le nom d'utilisateur et le mot de passe saisis par l'utilisateur. Si l'application incorpore simplement les entrées de l'utilisateur dans la requête SQL, un attaquant peut fournir une entrée comme `' OR '1'='1` dans le champ du nom d'utilisateur, ce qui rendra toujours la condition vraie, permettant ainsi à l'attaquant de se connecter sans mot de passe.

5. **Prévention :** Pour prévenir les injections SQL, les développeurs doivent utiliser des requêtes préparées ou des ORM (Object-Relational Mapping) qui échappent automatiquement les données utilisateur. Les données d'entrée doivent être validées, échappées et filtrées pour s'assurer qu'elles sont sans danger pour l'exécution SQL. De plus, les comptes de base de données utilisés par l'application doivent avoir des autorisations limitées pour minimiser les risques.

6. **Audit et test de sécurité :** Il est essentiel de réaliser des audits de sécurité réguliers et des tests de pénétration pour détecter et corriger les vulnérabilités d'injection SQL existantes dans une application. Des outils automatisés et des pratiques de codage sécurisées peuvent également contribuer à réduire ces vulnérabilités.

En conclusion, les injections SQL sont une menace sérieuse pour la sécurité des applications et des bases de données. Les développeurs et les équipes de sécurité doivent mettre en place des mesures de prévention rigoureuses pour protéger leurs systèmes contre cette vulnérabilité courante.

- XSS ❌ / ✔️

  **XSS (Cross-Site Scripting)**, ou injection de script intersite en français, est une vulnérabilité de sécurité courante qui peut avoir des conséquences graves pour les applications web, y compris celles développées avec React. Voici une explication de ce qu'est XSS et comment le prévenir :

### Qu'est-ce que XSS (Cross-Site Scripting) ?

XSS est une technique d'attaque où un attaquant injecte du code JavaScript malveillant dans une application web, qui est ensuite exécuté par le navigateur d'un utilisateur final. Cela se produit lorsque l'application ne filtre pas ou ne valide pas correctement les données fournies par l'utilisateur, permettant ainsi à l'attaquant d'injecter du code dans les pages web consultées par d'autres utilisateurs. Les conséquences possibles de XSS comprennent la vol de sessions utilisateur, la dégradation de la confidentialité des données, voire le contrôle total de l'application par l'attaquant.

### Prévention du XSS en React :

1. **Échapper les données :** L'une des meilleures pratiques pour prévenir XSS est d'échapper correctement toutes les données dynamiques rendues dans votre application React. Cela signifie que vous devez vous assurer que toutes les données fournies par l'utilisateur ou récupérées depuis une source externe sont correctement échappées avant d'être incluses dans le DOM. React effectue l'échappement par défaut pour les valeurs textuelles, mais vous devez toujours être vigilant.

2. **Utiliser les balises React pour l'injection de contenu HTML :** Si vous devez inclure du contenu HTML dans votre application, utilisez les fonctionnalités de React telles que `dangerouslySetInnerHTML` avec précaution. Assurez-vous que le contenu est sûr et provient d'une source fiable.

3. **Configurer les en-têtes HTTP de sécurité :** Utilisez les en-têtes de sécurité HTTP, tels que Content Security Policy (CSP), pour restreindre les sources autorisées de scripts et de contenu. CSP peut aider à bloquer l'exécution de scripts malveillants provenant de sources non autorisées.

4. **Utiliser des bibliothèques de sécurité :** Utilisez des bibliothèques et des frameworks qui intègrent des fonctionnalités de sécurité contre XSS. Par exemple, React Helmet peut vous aider à définir des en-têtes CSP de manière programmatique.

5. **Valider et filtrer les données côté serveur :** Ne faites jamais confiance aux données utilisateur. Côté serveur, effectuez une validation et un filtrage rigoureux des données pour garantir qu'elles sont sûres avant de les envoyer au client.

6. **Utiliser des outils de sécurité :** Utilisez des outils d'analyse statique, des scanners de vulnérabilités et des outils de test de sécurité pour identifier et corriger les vulnérabilités XSS potentielles dans votre application.

En conclusion, XSS est une vulnérabilité de sécurité sérieuse qui peut compromettre la sécurité de votre application React. Cependant, en suivant les bonnes pratiques de sécurité, en échappant les données correctement et en utilisant des outils de sécurité appropriés, vous pouvez réduire considérablement les risques de XSS et protéger votre application contre les attaques malveillantes.

- CRSF ❌ / ✔️

  **CSRF (Cross-Site Request Forgery)**, ou Forgery de Requête intersite en français, est une vulnérabilité de sécurité qui peut affecter les applications web, y compris celles développées avec React. Voici une explication de ce qu'est le CSRF et comment le prévenir :

### Qu'est-ce que le CSRF (Cross-Site Request Forgery) ?

Le CSRF est une attaque où un attaquant force un utilisateur connecté à effectuer involontairement des actions indésirables sur un site web auquel il est authentifié. Cela se produit lorsque l'utilisateur est incité à effectuer une action, telle que la modification de son mot de passe ou la suppression de son compte, sans son consentement explicite. L'attaque peut se produire si l'utilisateur a déjà une session ouverte sur le site ciblé et qu'il visite une page malveillante conçue pour exploiter cette session active.

### Prévention du CSRF en React :

1. **Utiliser des jetons anti-CSRF (CSRF tokens) :** L'une des meilleures pratiques pour prévenir le CSRF est d'utiliser des jetons anti-CSRF dans vos requêtes. Ces jetons sont générés côté serveur et inclus dans les formulaires ou les en-têtes de requête. Lorsqu'une requête est soumise, le serveur vérifie que le jeton correspond à celui généré pour l'utilisateur, empêchant ainsi les requêtes forgées.

2. **Utiliser les en-têtes HTTP de sécurité :** Configurez des en-têtes HTTP de sécurité, tels que SameSite, pour empêcher les cookies de session d'être envoyés dans des requêtes provenant d'autres sites web. L'en-tête SameSite=None; Secure peut être utilisé pour permettre les cookies cross-origin uniquement sur des connexions HTTPS sécurisées.

3. **Valider les origines des requêtes :** Côté serveur, assurez-vous de valider les origines (origins) des requêtes. Vous pouvez vérifier l'en-tête Referer ou l'origine (Origin) pour vous assurer que la requête provient d'un domaine autorisé.

4. **Soyez prudent avec les actions sensibles :** Évitez d'exposer des actions sensibles, telles que la modification de données ou la suppression de comptes, via des liens GET. Utilisez plutôt des méthodes POST ou d'autres méthodes de requête appropriées pour ces actions.

5. **Utiliser des mécanismes d'authentification forts :** Implémentez des mécanismes d'authentification forts, tels que l'authentification à deux facteurs (2FA), pour réduire davantage les risques d'attaques CSRF.

6. **Sensibiliser les utilisateurs :** Éduquez vos utilisateurs sur les risques potentiels du CSRF et encouragez-les à être vigilants lorsqu'ils effectuent des actions sensibles sur le web.

En conclusion, le CSRF est une vulnérabilité de sécurité qui peut mettre en danger l'intégrité des données des utilisateurs dans une application React. Cependant, en mettant en œuvre des mesures de sécurité appropriées, telles que l'utilisation de jetons anti-CSRF, la validation des origines des requêtes et la sensibilisation des utilisateurs, vous pouvez réduire considérablement les risques de CSRF et protéger votre application contre les attaques malveillantes.

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

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
