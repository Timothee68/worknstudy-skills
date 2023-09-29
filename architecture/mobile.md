# Technologies d'applications mobiles

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les différences entre les webapps, les applications hybrides et natives ❌ / ✔️
**Web Applications :**

- ✔️ Facilité de développement : Les web applications sont généralement plus faciles à développer car elles utilisent des technologies web standard telles que HTML, CSS et JavaScript.
- ✔️ Multiplateforme : Une seule base de code peut être utilisée sur plusieurs plates-formes grâce à l'accès via un navigateur web.
- ❌ Performances limitées : Les performances des web applications peuvent être limitées en comparaison avec les applications natives en raison de l'exécution dans un navigateur.
- ❌ Accès au matériel limité : Les web applications ont un accès limité au matériel du dispositif, tel que l'appareil photo ou les capteurs.
- ❌ Connectivité requise : En général, une connexion Internet est nécessaire pour accéder aux web applications.

**Applications Hybrides :**

- ✔️ Utilisation de technologies web : Les applications hybrides utilisent des technologies web telles que HTML, CSS et JavaScript pour le développement.
- ✔️ Accès au matériel : Les frameworks d'applications hybrides offrent un accès au matériel du dispositif via des plugins.
- ✔️ Multiplateforme : Une base de code peut être utilisée sur plusieurs plates-formes grâce à des frameworks tels que Apache Cordova ou React Native.
- ❌ Performances : Bien que meilleures que les web applications, les performances des applications hybrides peuvent être légèrement inférieures à celles des applications natives.

**Applications Natives :**

- ✔️ Performances optimales : Les applications natives sont optimisées pour la plate-forme spécifique sur laquelle elles sont développées, offrant ainsi les meilleures performances possibles.
- ✔️ Accès complet au matériel : Les applications natives ont un accès complet au matériel du dispositif, offrant ainsi une expérience utilisateur riche.
- ❌ Coût de développement plus élevé : Le développement d'applications natives peut être plus coûteux en raison de la nécessité de développer des versions distinctes pour chaque plate-forme.
- ❌ Temps de développement plus long : En raison de la nécessité de développer des versions distinctes pour chaque plate-forme, le temps de développement peut être plus long.
- ❌ Mises à jour séparées : Les mises à jour doivent être développées et publiées séparément pour chaque plate-forme.

En résumé, le choix entre une web application, une application hybride et une application native dépendra de nombreux facteurs, notamment les performances requises, le budget, les compétences techniques disponibles et les besoins spécifiques du projet. Chaque approche a ses avantages et ses inconvénients, et le choix final dépendra des priorités et des contraintes du projet.

- le fonctionnement d'une app React Native, ce qui sera en réalité produit et installé sur le téléphone de mes utilisateur·rices, comment le JS arrive à communiquer avec le natif ❌ / ✔️
  Fonctionnement d'une Application React Native :

Lorsqu'on aborde le fonctionnement d'une application React Native, il est essentiel de comprendre qu'il s'agit d'une technologie qui permet de développer des applications mobiles multiplateformes en utilisant principalement JavaScript. Voici comment cela se déroule :

Développement : Le processus commence par le développement de l'application. Les développeurs utilisent JavaScript, accompagné de technologies web familières telles que HTML et CSS, pour créer l'interface utilisateur de l'application. Ils ont également à leur disposition des composants et bibliothèques spécifiques à React Native qui facilitent l'accès aux fonctionnalités natives du téléphone.

Compilation : Une étape cruciale consiste à compiler le code JavaScript écrit par les développeurs. Cette compilation transforme le code JavaScript en code natif adapté à la plate-forme cible. Par exemple, pour iOS, le code JavaScript est transformé en code Objective-C ou Swift, tandis que pour Android, il devient du code Java ou Kotlin.

Installation : Ce qui est installé sur les téléphones des utilisateurs finaux, ce sont les fichiers binaires natifs résultants du processus de compilation. Pour Android, il s'agit d'un fichier APK, tandis que pour iOS, c'est un fichier IPA. Ces fichiers sont ce que les utilisateurs téléchargent depuis les boutiques d'applications respectives.

Exécution : Lorsqu'un utilisateur ouvre l'application sur son téléphone, c'est l'application native résultante qui s'exécute. Cette application utilise un moteur JavaScript intégré pour interpréter et exécuter le code JavaScript développé précédemment.

Communication entre JavaScript et le Natif :

