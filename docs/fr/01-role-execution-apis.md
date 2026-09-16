# 1. Le rôle des Execution APIs

Ethereum sépare aujourd’hui le client consensus, qui décide de la chaîne à suivre, et le client d’exécution, qui interprète les transactions et maintient l’état. Les Execution APIs sont le contrat qui permet à ces deux mondes de dialoguer.

Le dépôt décrit ces interfaces sous forme de schémas YAML dans src/. Les méthodes sont regroupées par domaine : eth pour les appels RPC usuels, engine pour le pilotage par le consensus, txpool pour la file d’attente et debug pour l’inspection.

Une API n’est pas un nœud : elle définit les messages, les paramètres et les réponses qu’un client doit comprendre. Cette distinction rend les implémentations interchangeables et permet aux clients Ethereum de rester compatibles.

La documentation française de ce parcours traduit les mécanismes présents dans le dépôt, sans exécuter le logiciel ni affirmer un résultat de test.

Suite : [JSON-RPC et modèle de données](02-json-rpc-modele-donnees.md).
