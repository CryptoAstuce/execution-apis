# 5. Engine API et passage de payloads

Le namespace engine relie le client consensus au client d’exécution. Le consensus demande au moteur de préparer un payload, puis lui soumet un payload proposé afin de vérifier qu’il respecte les règles d’exécution.

engine_forkchoiceUpdated reçoit la tête choisie, la tête finalisée et parfois des contraintes de construction. Le client d’exécution répond avec un statut et, selon le cas, un identifiant de payload à récupérer.

engine_getPayload restitue le contenu préparé ; engine_newPayload vérifie un bloc reçu. Les versions V1 à V5 visibles dans le dépôt représentent l’évolution des champs nécessaires aux mises à niveau d’Ethereum.

Les réponses distinguent notamment VALID, INVALID et SYNCING. Cette distinction permet au consensus de décider s’il doit poursuivre, corriger son choix ou attendre que l’exécution rattrape la chaîne.

La séparation clarifie les responsabilités : le consensus choisit la chaîne, l’exécution calcule les transitions d’état.

Suite : [Versionnement, erreurs et limites](06-versionnement-erreurs-limites.md).
