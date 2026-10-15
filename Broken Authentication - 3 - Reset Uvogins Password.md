# Broken Authentication - 3 - Reset Uvogin's Password

## 1. Méthodologie (étapes)
1. Récupérer l'email de Uvogin via admin.
2. Lancer le flow "mot de passe oublié".
3. Rechercher OSINT pour trouver l'indice demandé.
4. Soumettre la réponse pour réinitialiser le mot de passe.

**Outils** : OSINT, Burp Suite.

## 2. Vulnérabilité
- **Nom** : Question de sécurité OSINT-vulnérable
- **Composants** : flow reset password
- **Gravité** : élevée

## 3. Risques
- Compromission de compte via infos publiques

## 4. Actions
- Retirer questions basées sur données publiques
- Mettre en place MFA et vérification par email/token
