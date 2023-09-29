# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les différences et points communs entre du code react et du code react native ✔️
  -> points communs: composants, même syntaxe, states et props, cycle de vie des composants
  différences: plateforme ciblée (iOS et Android), composants natifs au lieu de composants HTML, styles, navigation..

- ce que devient et comment est interprêté le code javascript dans une application react native ✔️
  -> le code JavaScript dans une application React Native est responsable de la logique métier, de la construction de l'interface utilisateur et de l'interaction avec les composants natifs du système d'exploitation. Il est interprété par le moteur JavaScript intégré à l'application,

- les avantages et inconvénients de react native ✔️
  -> Avantages: dev multiplateformes, perfs élevées , hot reload... Inconvénients: moins performant pour les applications très gourmandes en ressources,
  accès natif complexe pour des fonctionnalités spécifiques, mises à journécessitent ajustements dans le code...

- la différence entre react native et expo ✔️
  -> plus de flexibilité avec react native (ex, bibliothèques tierces) mais demande une gestion plus avancée (mises à jour manuelles, gestion de fichiers
  d'installation Android et iOS). Expo simplifie le processus de dev et de distributin mais moins flexible pour les besoins avancés.

- les principales briques qui composent react native (core components) ✔️
  -> View, Text, Image, Scrollview, Button etc...

- comment écrire du style en react native ✔️
- comment est géré le layout en react native ✔️
  -> flexbox

## 💻 J'utilise

### Un exemple personnel commenté ✔️

<!-- createBottomNavigator permet de créer une barre de navigation en bas de page -->

import { createBottomTabNavigator } from "@react-navigation/bottom-tabs";
import { TouchableOpacity, Image, StyleSheet } from "react-native";
import Ionicons from "@expo/vector-icons/Ionicons";

import Article from "../screens/Article/index";
import Home from "../screens/Home/index";
import Friends from "../screens/Friends";

const Tab = createBottomTabNavigator();
export default function MyTabs({ navigation }: { navigation: any }) {
const navigateToProfil = () => {
navigation.navigate("Profil");
};

return (
<Tab.Navigator

<!-- code pour définir l'affichage et les options d'affichage des icones du menu selon la page sur laquelle on se trouve-->

      screenOptions={({ route }) => ({
        tabBarIcon: ({ focused, color, size }) => {
          let iconName: string = "";
          if (route.name === "Home") {
            iconName = focused ? "home" : "home-outline";
          } else if (route.name === "Article") {
            iconName = focused ? "newspaper" : "newspaper-outline";
          } else if (route.name === "Friends") {
            iconName = focused ? "people" : "people-outline";
          }
          return <Ionicons name={iconName as any} size={size} color={color} />;
        },

<!-- tout ce qui est 'header' définit ce qui s'affiche en haut de page -->

        headerStyle: {
          backgroundColor: "#D7CBB5",
        },
        headerTitle: () => (
          <Image
            source={require("../assets/leaf.png")}
            style={styles.logoCentral}
          />
        ),
        headerTitleAlign: "center",
        headerRight: () => (
          <TouchableOpacity
            onPress={navigateToProfil}
            style={styles.logoProfil}
          >
            <Ionicons
              size={30}
              color={"#3C8962"}
              name="person-sharp"
            ></Ionicons>
          </TouchableOpacity>
        ),

<!-- Définit les couleurs d'onglets actifs et inactifs -->

        tabBarActiveTintColor: "#7ED957",
        tabBarInactiveTintColor: "gray",
      })}
    >

<!-- screen: chaque page de l'appli, par défaut on est sur Home, Tab permet la navigation enre les screens -->

      <Tab.Screen
        name="Home"
        component={Home}

<!-- cette option démonte l'écran lorsque l'utilisateur quitte cet écran (démoter= composants retirés de la mémoire ) -->

        options={{ unmountOnBlur: true }}
      />
      <Tab.Screen name="Article" component={Article} />
      <Tab.Screen name="Friends" component={Friends} />
    </Tab.Navigator>

);
}

<!-- Stylesheet est une classe fournie par react native qui optimise la gestion des styles.
Quand on appelle Stylesheet.create() on crée un nouvel objet de feuille de style. Entre les accolades on met tout le style que l'on veut-->

const styles = StyleSheet.create({
container: {
flex: 1,
justifyContent: "center",
},
title: {
textAlign: "center",
backgroundColor: "#D644DB",
fontWeight: "bold",
fontSize: 15,
},
logoHeader: {
width: 40,
height: 40,
marginLeft: 20,
},
logoProfil: {
marginRight: 20,
},
logoCentral: {
width: 90,
height: 60,
marginBottom: 15,
},
});

### Utilisation dans un projet ✔️

[lien github] https://github.com/Timothee68/Wild-Carbon-Mobile

Description :
Adaptation de notre projet annuel en application React native

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- https://reactnavigation.org/
- documentation oficielle de react navigation

## 🚧 Je franchis les obstacles

Description: La navigation depuis le screen DeleteUser de mon application ne fonctionnait pas
Grâce aux recherches et à l'aide de mes camarades nous avons trouvé d'où venait le problème: l'affichage de certaines pages de navigation était conditionnel.
L'ajout de ce code dans le "handleDeleteUSer" permet de remettre les données de l'utilisateur à zero pour qu'il puisse naviger vers la page voulue:

<!-- ferme la modale sur laquelle on est -->

            setModalDeleteVisible(false);

<!-- met à jour l'état de userId: utilisateur effacé -->

    		setUserId("");

<!-- même chose que pour userId -->

    		setUserToken("");

<!-- l'utilisateurn'est plus connecté -->

    		setIsLoggedIn(false);

<!-- renvoie vers le screen "Login" -->

    		navigation.navigate("Login");

### Point de blocage ❌

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
