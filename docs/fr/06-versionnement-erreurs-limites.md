# 6. Versionnement, erreurs et limites

Les interfaces évoluent par versions plutôt que par rupture globale. Les suffixes V1, V2 et suivants rendent explicites les changements de payload, de preuve ou de règle introduits par les mises à niveau du protocole.

Les fichiers d’erreurs regroupent les fautes RPC, les erreurs d’exécution, les problèmes de gas, les erreurs de transaction pool et les erreurs propres aux payloads. Un client compatible doit préserver leur sens, pas seulement leur code numérique.

La spécification ne garantit ni la disponibilité d’une méthode sur tous les nœuds, ni une performance identique, ni une finalité applicative. Une réponse valide décrit l’état observé par ce client à cet instant.

Périmètre : ce parcours traduit l’architecture et les contrats présents dans src/, docs-api/ et les exemples de tests du dépôt. Aucune installation, compilation ou exécution n’a été effectuée. Pour vérifier le comportement concret, consulter la suite de tests officielle du dépôt.

Retour : [sommaire du parcours](README.md).
