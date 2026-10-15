# Information Disclosure - 3 - Access Log

## 1. Méthodologie (étapes)
1. Aller sur la page Support.
2. Essayer d'accéder à `/logs` ou chemins similaires.
3. Vérifier si les logs sont accessibles sans authentification.

**Outils** : navigateur, Burp Suite.

## 2. Vulnérabilité
- **Nom** : Information Disclosure (logs exposés)
- **Composants** : endpoint `/logs`, répertoires non protégés
- **Gravité** : élevée

## 3. Risques
- Exposition d'adresses e-mail, tokens et secrets en clair

## 4. Actions
- Restreindre accès logs, masquer ou nettoyer données sensibles
- Mettre en place authentification/ACL

 