# OSINT / Broken Authentication - 3 - Reset Bender's Password

## 1. Méthodologie (étapes)
1. Rechercher OSINT (ex : wiki, fan sites) pour trouver la réponse attendue.
2. Lancer le flow de reset pour Bender et fournir la réponse trouvée.
3. Vérifier que le mot de passe est réinitialisé.

**Outils** : moteurs de recherche, Burp Suite.

## 2. Vulnérabilité
- **Nom** : OSINT-exploitable security question
- **Composants** : flow reset password
- **Gravité** : élevée

## 3. Risques
- Prise de contrôle de compte via réponses accessibles publiquement

## 4. Actions
- Éviter questions basées sur culture/pop culture
- Implémenter MFA
