# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ❌ / ✔️

  ✅ Explication :

L'utilisation de l'état (state) pour contrôler l'affichage d'un composant est une pratique courante en développement d'applications React. Cette approche est extrêmement bénéfique car elle permet de gérer dynamiquement le contenu et l'apparence d'un composant en fonction des interactions de l'utilisateur ou des données reçues.

Initialisation de l'état : Vous pouvez déclarer un état initial pour votre composant en utilisant le hook useState (ou this.state dans une classe). Par exemple, vous pouvez définir une variable d'état isVisible initialement à true si vous souhaitez afficher un composant au chargement de l'écran.

Changement de l'état : Lorsqu'un événement se produit (par exemple, un clic sur un bouton), vous pouvez appeler une fonction pour mettre à jour l'état en utilisant la fonction setState (ou this.setState dans une classe). Par exemple, vous pouvez définir isVisible sur false pour masquer le composant lorsque l'utilisateur clique sur un bouton "Masquer".

Rendu conditionnel : Vous pouvez utiliser la valeur de l'état pour contrôler ce qui est affiché dans votre composant. Par exemple, vous pouvez conditionnellement rendre un élément ou un composant en fonction de la valeur de isVisible. Si isVisible est true, le composant sera affiché ; s'il est false, le composant sera masqué.

Réaction aux changements : Lorsque vous mettez à jour l'état, React réagit automatiquement en réexécutant la fonction de rendu du composant avec les nouvelles valeurs d'état. Cela entraîne une mise à jour de l'interface utilisateur pour refléter les changements.

✅ Avantages :

Contrôle dynamique de l'interface utilisateur : Vous pouvez modifier l'apparence et le comportement de votre application en fonction des actions de l'utilisateur ou des données reçues.

Réactivité : Grâce à React, les mises à jour de l'état sont gérées efficacement, ce qui garantit des mises à jour instantanées de l'interface utilisateur.

Logique conditionnelle : Vous pouvez utiliser des déclarations conditionnelles pour afficher ou masquer des éléments en fonction de l'état actuel.

❌ Attention :

Il est essentiel de gérer correctement l'état pour éviter les problèmes de performances et les comportements inattendus. Une mauvaise gestion de l'état peut entraîner des boucles de rendu excessives.

L'état local d'un composant est limité à ce composant. Si vous avez besoin de partager des données entre plusieurs composants, vous devrez envisager d'utiliser un gestionnaire d'état global ou de passer des données via les propriétés (props).

En résumé, l'utilisation de l'état pour contrôler l'affichage d'un composant est une pratique essentielle en développement d'applications React, permettant une gestion dynamique et réactive de l'interface utilisateur en réponse aux interactions de l'utilisateur et aux données.

- les composants enfants et les _props_ qu'on leur passe ❌ / ✔️

  
✅ Explication :

En React, les composants enfants et les props sont des concepts fondamentaux pour la construction d'applications modulaires et réutilisables. Ils permettent de créer une hiérarchie de composants où les données et les fonctionnalités peuvent être transmises de manière structurée de parent à enfant.

Composants Enfants : En React, un composant peut inclure d'autres composants à l'intérieur de lui-même. Les composants inclus sont appelés "composants enfants". Les composants enfants sont utilisés pour encapsuler et organiser des parties spécifiques de l'interface utilisateur. Ils sont définis comme des balises ou des éléments à l'intérieur du JSX du composant parent.

Props (Propriétés) : Les props (propriétés) sont des objets JavaScript qui permettent de passer des données d'un composant parent à un composant enfant. Les props sont essentiellement des arguments que vous pouvez fournir à un composant enfant lors de son utilisation dans un composant parent. Ces données peuvent être des valeurs, des fonctions ou d'autres composants React.

Passage de Props : Dans le composant parent, vous pouvez spécifier des props en les passant comme attributs aux composants enfants. Par exemple, <MonComposant nom="John" age={30} /> envoie les props nom et age au composant MonComposant.

Utilisation des Props : Dans le composant enfant, vous pouvez accéder aux props en les référençant comme des propriétés de l'objet props. Par exemple, this.props.nom ou props.age dans une fonction ou un composant fonctionnel.

✅ Avantages :

Réutilisation : Les composants peuvent être réutilisés avec différentes données en utilisant des props, ce qui favorise la modularité et l'efficacité du code.

Organisation : Les composants enfants permettent de découper une interface utilisateur complexe en composants plus petits et gérables, améliorant ainsi la lisibilité du code.

