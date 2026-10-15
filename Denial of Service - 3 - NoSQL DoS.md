# Denial of Service - 3 - NoSQL DoS

## Statut : notes incomplètes / détails manquants

Tu as indiqué que ce point était incomplet. Pour rédiger un rapport complet j'ai besoin :
- du vecteur exact utilisé (endpoint, payload, type de requête)
- des observations (CPU/mémoire, timeouts)
- preuves (logs, captures Burp)

Si tu veux, je peux rédiger un rapport générique couvrant : vecteurs typiques (ex : `$where` avec `sleep` en MongoDB), exemples de payloads, et mitigations (validation, rate-limiting, limitation complexité requêtes).

## Exemple général
- **Vulnérabilité** : Requête NoSQL mal formée provoquant exécution coûteuse côté DB (ex : `$where` avec fonction lourde)
- **Mitigations** : validation schéma, rate-limiting, monitoring, limiter usage d'opérateurs exécutables
