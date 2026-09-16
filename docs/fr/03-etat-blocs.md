# 3. Lire l’état et les blocs

Le namespace eth expose la vue consultable de la chaîne. eth_blockNumber donne le sommet connu, tandis que eth_getBlockByHash et eth_getBlockByNumber sélectionnent un bloc précis.

Un bloc associe un en-tête, des transactions et des informations de contexte. Les paramètres booléens déterminent notamment si les transactions sont renvoyées sous forme complète ou seulement comme identifiants.

Les méthodes eth_getBalance, eth_getCode, eth_getStorageAt et eth_getProof interrogent l’état d’un compte à un bloc donné. Le choix du bloc est important : une même adresse peut produire des résultats différents selon la hauteur consultée.

eth_call simule une exécution sans publier de transaction. eth_estimateGas fournit une estimation à partir d’un contexte, mais cette estimation dépend de l’état, du client et des règles de réseau.

Suite : [Transactions et transaction pool](04-transactions-txpool.md).
