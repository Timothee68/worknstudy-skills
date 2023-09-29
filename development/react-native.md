# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les différences et points communs entre du code react et du code react native ❌ / ✔️
  Points Communs (✔️) :
Même Langage de Programmation : Les deux utilisent JavaScript (ou TypeScript). Le code de base, la logique et la structure de données peuvent être très similaires.

Composants Réutilisables : Vous pouvez réutiliser des composants React dans une application React Native. Cette réutilisation de code permet de gagner du temps et de maintenir une cohérence visuelle.

Gestion d'État avec React : Vous pouvez utiliser les mêmes bibliothèques de gestion d'état React telles que Redux ou React Context pour gérer l'état de votre application, quel que soit l'environnement.

React Navigation : React Navigation est une bibliothèque de navigation populaire qui peut être utilisée à la fois dans React et React Native pour gérer les routes et la navigation.

Composants UI React : Vous pouvez utiliser des bibliothèques de composants d'interface utilisateur React telles que Material-UI ou Ant Design dans les deux environnements.

Différences (❌) :
Éléments d'Interface : React utilise des éléments HTML pour créer une interface utilisateur, tandis que React Native utilise des composants natifs tels que View, Text, Image, etc., qui se traduisent ensuite en éléments d'interface utilisateur natifs sur les plates-formes mobiles.

Styles CSS : React utilise des styles CSS traditionnels, tandis que React Native utilise un système de styles basé sur JavaScript qui se traduit en feuilles de styles natives. Vous utilisez des propriétés comme StyleSheet.create pour définir des styles.

Gestion des Événements : Les événements tels que les clics sont gérés différemment. Dans React, vous utilisez les gestionnaires d'événements HTML standard, tandis que dans React Native, vous utilisez des gestionnaires d'événements spécifiques à la plate-forme.

Mises en Page Flexbox : React Native utilise le modèle de mise en page Flexbox pour créer des mises en page, ce qui est différent de la mise en page HTML/CSS traditionnelle utilisée par React.

Composants Spécifiques à la Plate-forme : Dans React Native, vous pouvez avoir besoin d'utiliser des composants spécifiques à la plate-forme pour des fonctionnalités spécifiques à iOS ou Android, ce qui n'est pas nécessaire dans React.

Performances et Optimisations : En raison des différences dans la manipulation de l'interface utilisateur native, les performances et les optimisations peuvent varier entre les deux environnements. Vous devez prendre en compte les spécificités de chaque plate-forme pour optimiser votre application.

En résumé, bien que React et React Native partagent des concepts et des bibliothèques communs, ils présentent des différences significatives en ce qui concerne les éléments d'interface, les styles, la gestion des événements et d'autres aspects liés à la création d'applications mobiles natives. Il est important de comprendre ces différences pour développer efficacement dans chacun de ces environnements.

- ce que devient et comment est interprêté le code javascript dans une application react native ❌ / ✔️
  Interprétation du Code JavaScript (✔️) :
Transformation en Code Natif : Lorsque vous écrivez du code JavaScript dans une application React Native, ce code n'est pas exécuté directement par un moteur JavaScript tel que V8 (comme c'est le cas pour les applications web). Au lieu de cela, le code JavaScript est transpilé en code natif spécifique à la plate-forme. Cela signifie que votre code JavaScript est converti en code natif correspondant à iOS (Objective-C ou Swift) ou Android (Java ou Kotlin).

Utilisation d'un Moteur JavaScript : React Native utilise un moteur JavaScript interne pour exécuter le code JavaScript transpilé. Par défaut, il utilise JavaScriptCore sur iOS et JavaScriptCore ou V8 sur Android, selon la configuration.

React Native Bridge : Pour communiquer entre le code JavaScript et les composants natifs, React Native utilise un "pont" (bridge). Ce pont permet aux composants JavaScript et natifs de s'envoyer des messages et de partager des données. Par exemple, lorsque vous créez un composant Text en JavaScript, il est traduit en un composant natif de texte sur l'écran de l'appareil via le pont.

Exécution du Code JavaScript (✔️) :
Exécution en Temps Réel : Le code JavaScript de votre application React Native est exécuté en temps réel pendant l'exécution de l'application. Cela signifie que toute modification apportée au code JavaScript peut être immédiatement prise en compte sans avoir besoin de recompiler l'application.