Communication : Les props facilitent la communication entre les composants d'une application React en permettant le passage de données de parent à enfant.

Flexibilité : Vous pouvez personnaliser le comportement d'un composant en fonction des props qu'il reçoit, ce qui le rend flexible et adaptable.

❌ Attention :

Les props sont immuables, ce qui signifie qu'ils ne peuvent pas être modifiés directement par le composant enfant. Cela favorise la stabilité du flux de données dans l'application, mais si vous avez besoin de modifier des données, vous devrez généralement le faire dans le composant parent.

Une gestion incorrecte des props peut entraîner des erreurs ou des comportements inattendus. Il est essentiel de documenter et de comprendre les props attendues par chaque composant.

En résumé, en React, les composants enfants et les props sont des concepts cruciaux pour la création d'interfaces utilisateur modulaires et dynamiques. Ils permettent de structurer et de personnaliser les composants de manière à favoriser la réutilisation et la communication entre les différents éléments de l'application.

- le déclenchement d'instructions en fonction des actions de l'utilisateur ❌ / ✔️

  ✅ **Explication :**

En React, le déclenchement d'instructions en fonction des actions de l'utilisateur est une partie essentielle de la création d'applications interactives. Cela se fait généralement en réponse à des événements, tels que des clics de souris, des pressions sur des touches, des changements d'entrée, etc. Voici comment cela fonctionne :

1. **Gestion des Événements :** Pour détecter les actions de l'utilisateur, vous pouvez ajouter des gestionnaires d'événements à vos éléments JSX (comme des boutons, des champs de saisie, etc.). Ces gestionnaires d'événements sont des fonctions qui seront exécutées lorsque l'événement correspondant se produit. Par exemple, vous pouvez ajouter un gestionnaire `onClick` à un bouton pour réagir à un clic de souris.

   ```jsx
   <button onClick={handleClick}>Cliquez ici</button>
   ```

2. **Fonctions de Gestion d'Événements :** Les fonctions de gestion d'événements, comme `handleClick` dans l'exemple ci-dessus, sont des fonctions JavaScript définies par vous. Elles décrivent ce qui doit se produire lorsque l'événement se déclenche.

   ```jsx
   function handleClick() {
     alert('Bouton cliqué !');
   }
   ```

3. **État (State) :** Pour suivre l'état de votre application en réponse aux actions de l'utilisateur, vous pouvez utiliser l'état (`state`) de React. L'état est un objet JavaScript qui contient des données pertinentes pour votre composant. Lorsque l'état change, le composant se met à jour et React réagit en réexécutant le rendu du composant.

   ```jsx
   const [count, setCount] = useState(0); // Exemple de déclaration de l'état
   ```

4. **Mise à Jour de l'État :** Vous pouvez mettre à jour l'état à l'intérieur des fonctions de gestion d'événements en utilisant des fonctions telles que `setState`. Cela déclenche une réexécution du rendu du composant avec la nouvelle valeur de l'état.

   ```jsx
   function incrementCount() {
     setCount(count + 1); // Augmente la valeur de l'état count de 1
   }
   ```

5. **Rendu Dynamique :** Lorsque l'état change ou que d'autres données changent, React met à jour automatiquement le DOM pour refléter ces modifications. Cela signifie que vous pouvez créer des interfaces utilisateur réactives où le contenu est mis à jour en fonction des actions de l'utilisateur.

En résumé, en React, vous pouvez déclencher des instructions en fonction des actions de l'utilisateur en utilisant des gestionnaires d'événements pour détecter ces actions. Vous pouvez également suivre l'état de votre application à l'aide de l'état (`state`) de React et mettre à jour cet état pour déclencher des changements dynamiques dans votre interface utilisateur. Cette approche permet de créer des applications interactives et réactives.

- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ❌ / ✔️

  
✅ Explication :

En React, vous pouvez déclencher des instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props. Le cycle de vie du composant se compose de plusieurs étapes, telles que le montage, la mise à jour et le démontage. Voici comment cela fonctionne :

Montage du Composant :

Lorsqu'un composant est créé et inséré dans le DOM pour la première fois, il passe par le cycle de vie de montage.
Vous pouvez exécuter des instructions spécifiques à cette étape en utilisant la méthode componentDidMount (dans les composants de classe) ou le hook useEffect (dans les composants fonctionnels).
Exemple avec useEffect :

