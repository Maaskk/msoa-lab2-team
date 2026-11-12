# LAB 2 : parties séparées par membre

Chaque dossier contient uniquement le microservice attribue au membre, ses instructions et une copie de l'infrastructure commune necessaire a son execution. Aucun dossier ne contient les cinq autres services.

| Dossier | Membre | Service | Port |
|---|---|---|---|
| 01_ASHAD_Ossama_Orders | ASHAD Ossama | orders | 8084 |
| 02_ELHADDAJI_Hamza_Auth | Elhaddaji Hamza | auth | 8081 |
| 03_SEKKAT_Israa_Catalog | Sekkat Israa | catalog | 8082 |
| 04_AYAR_Mouhcine_Inventory | Mouhcine Ayar | inventory | 8083 |
| 05_MSOUHLI_Rahil_Payments | Rahil Msouhli | payments | 8085 |
| 06_KARANY_Mohamed_Amine_Shipping | Karany Mohamed Amine | shipping | 8086 |

## Utilisation

Décompresser le ZIP. Donner a chaque membre son dossier. Dans chaque dossier : copier .env.example en .env, choisir une même INTERNAL_KEY d'au moins 32 caracteres pour tout le groupe et lancer npm start avec Node.js 24+.

Les parcours de commande complets demandent les six services actifs. Chaque dossier peut etre extrait et lance sans le dossier parent ; /health fonctionne sans autre service. Catalog et Inventory incluent leur jeu de produits initial. Les copies de runtime.mjs doivent rester compatibles.

Le frontend de groupe et le rapport original restent dans Downloads/LAB2_MSOA. Ils ne sont pas dupliques dans les parties individuelles. Le partage des sources n'exige aucun mot de passe de compte et aucune base contenant des sessions nest fournie.

Manifest_Source.json indique les fichiers extraits et leurs SHA-256. La partie ASHAD Ossama contient egalement des tests de contrat avec doublures HTTP ; ces tests ne remplacent pas la verification avec les autres services réels.

## Depot GitHub individuel

La partie Orders d'ASHAD Ossama est publiee dans un depot prive : https://github.com/Maaskk/msoa-orders-service
Les autres parties restent uniquement dans leurs dossiers respectifs.
