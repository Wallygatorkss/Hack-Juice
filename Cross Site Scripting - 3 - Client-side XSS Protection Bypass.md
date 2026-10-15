# Cross Site Scripting (XSS) - 3 - Client-side XSS Protection Bypass

## 1. Méthodologie (étapes)
1. Créer un compte normal.
2. Intercepter la requête de création et injecter payloads XSS dans `email` ou autres inputs.
3. Forward et vérifier si l'application persiste et exécute le payload.
4. Observer si la sanitation côté client est contournée.

**Outils** : Burp Suite, DevTools.

## 2. Vulnérabilité
- **Nom** : Weak client-side filtering / reliance on client-side protections
- **Composants** : formulaires, validation côté client
- **Gravité** : élevée

## 3. Risques
- Stored XSS, compromission d'utilisateurs

## 4. Actions
- Valider et assainir côté serveur
- Ne pas se fier aux protections côté client

 