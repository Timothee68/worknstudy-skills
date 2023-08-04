# GraphQL

la différence entre REST et GraphQL ✔️
La différence majeure entre REST et GraphQL réside dans la manière dont les clients peuvent récupérer les données. REST suit une approche "stateless" où chaque ressource est exposée sous une URL spécifique, et le client doit effectuer plusieurs requêtes pour récupérer toutes les données nécessaires. En revanche, GraphQL permet au client de définir la structure des données dont il a besoin à partir d'une seule requête, ce qui permet d'éviter le surchargement des données.

les besoins auxquels répond GraphQL ✔️
GraphQL répond aux besoins des applications modernes en permettant aux clients de récupérer exactement les données dont ils ont besoin, ni plus ni moins. Cela améliore les performances en réduisant la surcharge du réseau et en évitant les problèmes liés au sur-recouvrement des données. De plus, GraphQL permet aux clients de récupérer des données provenant de différentes sources en une seule requête, ce qui simplifie le développement côté client.

la définition d'un schéma ✔️
Un schéma GraphQL définit les types de données disponibles dans l'API GraphQL et les relations entre ces types. Il définit également les requêtes (Query), les mutations (Mutation) et les abonnements (Subscription) que les clients peuvent utiliser pour interagir avec l'API. Le schéma agit comme un contrat entre le serveur GraphQL et les clients, garantissant que toutes les données renvoyées par l'API sont conformes à la structure définie.

Query ✔️
Les requêtes (Query) sont utilisées pour récupérer des données à partir de l'API GraphQL. Les clients spécifient les champs dont ils ont besoin dans la requête, et le serveur renvoie les données demandées sous la forme d'un objet JSON.

Mutation ✔️
Les mutations sont utilisées pour effectuer des modifications sur les données du serveur via l'API GraphQL. Les clients peuvent envoyer une requête de mutation pour ajouter, mettre à jour ou supprimer des données.

Subscription ✔️
Les abonnements (Subscription) permettent aux clients de s'abonner aux mises à jour en temps réel des données. Cela permet aux clients de recevoir des notifications lorsqu'une donnée spécifique est modifiée sur le serveur.

💻 J'utilise

@Resolver()
class ArticleResolver {
  // Définition d'un resolver pour la mutation "createArticle"
  @Mutation(() => Article) // Décorateur indiquant que cette fonction est un resolver pour une mutation qui renvoie un objet de type "Article"
  async createArticle(
    @Arg('title') title: string, // Argument "title" de type string extrait de la requête GraphQL
    @Arg('description') description: string, // Argument "description" de type string extrait de la requête GraphQL
    @Arg('url') url: string, // Argument "url" de type string extrait de la requête GraphQL
    @Arg('userId') userId: string, // Argument "userId" de type string extrait de la requête GraphQL
  ): Promise<Article> { // La fonction renvoie une promesse d'un objet de type "Article"
    try {
      // Vérification si les champs obligatoires sont bien renseignés
      if (!title || !description || !url) {
        throw new Error(
          'One of the following fields is missing : title, description, url, createdAt',
        );
      }

      // Création d'un nouvel objet "Article" avec les données fournies
      const article = new Article();
      article.title = title;
      article.description = description;
      article.url = url;
      article.createdAt = new Date(); // Définition de la date de création à la date actuelle
      article.user.id = userId; // Définition de l'ID de l'utilisateur associé à l'article

      // Sauvegarde de l'article dans la base de données à l'aide de TypeORM
      const createdArticle = await dataSource
        .getRepository(Article)
        .save(article);

      // Renvoi de l'article nouvellement créé
      return createdArticle;
    } catch (error) {
      console.error(error);
      throw error; // Lancement de l'erreur pour renvoyer un message d'erreur aux clients GraphQL
    }
  }
}
Ce code définit un resolver pour la mutation "createArticle" qui permet de créer un nouvel article en fournissant les champs "title", "description", "url" et "userId". La fonction effectue une vérification pour s'assurer que tous les champs obligatoires sont bien renseignés. Ensuite, elle crée un nouvel objet "Article" avec les données fournies, définissant automatiquement la date de création à la date actuelle. Enfin, elle sauvegarde l'article dans la base de données à l'aide de TypeORM et renvoie l'article nouvellement créé. Si une erreur survient lors de la création de l'article, elle est affichée dans la console et renvoyée aux clients GraphQL pour afficher un message d'erreur approprié.

### Utilisation dans un projet ❌ / ✔️

[lien github](...)
https://github.com/AlexisFaugeroux/wild-carbon
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
