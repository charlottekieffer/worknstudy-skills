# Tester son application

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les tests unitaires  ✔️
    on test de manière isolée les composants individuels d'une application. Les composants peuvent être des fonctions, des méthodes, des classes...

- les mocks  ✔️
    il s'agit d'un objet simulé utilisé pour remplacer un composant réel dans le cadre d'un test

- les tests d'integration  ✔️
    s'assurent que tous les composants d'une application fonctionnent correctement ensemble

- les tests de bout en bout (end to end)  ✔️
    vérifient que l'application fonctionne correctement depuis l'interface utilisateur jusqu'aux couches d'infrastructure, en passant par toutes les intéractions entre composants

- le TDD ✔️
    Test-Driven Development: méthodologie où l'ont écrit d'abord les tests avant le code de production: écriture du test -> écriture du code (en mvp) -> refacto

- les tests par snapshot ✔️
    On capture et compare des "instantanés" (snapshots) des éléments de l'interface utilisateur pour détecter les changements non intentionnels

## 💻 J'utilise

### Un exemple personnel commenté ✔️

describe('carbonCard', () => {
<!-- on vérifie si le composant 'CarbonCard' affiche un titre. -->
  it('should display a title', () => {

<!--on rend le composant en lui passant un titre -->
    render(<CarbonCard title="Ceci est un titre pollueur">Text</CarbonCard>);

<!-- on vérifie que le titre est présent dans le rendu -->
    expect(screen.getByText('Ceci est un titre pollueur')).toBeInTheDocument();
  });

});

### Utilisation dans un projet  ✔️

https://github.com/AlexisFaugeroux/wild-carbon

Description :

### Utilisation en production si applicable❌ 
[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ 

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