Hot Reloading : React Native prend en charge des fonctionnalités telles que le "Hot Reloading", ce qui signifie que vous pouvez voir les modifications apportées au code JavaScript reflétées instantanément dans l'application en cours d'exécution, accélérant considérablement le processus de développement.

Accès aux Fonctionnalités Natives (❌) :
Utilisation des Modules Nativement : Pour accéder à des fonctionnalités natives telles que la caméra, le GPS ou les notifications push, vous devez utiliser des modules écrits en langage natif (Objective-C/Swift pour iOS, Java/Kotlin pour Android). Ces modules peuvent être appelés à partir du code JavaScript via le pont React Native.

Modules Communautaires : La communauté React Native a développé de nombreux modules prêts à l'emploi pour accéder aux fonctionnalités natives, ce qui facilite l'intégration de ces fonctionnalités dans votre application JavaScript.

En résumé, le code JavaScript que vous écrivez dans une application React Native est transpilé en code natif spécifique à la plate-forme et interprété par un moteur JavaScript interne. Le pont React Native permet aux composants JavaScript et natifs de communiquer entre eux, tandis que les fonctionnalités natives sont généralement accessibles via des modules écrits en langage natif. Cela permet de créer des applications mobiles performantes et natives tout en utilisant principalement JavaScript pour le développement.

- les avantages et inconvénients de react native ❌ / ✔️
  Avantages de React Native (✔️) :
Développement Rapide : React Native permet un développement plus rapide grâce à la réutilisation de composants et de logique métier entre les plates-formes iOS et Android.

Partage de Code : Une grande partie du code source peut être partagée entre les versions iOS et Android de l'application, ce qui réduit les efforts de développement et les coûts.

Performance : Les applications React Native offrent des performances élevées grâce à la traduction du code JavaScript en code natif. Les applications sont proches des performances des applications natives.

Écosystème React : Les développeurs React peuvent facilement se familiariser avec React Native, car il utilise le même modèle de composants et la même philosophie de développement que React.

Hot Reloading : La fonction de "Hot Reloading" permet aux développeurs de voir instantanément les modifications apportées au code sans avoir à recompiler l'application, ce qui accélère le développement.

Grande Communauté : React Native bénéficie d'une grande communauté de développeurs, ce qui signifie que vous pouvez trouver de nombreux packages et ressources en ligne.

Inconvénients de React Native (❌) :
Fonctionnalités Natives Complexes : Pour certaines fonctionnalités natives complexes ou spécifiques à une plate-forme, vous devrez écrire des modules natifs personnalisés, ce qui peut augmenter la complexité du développement.

Taille de l'Application : Les applications React Native peuvent être plus volumineuses que les applications natives en raison de la nécessité d'inclure le moteur JavaScript et la bibliothèque React Native.

Limitations de Performance : Bien que les performances soient généralement bonnes, les applications React Native peuvent présenter des performances légèrement inférieures à celles des applications natives dans certains cas.

Dépendance de Facebook : React Native est géré par Facebook, ce qui signifie que l'avenir de la plate-forme dépend en partie de la stratégie de l'entreprise.

Documentation Hétérogène : La qualité de la documentation peut varier en fonction des packages et des modules que vous utilisez, ce qui peut rendre la recherche de solutions à certains problèmes plus difficile.

Ressources Limitées pour les Plates-formes Moins Courantes : Si vous envisagez de cibler des plates-formes moins courantes, telles que Windows ou Web, les ressources et la prise en charge peuvent être limitées par rapport aux plates-formes iOS et Android.

En fin de compte, le choix d'utiliser React Native dépend des besoins spécifiques de votre projet. Il offre une approche efficace pour le développement d'applications multiplateformes, mais il est important de peser ses avantages par rapport à ses inconvénients en fonction des caractéristiques uniques de votre application et de votre équipe de développement.
- la différence entre react native et expo ❌ / ✔️

  Différences entre React Native et Expo (❌ / ✔️) :
React Native (❌) :
Configuration et Personnalisation : React Native offre une flexibilité maximale pour configurer et personnaliser votre application. Vous avez un contrôle total sur les modules natifs et pouvez les personnaliser selon vos besoins.

