# Integration continue

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les enjeux de l'integration continue ✔️
    détection des erreurs, amélioration de la qualité du code, facilitation de la collaboration
- la mise en place d'une github action  ✔️
    fichier workflow en yaml, définir les étapes dans ce fichier (runs-on: décide sur quelle machine virtuelle le code va tourner, steps: toutes les étapes par lesquelles on souhaite passer)

## 💻 J'utilise

### Un exemple personnel commenté  ✔️

name: jest-ci-wild-carbone

<!-- les étapes se réalisent au moment où l'ont crée une pull request -->
on: pull_request

jobs:

<!-- le job test front s'effectue sur une machine virtuelle avec le système d'exploitation Ubuntu -->
  test-front:
    runs-on: ubuntu-latest

<!-- toutes les étapes du job -->
    steps:
<!-- récupère le code source qui sera testé  -->
      - name: Check out code
        uses: actions/checkout@v4
<!-- change de répertoire de travail pour aller dans la partie 'front' du projet -->
      - name: Goto front
        run: cd front && npm i
<!-- vérifie le code Typescript (--noEmit fait en sorte qu'aucun fichier ne soit généré) -->
      - name: Check TS
        run: cd front && npx tsc --noEmit
<!-- cette étape construit l'application -->
        run: cd front && npm run build
<!-- cette étape lance les tests  dans le répertoire front -->
      - name: run tests
        run: cd front && npm test

### Utilisation dans un projet  ✔️

https://github.com/AlexisFaugeroux/wild-carbon/
Description : utilisation de CI sur le projet d'école Wild Carbon

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- https://jestjs.io/docs/getting-started
- documentation de jest

- https://jestjs.io/docs/mock-function-api#methods
- méthodes d'implémentation de mocks dans les tests

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