useEffect(() => {
  // Instructions à exécuter après le montage du composant
  console.log('Le composant est monté.');
  // Vous pouvez effectuer des appels AJAX, des abonnements, etc.
}, []); // Le tableau vide signifie que cela ne s'exécutera qu'une fois après le montage.
Mise à Jour du Composant :

Lorsque les props ou l'état (state) d'un composant changent, il passe par le cycle de vie de mise à jour.
Vous pouvez exécuter des instructions spécifiques à cette étape en utilisant la méthode componentDidUpdate (dans les composants de classe) ou le hook useEffect (dans les composants fonctionnels).
Exemple avec useEffect pour surveiller les changements de props :

useEffect(() => {
  // Instructions à exécuter lorsque les props changent
  console.log('Les props ont changé :', props);
}, [props]); // L'effet sera déclenché lorsque les props changent.
Démontage du Composant :

Lorsqu'un composant est supprimé du DOM, il passe par le cycle de vie de démontage.
Vous pouvez exécuter des instructions spécifiques à cette étape en utilisant la méthode componentWillUnmount (dans les composants de classe) ou en nettoyant les effets dans le hook useEffect (dans les composants fonctionnels).
Exemple avec useEffect pour nettoyer un effet :

useEffect(() => {
  // Instructions à exécuter lors du montage
  console.log('Le composant est monté.');

  return () => {
    // Instructions à exécuter lors du démontage
    console.log('Le composant est démonté.');
    // Vous pouvez annuler des abonnements ou nettoyer des ressources.
  };
}, []);

// ...

return (
  // Contenu du composant
);
En résumé, vous pouvez déclencher des instructions en fonction de l'étape du cycle de vie du composant en utilisant les méthodes ou les hooks appropriés. De plus, vous pouvez également exécuter des instructions en fonction des changements de props en surveillant les changements à l'aide de useEffect (dans les composants fonctionnels) ou des méthodes de cycle de vie (dans les composants de classe). Cela vous permet de contrôler le comportement et l'interaction de vos composants en fonction de différentes situations et étapes d'exécution.

- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant
- 
✅ **Explication :**

En React, l'utilisation d'un reducer avec `useReducer` permet de gérer un état complexe dans un composant de manière structurée. Un reducer est une fonction qui spécifie comment l'état d'un composant doit être mis à jour en réponse à des actions. Voici comment cela fonctionne :

1. **Initialisation du Reducer :**

   Pour utiliser `useReducer`, vous devez d'abord initialiser un état initial et un reducer. L'état initial représente l'état de départ de votre composant, tandis que le reducer est une fonction qui définit comment cet état peut être modifié en réponse à des actions.

   Exemple :
   ```jsx
   const initialState = {
     count: 0,
     user: null,
   };

   const reducer = (state, action) => {
     switch (action.type) {
       case 'INCREMENT':
         return { ...state, count: state.count + 1 };
       case 'DECREMENT':
         return { ...state, count: state.count - 1 };
       case 'SET_USER':
         return { ...state, user: action.payload };
       default:
         return state;
     }
   };
   ```

2. **Utilisation de `useReducer` :**

   Une fois que vous avez initialisé votre état initial et votre reducer, vous pouvez les utiliser avec `useReducer` dans votre composant.

   Exemple :
   ```jsx
   import React, { useReducer } from 'react';

   function MyComponent() {
     const [state, dispatch] = useReducer(reducer, initialState);

     // Vous pouvez maintenant accéder à l'état et au dispatch pour effectuer des actions.
     const { count, user } = state;

     const increment = () => {
       dispatch({ type: 'INCREMENT' });
     };

     const decrement = () => {
       dispatch({ type: 'DECREMENT' });
     };

     const setUser = (userData) => {
       dispatch({ type: 'SET_USER', payload: userData });
     };

     return (
       <div>
         <p>Count: {count}</p>
         <button onClick={increment}>Increment</button>
         <button onClick={decrement}>Decrement</button>
         <button onClick={() => setUser({ name: 'John' })}>Set User</button>
       </div>
     );
   }
   ```

3. **Actions et Mise à Jour de l'État :**

   Lorsque vous appelez `dispatch` avec une action, le reducer est exécuté, et en fonction du type de l'action, il mettra à jour l'état en conséquence.

   - Dans l'exemple ci-dessus, lorsque vous appelez `increment()`, cela envoie une action de type 'INCREMENT', ce qui incrémente la valeur de `count` dans l'état.
   - De même, `decrement()` envoie une action de type 'DECREMENT' pour décrémenter la valeur de `count`.
   - `setUser(userData)` envoie une action de type 'SET_USER' avec les données de l'utilisateur, mettant à jour la valeur de `user` dans l'état.

