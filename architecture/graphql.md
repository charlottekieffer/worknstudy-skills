# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL ✔️
- les besoins auxquels répond GraphQL ✔️
- la définition d'un schéma
- Query  ✔️
- Mutation  ✔️
- Subscription ❌ / ✔️

## 💻 J'utilise
GraphQL

### Un exemple personnel commenté  ✔️
'
// ici nous avons une requête simple de récupération d'un seul "book", l'argument 'bookId' permet de le récupérer par son id.
// getRepository nous permet de récupérer l'information depuis la table 'Book', le findOneByOrFail permet de récupérer un book par son id, ou renvoie un message d'erreur si la récupération est impossible. 

  @Query(() => Book)
  async getBook(@Arg('bookId') id: number): Promise<Book> {
    const book = await dataSource.getRepository(Book).findOneByOrFail({ id });

    return book;
  }
### Utilisation dans un projet ❌ / ✔️

https://github.com/AlexisFaugeroux/wild-carbon/blob/feature/resolver/back/src/resolver/CategoryResolver.ts

Description : toutes les Querys et Mutations la partie "Category" de notre projet

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Mon entreprise n'utilise pas graphQL

Description :

## 🌐 J'utilise des ressources

### Titre

- https://www.redhat.com/en/topics/api/what-is-graphql
- Une présentation globale de graphQL avec des exemples

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
