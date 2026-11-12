# API Payments

Toutes les réponses d'erreur : `{ "message": "...", "requestId": "..." }`.
200 = succès ; 400 = entrée invalide ; 401 = session absente/invalide ; 403 = propriétaire/acteur interdit ; 404 = ressource absente ; 409 = conflit métier ; 503 = service dépendant indisponible.

| Service | Methode / chemin | Entree | Sortie |
|---|---|---|---|
| Payments | GET /api/payments | session | paiements de l'utilisateur |
| Payments | GET /api/payments/order/{orderId} | session propriétaire | paiement |
| Payments | POST /api/payments | orderId,method:CARD ou CASH | id,orderId,userId,amount,method,status,createdAt |

GET /health est public et renvoie le nom du service et son etat.

POST /internal/payments/{orderId}/capture et POST /internal/payments/{orderId}/refund exigent X-Internal-Key. Il s'agit de simulations sans carte ni transaction bancaire.
