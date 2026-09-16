# 2. JSON-RPC et modèle de données

Les méthodes d’exécution sont exposées comme des appels JSON-RPC. Une requête porte un identifiant, un nom de méthode et une liste de paramètres ; la réponse renvoie soit un résultat, soit une erreur structurée.

Les schémas de src/schemas/ jouent le rôle de vocabulaire commun. Ils décrivent les blocs, transactions, reçus, comptes, filtres et types de base comme les quantités hexadécimales et les valeurs binaires.

Le format hexadécimal est essentiel : il évite les ambiguïtés de taille et d’encodage entre clients écrits dans des langages différents. Les champs optionnels permettent aussi de faire évoluer l’API sans casser les anciennes méthodes.

Le dépôt contient également une description GraphQL et des fichiers générés pour la documentation. La source de vérité reste la spécification versionnée, pas une copie d’interface produite automatiquement.

Suite : [Lire l’état et les blocs](03-etat-blocs.md).