4. **Avantages :**

   - `useReducer` est utile pour gérer des états complexes, en particulier lorsque l'état dépend de plusieurs variables.
   - Il favorise une gestion structurée des mises à jour de l'état en regroupant les actions dans un reducer.
   - Il est souvent préféré pour les états complexes par rapport à `useState`.

5. **Inconvénients :**

   - Il peut sembler verbeux pour des états simples.
   - Il peut nécessiter plus de code initial par rapport à `useState`, mais il devient plus avantageux à mesure que la complexité de l'état augmente.

En résumé, `useReducer` est une méthode puissante pour gérer l'état d'un composant React, en particulier lorsque cet état est complexe et dépend de plusieurs actions. Il vous permet de structurer votre code de manière propre et de gérer les mises à jour de l'état de manière plus prévisible.
  
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ❌ / ✔️
✅ **Explication :**

En React, l'état stocké dans un composant avec un **Context Provider** et accessible dans ses descendants via `useContext` est une technique qui permet de partager des données entre des composants sans avoir besoin de les passer explicitement via les _props_. Voici comment cela fonctionne :

1. **Création du Context :**

   Tout d'abord, vous créez un context en utilisant `React.createContext()`. Ce context servira de point de communication pour les composants descendants.

   Exemple :
   ```jsx
   import React, { createContext, useContext, useState } from 'react';

   const MyContext = createContext();
   ```

2. **Création du Context Provider :**

   Ensuite, vous créez un composant qui agit comme le **Context Provider**. Ce composant contient l'état que vous souhaitez partager et fournit des méthodes pour le mettre à jour.

   Exemple :
   ```jsx
   function MyContextProvider({ children }) {
     const [data, setData] = useState('Initial data');

     const updateData = (newData) => {
       setData(newData);
     };

     return (
       <MyContext.Provider value={{ data, updateData }}>
         {children}
       </MyContext.Provider>
     );
   }
   ```

3. **Utilisation du Context Provider :**

   Vous enveloppez les composants qui doivent accéder à cet état dans le **Context Provider** en les plaçant à l'intérieur de ce composant.

   Exemple :
   ```jsx
   function App() {
     return (
       <MyContextProvider>
         {/* Vos composants ici */}
         <ChildComponent />
       </MyContextProvider>
     );
   }
   ```

4. **Accès à l'État avec `useContext` :**

   Pour accéder à l'état partagé dans un composant descendant, vous utilisez le hook `useContext` en passant le context que vous avez créé. Cela permet au composant de lire et de mettre à jour l'état partagé.

   Exemple :
   ```jsx
   function ChildComponent() {
     const { data, updateData } = useContext(MyContext);

     return (
       <div>
         <p>Données partagées : {data}</p>
         <button onClick={() => updateData('Nouvelles données')}>Mettre à jour</button>
       </div>
     );
   }
   ```

5. **Avantages :**

   - L'utilisation d'un **Context Provider** simplifie le partage d'état entre des composants éloignés dans l'arborescence des composants, évitant ainsi de passer des _props_ à travers plusieurs niveaux.
   - Il améliore la maintenabilité en regroupant la gestion de l'état dans un seul endroit.
   - Les composants consommateurs peuvent accéder à l'état partagé de manière simple et efficace grâce à `useContext`.

6. **Inconvénients :**

   - Il peut être surutilisé, ce qui rendrait le code difficile à comprendre s'il y a trop de contextes différents dans une application.
   - Il est généralement adapté pour partager des données globales, mais pas pour des données spécifiques à quelques composants.

En résumé, l'utilisation d'un **Context Provider** en combinaison avec `useContext` est une méthode puissante pour partager des données entre des composants sans dépendre des _props_. Cela rend le code plus propre et plus facile à maintenir, en particulier pour des états partagés à l'échelle de l'application.
## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️
import {
  Dispatch,
  FC,
  SetStateAction,
  createContext,
  useEffect,
  useMemo,
  useState,
} from 'react';
import { getUserTokenFromLocalStorage } from './localStorage';

interface LoginContextType {
  isLoggedIn: boolean;
  setIsLoggedIn: Dispatch<SetStateAction<boolean>>;
  userToken: string | undefined;
  setUserToken: Dispatch<SetStateAction<string | undefined>>;
  userId: string;
  setUserId: Dispatch<SetStateAction<string>>;
}