Pour comprendre comment JavaScript communique avec le code natif dans le contexte de React Native, il est essentiel de considérer les éléments suivants :

Bridge JavaScript-Natif : React Native intègre un composant clé appelé le "Bridge JavaScript-Natif". Ce pont est responsable de la communication bidirectionnelle entre le code JavaScript et le code natif. Il gère le passage des données et des événements entre les deux environnements.

Modules Natifs : Il est possible de créer des modules natifs personnalisés en utilisant les langages natifs tels qu'Objective-C, Swift, Java ou Kotlin. Ces modules effectuent des opérations spécifiques au niveau natif et peuvent être appelés depuis le code JavaScript pour interagir avec le matériel du téléphone ou accéder à des fonctionnalités indisponibles via les bibliothèques React Native.

Bibliothèques React Native : Pour simplifier la communication entre le code JavaScript et les fonctionnalités natives courantes (comme la caméra, la géolocalisation, les notifications push, etc.), React Native propose des bibliothèques JavaScript spécifiques. Ces bibliothèques encapsulent la logique de communication avec le code natif via le pont JavaScript-Natif.

Communication Asynchrone : La communication entre JavaScript et le code natif est asynchrone par nature. Lorsqu'une méthode native est appelée depuis JavaScript, cela se fait de manière asynchrone, et les résultats sont renvoyés via des callbacks ou des promesses.

Interopérabilité : JavaScript et le code natif échangent des données sous forme de JSON. React Native gère automatiquement la conversion entre les types de données JavaScript et natifs.

En résumé, une application React Native combine le meilleur des deux mondes : une grande partie du développement en JavaScript, mais également la possibilité d'accéder aux fonctionnalités natives du téléphone. Cette interaction est rendue possible grâce au pont JavaScript-Natif et à des modules natifs personnalisés. Le résultat final est une application performante et réactive, disponible sur différentes plates-formes mobiles.

- quelles sont les différentes technologies (frameworks) existantes pour développer des apps mobiles ❌ / ✔️
  Les Différentes Technologies/Frameworks pour le Développement d'Applications Mobiles :

Lorsqu'il s'agit de développer des applications mobiles, il existe plusieurs technologies et frameworks parmi lesquels choisir. Chacun a ses avantages et ses inconvénients, et le choix dépend souvent des besoins spécifiques du projet. Voici un aperçu de ces différentes options :

1. Développement Natif (✔️) :

Langages : Pour iOS, on utilise principalement Objective-C ou Swift, tandis qu'Android utilise Java ou Kotlin.
Avantages : Performant, accès complet aux fonctionnalités natives, meilleure expérience utilisateur, idéal pour les applications complexes.
Inconvénients : Temps et coût de développement plus élevés, nécessite une expertise spécifique pour chaque plate-forme.
2. Développement Web (❌) :

Technologies : HTML, CSS, JavaScript.
Avantages : Développement multiplateforme, réutilisation du code web, coût réduit.
Inconvénients : Performance inférieure à celle du natif, accès limité aux fonctionnalités natives, expérience utilisateur moins fluide.
3. Applications Hybrides (✔️) :

Frameworks : Apache Cordova, Ionic, PhoneGap.
Avantages : Utilisation de technologies web familières, développement multiplateforme, réduction des coûts, accès partiel aux fonctionnalités natives via des plugins.
Inconvénients : Performance moins élevée que le natif, expérience utilisateur parfois moins fluide, dépendance aux mises à jour des frameworks.
4. React Native (✔️) :

Langage : JavaScript.
Avantages : Développement multiplateforme, partage de code entre iOS et Android, accès aux fonctionnalités natives via des modules natifs, performances proches du natif, large communauté et écosystème de bibliothèques.
Inconvénients : Certains composants personnalisés nécessitent du code natif, complexité accrue pour des fonctionnalités spécifiques.
5. Xamarin (✔️) :

Langage : C#.
Avantages : Développement multiplateforme, partage de code, accès complet aux fonctionnalités natives, performances élevées, intégration aisée avec les produits Microsoft.
Inconvénients : Complexité accrue pour les applications complexes, courbe d'apprentissage.
6. Flutter (✔️) :

Langage : Dart.
Avantages : Développement multiplateforme, performances élevées, interface utilisateur personnalisée, widgets riches, hot-reloading, croissance rapide de la communauté.
Inconvénients : Moins d'expérience dans l'écosystème par rapport aux autres, certaines bibliothèques tierces peuvent manquer.
7. Progressive Web Apps (❌/✔️) :

