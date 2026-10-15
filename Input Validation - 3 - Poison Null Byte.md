# Input Validation - 3 - Poison Null Byte

## 1. Méthodologie (étapes)
1. Identifier un endpoint qui refuse un caractère null littéral (`%00`) dans le nom de fichier ou paramètre.
2. Encoder le signe `%` en `%25` puis ajouter `00` → `...%2500...`. Après un double décodage côté serveur cela peut produire un `\x00` effectif.
3. Tester si le serveur traite différemment la ressource (ex. suppression/ignorance d'extension ou lecture non intentionnelle).

**Outils** : navigateur, Burp Suite (Repeater), utilitaire d'URL-encoding.

## 2. Vulnérabilité
- **Nom** : Null byte poisoning / improper input decoding
- **Composants** : routines de décodage d'URL côté serveur, gestion des chemins de fichiers
- **Gravité** : moyenne à élevée (selon la logique de traitement des chemins)

## 3. Risques
- Accès à des fichiers non destinés (backups, scripts), contournement de contrôle d'extension

## 4. Actions (remédiation)
- Normaliser et valider les entrées après décodage complet (ne pas appliquer de décisions basées sur des versions partiellement décodées)
- Refuser les caractères non imprimables / null bytes dans les noms de fichiers et paramètres
- Vérifier les extensions et types MIME après décodage
- Journaliser et alerter sur accès inhabituels aux endpoints de fichiers