Accès Natif Complet : Avec React Native, vous avez un accès complet à toutes les fonctionnalités et API natives d'Android et d'iOS. Cela signifie que vous pouvez intégrer des fonctionnalités complexes et spécifiques à une plate-forme sans restrictions majeures.

Liberté de Choix : Vous pouvez choisir les packages et les bibliothèques que vous souhaitez utiliser dans votre application sans restrictions imposées par Expo. Cela offre une grande flexibilité, mais peut également nécessiter plus de travail de configuration.

Expo (✔️) :
Simplicité de Démarrage : Expo est une plate-forme construite au-dessus de React Native qui simplifie considérablement le processus de démarrage. Vous n'avez pas besoin de configurer Xcode ou Android Studio, ce qui facilite la mise en route.

Accès Limité aux Modules Natifs : Expo limite l'accès aux modules natifs d'Android et d'iOS pour des raisons de sécurité et de stabilité. Cela signifie que certaines fonctionnalités avancées peuvent ne pas être accessibles.

Service Expo : Expo propose un service cloud qui facilite le déploiement et la mise à jour de votre application sans avoir à gérer des serveurs. Cela peut être un avantage pour les petits projets ou les développeurs individuels.

Expo SDK : Expo propose son propre ensemble de modules et d'API, appelé Expo SDK, qui facilite le développement d'applications en fournissant des fonctionnalités courantes prêtes à l'emploi.

En fin de compte, le choix entre React Native et Expo dépend de vos besoins et de votre niveau de contrôle sur l'application. Si vous avez besoin d'une personnalisation poussée et d'un accès complet aux modules natifs, React Native peut être la meilleure option. En revanche, si vous préférez une approche plus simple et rapide pour le développement d'applications, Expo peut être un excellent choix, en particulier pour les projets plus petits ou les prototypes.

- les principales briques qui composent react native (core components) ❌ / ✔️

  Les principales briques de React Native (Core Components) (✔️) :
React Native est une bibliothèque JavaScript qui permet de développer des applications mobiles natives pour Android et iOS en utilisant une syntaxe similaire à React. Ses principales briques, également appelées "core components", sont les éléments clés qui facilitent la création d'interfaces utilisateur riches et réactives. Voici quelques-unes de ces briques essentielles :

View :

La View est l'équivalent d'une boîte ou d'un conteneur qui permet de regrouper d'autres éléments.
Elle peut être utilisée pour créer des mises en page, des sections ou des conteneurs pour d'autres composants.
Text :

Le composant Text est utilisé pour afficher du texte à l'écran.
Il prend en charge la mise en forme du texte, comme la couleur, la taille de la police, et le poids de la police.
Image :

Le composant Image permet d'afficher des images à partir de différentes sources, telles que des fichiers locaux ou des URL distantes.
Il prend en charge le redimensionnement et le chargement progressif des images.
TextInput :

TextInput est utilisé pour capturer la saisie de l'utilisateur, que ce soit du texte simple, des mots de passe, ou des champs de recherche.
Il peut être contrôlé et surveillé à l'aide d'états.
ScrollView :

Le composant ScrollView permet de créer des listes défilantes ou des vues défilantes pour afficher du contenu qui ne tient pas entièrement à l'écran.
Il prend en charge le défilement horizontal et vertical.
TouchableOpacity :

TouchableOpacity est un composant qui ajoute un effet d'opacité lorsque l'utilisateur appuie dessus, ce qui le rend idéal pour les boutons et les éléments interactifs.
FlatList :

FlatList est utilisé pour afficher des listes de données dynamiques et optimisées en termes de performances. Il permet de faire défiler de longues listes sans consommer trop de mémoire.
StyleSheet :

StyleSheet est un module qui permet de créer des feuilles de style pour les composants React Native. Il offre un moyen optimisé de définir des styles en utilisant JavaScript.
Navigation :

React Native offre plusieurs solutions de navigation, notamment React Navigation, qui permet de gérer la navigation entre les écrans de l'application.
Autres composants :