Technologies : HTML, CSS, JavaScript.
Avantages : Facilité de déploiement, aucune installation requise, compatibilité multiplateforme.
Inconvénients : Accès limité aux fonctionnalités natives (peut être amélioré avec les APIs de service workers), dépendance à une connexion Internet.
En résumé, le choix de la technologie ou du framework pour le développement d'applications mobiles dépend des exigences du projet, du budget, de la performance souhaitée et de la disponibilité des compétences. Chaque option a ses avantages et ses limites, et il est important de les peser soigneusement en fonction des besoins spécifiques de l'application.

- quels sont les principaux points d'attention entre le développement d'une app mobile ou desktop ❌ / ✔️
  Principaux Points d'Attention Entre le Développement d'une Application Mobile et d'une Application de Bureau :

Le développement d'applications, que ce soit pour mobile ou pour bureau, est une tâche complexe et exigeante qui nécessite une compréhension approfondie des besoins de l'utilisateur, des plateformes cibles et des technologies disponibles. Cependant, il existe des différences significatives entre le développement d'une application mobile et d'une application de bureau. Voici les principaux points d'attention à prendre en compte :

1. Taille de l'Écran (❌/✔️) :

Mobile : Les appareils mobiles ont des écrans plus petits, ce qui nécessite une conception d'interface utilisateur (UI) adaptée avec une disposition et des contrôles optimisés.
Desktop : Les ordinateurs de bureau ont des écrans plus grands, offrant plus d'espace pour afficher des informations. Cependant, la conception doit toujours être adaptée à différentes résolutions d'écran.
2. Interaction Tactile (❌/✔️) :

Mobile : Les appareils mobiles utilisent des écrans tactiles, ce qui nécessite une prise en charge des gestes, des interactions tactiles intuitives et des éléments de navigation adaptés.
Desktop : Les ordinateurs de bureau utilisent principalement une souris et un clavier pour l'interaction, ce qui permet des interactions plus précises. Les applications de bureau doivent prendre en charge ces dispositifs.
3. Plateformes et OS (❌/✔️) :

Mobile : Les applications mobiles sont généralement développées pour des plateformes spécifiques telles qu'Android et iOS. Cela nécessite une expertise dans les langages de programmation et les kits de développement logiciel (SDK) spécifiques à chaque plateforme.
Desktop : Les applications de bureau peuvent être développées pour différentes plateformes, notamment Windows, macOS et Linux. Des frameworks tels qu'Electron permettent de créer des applications multiplateformes.
4. Accessibilité (❌/✔️) :

Mobile : Les applications mobiles doivent prendre en compte l'accessibilité pour les utilisateurs ayant des besoins spécifiques, tels que la navigation vocale ou les gestes adaptés.
Desktop : Les applications de bureau doivent également être accessibles, mais les besoins peuvent varier en fonction du public cible.
5. Notifications et Contexte (✔️) :

Mobile : Les applications mobiles ont un accès plus facile aux notifications push, ce qui permet de fournir des informations en temps réel aux utilisateurs.
Desktop : Les applications de bureau peuvent offrir des notifications, mais elles sont généralement moins intrusives et dépendent davantage de l'interaction de l'utilisateur.
6. Conception de l'Interface Utilisateur (❌/✔️) :

Mobile : Les applications mobiles suivent souvent des directives de conception spécifiques à chaque plateforme (Material Design pour Android, Human Interface Guidelines pour iOS).
Desktop : Les applications de bureau peuvent avoir une plus grande liberté de conception, mais elles doivent toujours fournir une expérience utilisateur cohérente.
7. Performances et Ressources (❌/✔️) :

Mobile : Les appareils mobiles ont des ressources limitées en termes de CPU, de mémoire et de batterie, ce qui nécessite une optimisation rigoureuse de la performance.
Desktop : Les ordinateurs de bureau ont généralement plus de ressources, ce qui permet des fonctionnalités plus complexes et une meilleure qualité graphique.
En résumé, le développement d'applications mobiles et de bureau présente des différences importantes en termes de conception, d'interaction utilisateur, de plateformes cibles et de ressources matérielles. Les développeurs doivent tenir compte de ces différences pour créer des applications efficaces et conviviales pour leurs utilisateurs.

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

const Stack = createNativeStackNavigator();

