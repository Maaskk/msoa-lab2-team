# API Auth

Toutes les réponses d'erreur : `{ "message": "...", "requestId": "..." }`.
200 = succès ; 400 = entrée invalide ; 401 = session absente/invalide ; 403 = propriétaire/acteur interdit ; 404 = ressource absente ; 409 = conflit métier ; 503 = service dépendant indisponible.

| Service | Methode / chemin | Entree | Sortie |
|---|---|---|---|
| Auth | POST /api/auth/register | name,email,password (min 6) | id,name,email,role |
| Auth | POST /api/auth/login | email,password | user,token |
| Auth | GET /api/auth/me | Bearer token | utilisateur public |
| Auth | POST /api/auth/logout | Bearer token | success |

GET /health est public et renvoie le nom du service et son etat.