export const LoginContext = createContext<LoginContextType>({
  isLoggedIn: false,
  setIsLoggedIn: () => {},
  userToken: "",
  setUserToken: () => {},
  userId: "",
  setUserId: () => {},
});

export const LoginContextProvider: FC<{ children: React.ReactNode }> = ({
  children,
}) => {
  const userTokenData = useMemo(() => getUserTokenFromLocalStorage(), []);
  const [isLoggedIn, setIsLoggedIn] = useState(!!userTokenData?.userToken);
  const [userToken, setUserToken] = useState<string | undefined>(
    userTokenData?.userToken,
  );
  const [userId, setUserId] = useState("")

  const providerValue = useMemo(
    () => ({
      isLoggedIn,
      setIsLoggedIn,
      userToken,
      setUserToken,
      userId,
      setUserId,
    }),
    [isLoggedIn, setIsLoggedIn],
  );

  useEffect(() => {
    if (userTokenData) {
      setIsLoggedIn(!!userTokenData.userToken);
      setUserToken(userTokenData.userToken);
    }
  }, [userTokenData]);

  return (
    <LoginContext.Provider value={providerValue}>
      {children}
    </LoginContext.Provider>
  );
};

Ce code en React permet de créer un contexte de connexion (LoginContext) pour gérer l'état de la connexion de l'utilisateur dans une application. Voici une explication détaillée du code :

1. Importations :
   - Plusieurs éléments sont importés depuis la bibliothèque React, notamment `Dispatch`, `FC`, `SetStateAction`, `createContext`, `useEffect`, `useMemo`, et `useState`.
   - La fonction `getUserTokenFromLocalStorage` est importée depuis un module nommé `localStorage`.

2. Interface `LoginContextType` :
   - Une interface `LoginContextType` est définie pour spécifier le type de données qui seront stockées dans le contexte.
   - Elle contient les propriétés suivantes :
     - `isLoggedIn`: Un booléen qui indique si l'utilisateur est connecté ou non.
     - `setIsLoggedIn`: Une fonction pour mettre à jour l'état de la connexion.
     - `userToken`: Une chaîne de caractères qui stocke le jeton de l'utilisateur.
     - `setUserToken`: Une fonction pour mettre à jour le jeton de l'utilisateur.
     - `userId`: Une chaîne de caractères qui stocke l'ID de l'utilisateur.
     - `setUserId`: Une fonction pour mettre à jour l'ID de l'utilisateur.

3. Création du Contexte `LoginContext` :
   - Un contexte nommé `LoginContext` est créé en utilisant la fonction `createContext`.
   - Les valeurs par défaut sont spécifiées pour chaque propriété du contexte, mais elles seront écrasées ultérieurement.

4. Composant `LoginContextProvider` :
   - Un composant fonctionnel `LoginContextProvider` est défini. Il prend un prop nommé `children` qui représente les composants enfants qui auront accès à ce contexte.
   - Dans ce composant, la valeur du jeton d'utilisateur est obtenue à partir du stockage local à l'aide de la fonction `getUserTokenFromLocalStorage` et est mémorisée dans la variable `userTokenData`.
   - Trois états sont créés à l'aide de `useState` :
     - `isLoggedIn`: Il est initialisé à `true` si `userTokenData?.userToken` est défini, sinon à `false`.
     - `userToken`: Il est initialisé avec la valeur de `userTokenData?.userToken` s'il est défini, sinon à `undefined`.
     - `userId`: Il est initialisé à une chaîne vide (`""`).
   - La valeur du contexte est créée avec `useMemo` pour s'assurer que les valeurs ne sont recalculées que lorsque `isLoggedIn` change.
   - Un effet `useEffect` est utilisé pour mettre à jour `isLoggedIn` et `userToken` lorsque `userTokenData` change, c'est-à-dire lorsque le jeton de l'utilisateur est récupéré ou supprimé du stockage local.

5. Rendu du composant `LoginContextProvider` :
   - Le composant `LoginContextProvider` enveloppe ses composants enfants avec `LoginContext.Provider` et passe `providerValue` comme valeur du contexte.

Ce code crée un contexte de connexion (LoginContext) qui stocke l'état de la connexion de l'utilisateur et les informations de l'utilisateur. Ce contexte peut ensuite être utilisé dans d'autres composants de l'application pour accéder à ces données sans avoir besoin de les propager manuellement via les _props_.
### Utilisation dans un projet ❌ / ✔️

[[lien github](...)](https://github.com/AlexisFaugeroux/wild-carbon)

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