export default function Login({ navigation }: { navigation: any }) {
	// Utilisation de l'hook useMutation pour gérer la mutation LOGIN
	const [login, { loading }] = useMutation(LOGIN, {
		onCompleted: async (data) => {
			if (data?.login && data.login.success) {
				setUserId(data.login.user.id);
				setUserToken(data.login.token);
				await saveUserTokenInLocalStorage({
					userToken: data.login.token,
					userId: data.login.user.id,
				});
				navigateToHome();
			} else {
				setErrorMessage("Identifiants invalides");
			}
		},
		onError: (error) => {
			console.error("Mutation error:", error);
		},
	});

	// Utilisation du contexte de connexion
	const { setIsLoggedIn, setUserToken, setUserId } = useLoginContext();

	// Fonction de navigation vers la page d'inscription
	const navigateToRegister = () => {
		navigation.navigate("Register");
	};

	// Fonction de navigation vers la page d'accueil
	const navigateToHome = () => {
		setErrorMessage(null);
		setIsLoggedIn(true);
		navigation.navigate("Tabs");
	};

	// États locaux pour les champs d'entrée et les messages d'erreur
	const [email, setEmail] = useState("");
	const [motDePasse, setMotDePasse] = useState("");
	const [errorMessage, setErrorMessage] = useState<string | null>(null);

	// Fonction pour gérer la soumission du formulaire de connexion
	const handleLogin = async () => {
		setErrorMessage("");
		await login({
			variables: {
				email: email,
				password: motDePasse,
			},
		});
	};

	return (
		<>
			<TouchableWithoutFeedback onPress={Keyboard.dismiss} accessible={false}>
				<SafeAreaView style={styles.container}>
					<Image
						source={require("../../assets/finalLogo.png")}
						resizeMode="contain"
						style={{ width: 300 }}
					/>
					<View style={styles.card}>
						<Text style={styles.title}>Se connecter</Text>
						<View>
							<TextInput
								placeholder="Email"
								style={styles.input_container}
								value={email}
								onChangeText={(text) => setEmail(text)}
							/>
							<TextInput
								placeholder="Mot de passe"
								style={styles.input_container}
								secureTextEntry={true}
								value={motDePasse}
								onChangeText={(text) => setMotDePasse(text)}
							/>
							{errorMessage ? (
								<Text style={styles.errorMessage}>{errorMessage}</Text>
							) : null}
							{loading ? (
								<Text style={styles.loadingMessage}>Loading...</Text>
							) : (
								<Button
									color="#7ED957"
									onPress={() => handleLogin()}
									title="Me connecter"
									containerStyle={styles.button}
								/>
							)}

							<Button
								containerStyle={styles.button}
								onPress={() => navigateToRegister()}
								title="Créer un compte"
							/>
						</View>
					</View>
				</SafeAreaView>
			</TouchableWithoutFeedback>
		</>
	);
}

const styles = StyleSheet.create({
	// Styles pour les éléments d'interface
});
### Utilisation dans un projet ❌ / ✔️

[[lien github](...)](https://github.com/Timothee68/Wild-Carbon-Mobile)

Description :
Ce code est un composant React Native qui représente l'écran de connexion d'une application mobile. Voici les points clés :

Il utilise React Navigation pour gérer la navigation entre les écrans de l'application.

Le composant utilise useMutation d'Apollo Client pour gérer la mutation de connexion (LOGIN) vers un serveur GraphQL.

Lorsque l'utilisateur se connecte avec succès, son jeton d'utilisateur est stocké localement, et il est redirigé vers la page d'accueil.

Les champs d'entrée pour l'email et le mot de passe, ainsi que les messages d'erreur, sont gérés à l'aide de l'état local.

La fonction handleLogin est déclenchée lorsque l'utilisateur appuie sur le bouton de connexion, envoyant les informations de connexion au serveur.

Les styles de l'interface utilisateur sont définis dans un objet styles à l'aide de StyleSheet.create pour une gestion efficace des styles.

Ce composant est un exemple d'écran d'authentification dans une application mobile développée avec React Native.

### Utilisation en production si applicable ❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources
Documentation officielle de React Native

React Native Express - Tutoriel interactif
Cours React Native sur Udemy
Cours React Native sur Coursera
Chaîne YouTube The Net Ninja - React Native Tutorial
Répertoire React Native Community sur GitHub
Stack Overflow - Questions et réponses sur React Native
Awesome React Native sur GitHub - Liste de projets open source

Expo - Explorez les projets et exemples
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
- J'ai ecrit un [article](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
