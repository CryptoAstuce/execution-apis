# 4. Transactions et transaction pool

Une transaction signée n’entre pas immédiatement dans un bloc. Le transaction pool la conserve en attente, vérifie sa forme et la rend disponible au producteur de bloc.

Les méthodes eth_sendRawTransaction et eth_sendTransaction correspondent à deux parcours différents : la première reçoit déjà une transaction signée ; la seconde suppose que le client possède le compte et peut signer.

Le namespace txpool permet d’observer la file d’attente. txpool_status résume les transactions prêtes et celles qui attendent encore, tandis que txpool_content expose leur organisation par adresse et nonce.

Le nonce impose un ordre par compte. Une transaction future peut donc rester bloquée derrière une transaction manquante. Les règles de remplacement et de prix sont propres à l’implémentation, même si les structures RPC sont communes.

Suite : [Engine API et passage de payloads](05-engine-api-payloads.md).
