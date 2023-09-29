# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ❌ / ✔️
L'importance de TypeScript dans le contexte d'un environnement de développement intégré, ou IDE. TypeScript est un sur-ensemble de JavaScript, apportant des avantages considérables au processus de développement logiciel.

Tout d'abord, TypeScript introduit le concept de typage statique. Cela signifie que chaque variable, paramètre de fonction et valeur de retour de fonction peut être annoté avec un type de données spécifique. Cette fonctionnalité offre de nombreux avantages, à commencer par la détection précoce des erreurs. Contrairement à JavaScript, où les erreurs de typage ne sont souvent découvertes qu'à l'exécution, TypeScript les repère avant même que le code ne soit exécuté. Cela permet d'éviter de nombreux bogues coûteux à corriger.

En outre, TypeScript améliore la lisibilité du code. Les types explicites servent de documentation en temps réel, permettant aux développeurs de comprendre rapidement comment utiliser une fonction ou une variable donnée. Cela facilite la collaboration au sein de l'équipe et accélère le processus de développement.

Un autre avantage significatif est l'intégration étroite de TypeScript avec les IDE populaires, tels que Visual Studio Code. L'IDE peut fournir des fonctionnalités avancées, telles que la saisie semi-automatique, les suggestions intelligentes et les diagnostics en temps réel. Cela améliore la productivité des développeurs en leur permettant d'écrire du code de manière plus efficace et sans erreur.

De plus, TypeScript facilite la maintenance à long terme des applications. Lorsque le code est typé de manière explicite, il est plus facile de comprendre la structure de l'application et d'apporter des modifications en toute confiance. Cela contribue à réduire la dette technique et à garantir que l'application reste robuste et évolutive au fil du temps.

En conclusion, l'introduction de TypeScript dans un IDE est un choix judicieux pour tout projet de développement logiciel. Il permet la détection précoce des erreurs, améliore la lisibilité du code, renforce la productivité des développeurs et facilite la maintenance à long terme. En tant que développeur, je considère TypeScript comme un outil essentiel pour garantir la qualité et la fiabilité de nos applications."
- les types de bases ❌ / ✔️
  TypeScript : Les Types de Base

TypeScript est un langage de programmation qui s'appuie sur JavaScript en y ajoutant des fonctionnalités de typage statique. Cette caractéristique permet de détecter des erreurs potentielles lors de la phase de développement, ce qui rend le code plus fiable et plus facile à maintenir.

Voici quelques-uns des types de base les plus couramment utilisés en TypeScript :

number : Ce type est utilisé pour représenter les nombres, qu'ils soient entiers ou à virgule flottante. Par exemple :

let age: number = 30;
let pi: number = 3.14;
string : Le type "string" est utilisé pour représenter les chaînes de caractères. Il peut contenir du texte, des nombres ou d'autres caractères. Exemple :

let nom: string = "Jean";
boolean : Les valeurs booléennes "true" ou "false" sont représentées par le type "boolean". Par exemple :

let estActif: boolean = true;
array : Les tableaux peuvent contenir une liste de valeurs du même type ou de types différents. Vous pouvez spécifier le type des éléments à l'intérieur du tableau en utilisant des crochets [] ou la syntaxe générique Array<type>. Exemple :

let nombres: number[] = [1, 2, 3, 4];
let fruits: Array<string> = ["pomme", "banane", "orange"];
object : Le type "object" peut représenter n'importe quel objet JavaScript. Cependant, il est généralement préférable de spécifier la forme attendue de l'objet en utilisant des interfaces ou des types personnalisés. Exemple :

let personne: object = { nom: "Alice", age: 25 };
null et undefined : Ces types sont utilisés pour représenter l'absence de valeur. Par exemple, une variable peut être déclarée comme suit :

let variableNulle: null = null;
let variableNonDéfinie: undefined = undefined;
any : Le type "any" permet de désactiver le typage statique pour une variable, ce qui signifie qu'elle peut contenir n'importe quel type de valeur. Bien que pratique, l'utilisation excessive de "any" peut annuler certains avantages de TypeScript en termes de sécurité. Exemple :

let valeurDynamique: any = "Je peux être de n'importe quel type !";
void : Le type "void" est principalement utilisé pour indiquer qu'une fonction ne renvoie aucune valeur. Exemple :

function afficherMessage(): void {
    console.log("Bonjour !");
}
En utilisant ces types de base, TypeScript permet aux développeurs de mieux comprendre et de gérer les données dans leur code, ce qui contribue à réduire les erreurs et à rendre le développement plus efficace.
- comment et pourquoi étendre une interface ❌ / ✔️

Étendre une Interface en TypeScript

En TypeScript, les interfaces sont des contrats qui définissent la forme des objets et des classes. L'une des fonctionnalités puissantes de TypeScript est la possibilité d'étendre une interface existante pour créer de nouvelles interfaces plus spécifiques. Cela se fait en utilisant le mot-clé extends. Voyons comment et pourquoi cela est utile.