En plus de ces composants de base, React Native propose de nombreux autres composants pour gérer la navigation, les animations, la caméra, la géolocalisation, etc.
En combinant ces core components avec JavaScript et React, les développeurs peuvent créer des interfaces utilisateur riches et réactives pour les applications mobiles natives, tout en partageant une grande partie du code entre les plates-formes Android et iOS. Cela permet de gagner du temps et des ressources lors du développement d'applications multiplateformes.

- comment écrire du style en react native ❌ / ✔️

  Écrire du style en React Native (✔️) :
L'écriture de styles en React Native est similaire à celle de CSS, mais elle utilise JavaScript au lieu de CSS traditionnel. Voici comment vous pouvez écrire du style pour vos composants React Native :

Styles en ligne (Inline Styles) :

Vous pouvez définir des styles directement dans la déclaration de votre composant en utilisant l'attribut style.
Les styles en ligne sont définis à l'aide d'un objet JavaScript où les clés sont des noms de propriétés de style, et les valeurs sont les valeurs correspondantes.
Exemple :

<View style={{ backgroundColor: 'blue', padding: 10 }}>
  <Text style={{ color: 'white', fontSize: 18 }}>Hello, React Native!</Text>
</View>
Styles externes (External Styles) :

Pour rendre le code plus propre et réutilisable, vous pouvez définir des styles dans un objet JavaScript séparé.
Vous importez ensuite ces styles et les utilisez dans vos composants en utilisant la propriété style.
Exemple :

// Définir des styles dans un fichier styles.js
const styles = {
  container: {
    backgroundColor: 'blue',
    padding: 10,
  },
  text: {
    color: 'white',
    fontSize: 18,
  },
};

// Dans votre composant
import styles from './styles';

<View style={styles.container}>
  <Text style={styles.text}>Hello, React Native!</Text>
</View>
Feuilles de style (StyleSheet) :

Pour améliorer les performances de l'application, il est recommandé d'utiliser l'objet StyleSheet fourni par React Native pour définir vos styles.
Vous créez un objet de style en utilisant StyleSheet.create et référencez ces styles dans vos composants.
Exemple :

// Définir des styles avec StyleSheet
import { StyleSheet } from 'react-native';

const styles = StyleSheet.create({
  container: {
    backgroundColor: 'blue',
    padding: 10,
  },
  text: {
    color: 'white',
    fontSize: 18,
  },
});

// Dans votre composant
<View style={styles.container}>
  <Text style={styles.text}>Hello, React Native!</Text>
</View>
Styles conditionnels :

Vous pouvez utiliser des expressions conditionnelles pour définir des styles en fonction de certaines conditions.
Par exemple, vous pouvez conditionner la couleur du texte en fonction d'une variable d'état.


<Text style={{ color: isDarkMode ? 'white' : 'black' }}>Thème sombre</Text>
Héritage de styles :

Les styles peuvent être hérités par les composants enfants, ce qui signifie que les styles définis sur un composant parent peuvent affecter ses enfants.
Vous pouvez également ajouter des styles supplémentaires aux enfants si nécessaire.


<View style={styles.container}>
  <Text style={styles.text}>Parent</Text>
  <Text style={{ ...styles.text, fontSize: 14 }}>Enfant</Text>
</View>
En utilisant ces techniques, vous pouvez personnaliser l'apparence de vos composants React Native et créer des interfaces utilisateur attrayantes pour vos applications mobiles.

- comment est géré le layout en react native ❌ / ✔️

Gestion du Layout en React Native (✔️) :
La gestion du layout en React Native est essentielle pour créer une interface utilisateur efficace et réactive. Voici comment elle est gérée :

Flexbox :

Le modèle de layout principal en React Native est basé sur Flexbox, tout comme en CSS. Cela signifie que vous utilisez des conteneurs flexibles (View) pour organiser vos éléments.

<View style={{ flexDirection: 'row', justifyContent: 'space-between' }}>
  <Text>Élément 1</Text>
  <Text>Élément 2</Text>
  <Text>Élément 3</Text>
</View>
Les propriétés flex telles que flexDirection, justifyContent, et alignItems sont couramment utilisées pour définir la disposition des éléments à l'intérieur des conteneurs flex.
Dimensions :

Vous pouvez définir les dimensions des éléments en utilisant les propriétés width et height. Vous pouvez utiliser des unités telles que px, dp, %, etc.

