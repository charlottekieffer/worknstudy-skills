# REST API

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les verbes HTTP  ✔️
    Ils définissent le type d'opération que le client souhaite effectuer sur une ressource (GET, POST, PUT, DELETE)

- les statuts HTTP  ✔️
    codes renvoyés par un serveur en réponse à une requête (ex: 404 la ressource n'a pas été trouvée)

- les endpoints  ✔️
    c'est une ressource spécifique ou un point d'accès particulier dans une API qui peut être identifiée par une URL, ils permettent de structurer l'accès aux ressources 

- CORS ❌ / ✔️

- la nomenclature recommandée pour les routes ✔️
    

## 💻 J'utilise

### Un exemple personnel commenté  ✔️

<!-- exemple de création d'un "skill" dans le cadre d'une architecture REST -->

    create: async (req, res) => {
        try {
            await dataSource            // on requête la base de données
            .getRepository(Skill)       // on vise la table "Skill"
            .save(req.body);            // on enregistre l'information
            res.send("Created skill");  // on renvoit un message à la création de la donnée
            
<!-- le catch existe pour les cas d'erreurs -->

        } catch(error) {
            console.log(error);
            res.send("Error while creating skill");
            }
    }

### Utilisation dans un projet  ✔️

https://github.com/charlottekieffer/wild-book-typescript/blob/main/backend/src/controller/wilder.ts

Description : architecture REST dans un exercice

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- https://lo-victoria.com/introduction-to-cross-origin-resource-sharing-cors
- un article sur le fonctionnement de CORS

- https://blog.nicolashachet.com/developpement-php/larchitecture-rest-expliquee-en-5-regles/
- un article sur l'architecture REST de base 


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