Comment étendre une interface :

Pour étendre une interface, vous utilisez le mot-clé extends. Par exemple, supposons que nous ayons une interface de base pour définir les caractéristiques d'un animal :

interface Animal {
    nom: string;
    type: string;
}
Maintenant, si nous voulons créer une interface pour définir les caractéristiques spécifiques d'un oiseau, nous pouvons étendre l'interface Animal comme ceci :

interface Oiseau extends Animal {
    envergure: number;
    couleurPlumes: string;
}
L'interface Oiseau hérite des propriétés de l'interface Animal et ajoute ses propres propriétés spécifiques aux oiseaux.

Pourquoi étendre une interface :

Réutilisation de code : L'extension d'interfaces permet de réutiliser des définitions de propriétés. Dans l'exemple précédent, nous n'avons pas besoin de redéfinir nom et type pour chaque interface d'animal spécifique.

Organisation du code : Les interfaces étendues aident à organiser le code de manière logique. Vous pouvez définir une interface de base avec des propriétés communes, puis créer des interfaces spécialisées pour chaque type spécifique.

Clarté et maintenabilité : En définissant des interfaces spécifiques, le code devient plus clair et plus facile à maintenir. Vous savez immédiatement quelles propriétés sont requises pour chaque type d'objet.

Sécurité du typage : TypeScript effectue des vérifications de type statiques, ce qui signifie que vous serez averti en cas d'omission ou de mauvaise utilisation de propriétés. Étendre des interfaces permet de garantir une cohérence dans l'utilisation des objets.

En conclusion, étendre une interface en TypeScript est une pratique courante et utile pour organiser, réutiliser et clarifier votre code. Cela contribue à une meilleure compréhension du code, à sa maintenance et à sa sécurité en matière de typage.

- les classes et les decorators ❌ / ✔️

  Classes et Decorators en TypeScript

En TypeScript, les classes sont des structures fondamentales pour créer des objets réutilisables et organiser votre code de manière orientée objet. Les decorators, quant à eux, sont des fonctionnalités avancées qui permettent de modifier le comportement des classes, des propriétés ou des méthodes. Explorons ces concepts plus en détail.

Les Classes :

Une classe est un modèle ou un plan pour créer des objets. Elle définit à quoi ressemblera un objet, quelles propriétés il aura et quelles méthodes il pourra exécuter. Voici un exemple de déclaration de classe en TypeScript :

class Animal {
    nom: string;
    constructor(nom: string) {
        this.nom = nom;
    }
    faireDuBruit() {
        console.log(`L'animal ${this.nom} fait un bruit.`);
    }
}
Dans cet exemple, nous avons une classe Animal avec une propriété nom et une méthode faireDuBruit.

Les Decorators :

Les decorators sont des fonctions spéciales utilisées pour annoter ou modifier des classes, des méthodes, des propriétés ou des paramètres de méthode. Ils sont précédés du symbole @. Voici un exemple de décorateur de méthode en TypeScript :

function logExecution(target: any, propertyKey: string, descriptor: PropertyDescriptor) {
    const originalMethod = descriptor.value;
    descriptor.value = function (...args: any[]) {
        console.log(`Méthode ${propertyKey} exécutée avec les arguments : ${args}`);
        return originalMethod.apply(this, args);
    };
}
Dans cet exemple, nous avons créé un décorateur logExecution qui affiche un message chaque fois qu'une méthode est appelée.

Pourquoi utiliser les Decorators :

Métadonnées et annotations : Les decorators permettent d'ajouter des métadonnées et des annotations aux classes, aux méthodes ou aux propriétés. Cela peut être utile pour la réflexion, la validation ou d'autres tâches.

Aspect-Oriented Programming (AOP) : Les decorators facilitent l'implémentation de la programmation orientée aspect, où vous pouvez séparer les préoccupations transversales du code métier.

Modularité : Les decorators permettent d'ajouter des fonctionnalités supplémentaires aux classes sans les modifier directement. Cela favorise la modularité du code.

Lisibilité : Les decorators peuvent améliorer la lisibilité du code en déplaçant des fonctionnalités complexes ou répétitives vers des décorateurs réutilisables.

Exemple d'utilisation de Decorators :

class ExempleClasse {
    @logExecution
    methodeA() {
        // ...
    }
}
Dans cet exemple, la méthode methodeA de ExempleClasse est annotée avec le décorateur logExecution. Lorsque methodeA est appelée, le décorateur ajoute un message de journalisation.

En conclusion, les classes sont des éléments clés de la programmation orientée objet en TypeScript, et les decorators sont des outils puissants pour améliorer la modularité, la lisibilité et l'extensibilité de votre code.

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

### Utilisation dans un projet ❌ / ✔️

https://github.com/AlexisFaugeroux/wild-carbon

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

TypeScript Documentation : https://www.typescriptlang.org/docs/
stackoverflow

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
ecris tous comme si je l'écrivais moi pour un jury et explique