<View style={{ width: 200, height: 100 }}>
  {/* Contenu */}
</View>
Positionnement :

Les éléments peuvent être positionnés en utilisant des propriétés telles que position, top, bottom, left, et right.
Cependant, en Flexbox, la plupart du positionnement se fait automatiquement en fonction de la disposition des éléments dans le conteneur parent.

<View style={{ position: 'absolute', top: 10, left: 20 }}>
  {/* Contenu */}
</View>
Styles conditionnels :

Vous pouvez également gérer le layout de manière conditionnelle en fonction de l'état de votre application. Par exemple, vous pouvez conditionner l'affichage ou la position des éléments en fonction de variables d'état.

<View style={{ flex: isExpanded ? 1 : 0 }}>
  {/* Contenu */}
</View>
Réactivité :

React Native gère automatiquement le redimensionnement et la réorganisation des éléments lorsque l'orientation de l'appareil change ou lorsque le clavier est affiché/masqué. Vous pouvez réagir à ces changements en utilisant des gestionnaires d'événements.
Orientation et Adaptabilité :

Vous pouvez gérer différentes orientations de l'appareil en ajustant les styles en conséquence. Par exemple, vous pouvez utiliser Dimensions pour obtenir les dimensions actuelles de l'écran.

import { Dimensions } from 'react-native';
const { width, height } = Dimensions.get('window');
Bibliothèques de gestion du layout :

Pour simplifier la gestion du layout, vous pouvez utiliser des bibliothèques tierces telles que react-native-responsive-layout ou react-native-extended-stylesheet qui offrent des fonctionnalités supplémentaires pour créer des layouts réactifs.
En utilisant ces concepts et techniques, vous pouvez créer des mises en page flexibles et réactives pour vos applications React Native, adaptées à une variété de tailles d'écran et d'orientations.

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️
import React from "react";
import {
  Text,
  StyleSheet,
  View,
  SafeAreaView,
  ScrollView,
  RefreshControl,
} from "react-native";
import { GET_USER } from "../../src/gql/UserGql";
import { useQuery } from "@apollo/client";
import { UserProfile } from "../../src/types/UserType";
import { Logs } from "expo";
import ModalDeleteUser from "./components/ModalDeleteUser";
import ModalUpdatePasswordUser from "./components/ModalUpdatePassword";
import UpdateInfosUser from "./components/UpdateInfosUser";
import useLoginContext from "../../src/hooks/useLoginContext";
import Logout from "./components/Logout";
Logs.enableExpoCliLogging();

export default function Profil() {
	const [refreshing, setRefreshing] = React.useState(false);
	const { userId } = useLoginContext();
	const onRefresh = React.useCallback(() => {
		setRefreshing(true);
		refetch();
		setTimeout(() => {
			setRefreshing(false);
		}, 2000);
	}, []);

	const {
		data: user,
		loading,
		error,
		refetch,
	} = useQuery<UserProfile>(GET_USER, { variables: { userId: userId } });

	if (!user) {
		return <Text>Il y a eu un probleme...</Text>;
	}

	if (error) {
		return <Text>Erreur : {error.message}</Text>;
	}

	if (loading) {
		return <Text>Fetching data...</Text>;
	}

  return (
    <>
      <ScrollView
        refreshControl={
          <RefreshControl refreshing={refreshing} onRefresh={onRefresh} />
        }
      >
        <View style={styles.container}>
          <Text style={styles.title}>Mon profil</Text>
          <View style={styles.card}>
            <Text style={styles.text}>Informations Personelles</Text>
            <SafeAreaView>
              <UpdateInfosUser
                userId={userId}
                refetch={refetch}
                styles={styles}
                user={user}
              />
            </SafeAreaView>
          </View>
          <View style={styles.card}>
            <Text style={styles.text}>Mot de passe</Text>
            <SafeAreaView>
              <ModalUpdatePasswordUser
                userId={userId}
                refetch={refetch}
                styles={styles}
              />
            </SafeAreaView>
          </View>
          <Logout />
          <ModalDeleteUser userId={userId} styles={styles} />
        </View>
      </ScrollView>
    </>
  );
}

