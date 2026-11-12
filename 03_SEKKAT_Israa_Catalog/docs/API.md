# API Catalog

Toutes les réponses d'erreur : `{ "message": "...", "requestId": "..." }`.
200 = succès ; 400 = entrée invalide ; 401 = session absente/invalide ; 403 = propriétaire/acteur interdit ; 404 = ressource absente ; 409 = conflit métier ; 503 = service dépendant indisponible.

| Service | Methode / chemin | Entree | Sortie |
|---|---|---|---|
| Catalog | GET /products | public | tableau de produits |
| Catalog | GET /products/{id} | public | id,name,category,price,image,description |

GET /health est public et renvoie le nom du service et son etat.

