# OAS TD2 responses

**<i>Ce fichier contient les réponses pour les questions evoquées à des dernières parties du TD2 du projet OpenAPI Specification (OAS) !</i>**

<br/>

### Est ce qu’on peut gérer la pagination à travers les entêtes de la requête ? Justifiez votre réponse:

En général, gérer la pagination à travers les entêtes de la requête n'est pas vraiment une bonne pratique mais **OUI** c'est possible. La gestion de la pagination se fait à travers de paramètres de requête. Les paramètres de requête sont directement liés aux donnée demandées, pour avoir une API plus conviviale pour les devs

**Exemple de pagination avec des paramètres de requête:**

- `GET /books?page=2&pageSize=10` : Récupère la deuxième page de 10 éléments par page dans une liste de livres
  <br/>

Bien que la gestion de la pagination à travers l'entête est possible, comme je l'ai dis bien avant, c'est moins courante et peut compliquer la conception de l'API

**Exemple de pagination avec dans l'entête de requête:**

```http
GET /books
Header: X-Page: 2
Header: X-PageSize: 10
```

<br/>

### Est ce qu’on doit gérer la pagination  à travers les entêtes de la requête ? Justifiez votre réponse:
**NON**, on ne doit pas gérer la pagination à travers l'entête de la requête comme je l'ai dans la réponse de la précédente question. Ce n'est pas recommandé. Il est généralement préférable de suivre les conventions RESTful et d'utiliser des paramètres de requête pour la pagination. Cela rend l'API plus conviviale, plus intuitive et plus compatible avec les pratiques courantes de conception d'API.