const styles = StyleSheet.create({
  container: {
      flex: 0.5,
      justifyContent: "center",
      backgroundColor: "#D7CBB5",
  },
  card: {
      margin: 30,
      backgroundColor: "#fff",
      padding: 20,
  },
  text: {
      paddingTop: 20,
      textAlign: "center",
      fontWeight: "bold",
      fontSize: 15,
      marginBottom: 10,
  },
  textError: {
      paddingTop: 20,
      textAlign: "center",
      fontWeight: "bold",
      fontSize: 15,
      marginBottom: 10,
      color: "red",
  },
  input: {
      height: 40,
      margin: 12,
      borderWidth: 1,
      padding: 10,
      borderColor: "#7ED957",
      marginTop: 10,
      marginBottom: 10,
      borderRadius: 10,
  },
  title: {
      fontSize: 35,
      color: "#3C8962",
      textAlign: "center",
  },
  button: {
      marginLeft: 50,
      marginRight: 50,
      backgroundColor: "#A98E60",
      borderRadius: 10,
      elevation: 2,
      width:200
  },
  centeredView: {
      flex: 1,
      justifyContent: "center",
      alignItems: "center",
      marginTop: 22,
  },
  modalView: {
      margin: 20,
      backgroundColor: "white",
      borderRadius: 20,
      padding: 35,
      alignItems: "center",
      shadowColor: "#000",
      shadowOffset: {
          width: 0,
          height: 2,
      },
      shadowOpacity: 0.25,
      shadowRadius: 4,
      elevation: 5,
  },
  buttonOpen: {
      backgroundColor: "#A98E60",
  },
  buttonClose: {
      backgroundColor: "#A98E60",
  },
  textStyle: {
      color: "#7ED957",
      fontWeight: "bold",
      textAlign: "center",
  },
  modalText: {
      marginBottom: 15,
      textAlign: "center",
  },
});

Importation de composants : Le code commence par l'importation de plusieurs composants React Native nécessaires à la construction de l'écran, notamment Text, StyleSheet, View, SafeAreaView, ScrollView, et RefreshControl.

Gestion du Layout :

Le layout est géré en utilisant des composants tels que View, SafeAreaView, et ScrollView pour structurer la mise en page.
Les styles sont définis à l'aide de l'objet styles créé avec StyleSheet.create(). Ces styles sont ensuite appliqués aux éléments de l'interface utilisateur pour spécifier la mise en page, les couleurs et la typographie.
Récupération de données :

Les données du profil utilisateur sont récupérées en utilisant useQuery du client Apollo. Cela permet de récupérer les informations utilisateur à partir du serveur en utilisant la requête GraphQL GET_USER.
Gestion de l'état :

L'état de rafraîchissement (refreshing) est géré à l'aide de l'état local React (useState). Il est utilisé pour indiquer quand l'utilisateur effectue un geste de tirage vers le bas pour rafraîchir la page.
Gestion des événements :

Lorsque l'utilisateur effectue un geste de tirage vers le bas pour rafraîchir (onRefresh), une fonction est déclenchée pour actualiser les données en appelant refetch et en définissant l'état de rafraîchissement à true.
Affichage conditionnel :

Le code gère plusieurs scénarios, tels que la récupération des données en cours (loading), les erreurs (error), ou l'affichage des informations de l'utilisateur.
Modularité :

Le code est bien structuré en utilisant des composants React Native réutilisables tels que ModalDeleteUser, ModalUpdatePasswordUser, et UpdateInfosUser. Cela améliore la lisibilité et la maintenance du code.
Utilisation d'Expo :

Le code importe également Logs d'Expo pour activer les journaux de l'application.
En résumé, ce code illustre comment développer un écran de profil utilisateur en React Native en utilisant des concepts tels que la gestion du layout, la récupération de données à partir d'une API GraphQL, la gestion de l'état, la gestion des événements, et la modularité. C'est un exemple de mise en œuvre des principes de développement que j'ai expliqués précédemment.
### Utilisation dans un projet ❌ / ✔️

https://github.com/Timothee68/Wild-Carbon-Mobile

Description :

### Utilisation en production si applicable❌ / ✔️
https://github.com/Timothee68/Wild-Carbon-Mobile
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
