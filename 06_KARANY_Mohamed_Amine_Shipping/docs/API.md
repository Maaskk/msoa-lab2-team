# API Shipping

Toutes les réponses d'erreur : `{ "message": "...", "requestId": "..." }`.
200 = succès ; 400 = entrée invalide ; 401 = session absente/invalide ; 403 = propriétaire/acteur interdit ; 404 = ressource absente ; 409 = conflit métier ; 503 = service dépendant indisponible.

| Service | Methode / chemin | Entree | Sortie |
|---|---|---|---|
| Shipping | GET /api/shipments | session | expéditions de l'utilisateur |
| Shipping | GET /api/shipments/order/{orderId} | session propriétaire | expédition |
| Shipping | POST /api/shipments | orderId,address conforme à la commande | id,orderId,userId,address,trackingNumber,status,createdAt,updatedAt |
| Shipping | PATCH /api/shipments/{id}/status | status | expédition synchronisée avec Orders |

GET /health est public et renvoie le nom du service et son etat.

POST /internal/shipments/{orderId}/prepare, /advance et /cancel exigent X-Internal-Key. Progression : PREPARING, SHIPPED, IN_TRANSIT, DELIVERED.
