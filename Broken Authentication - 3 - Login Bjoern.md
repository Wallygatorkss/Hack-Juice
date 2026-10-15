# Broken Authentication - 3 - Login Bjoern

## 1. Méthodologie (étapes)
1. Trouver l'email `bjoern@owasp.org`.
2. Analyser le code client (ex : `main.js`) et repérer la méthode de dérivation du mot de passe (ex : `btoa(n.email.split("").reverse().join(""))`).
3. Reproduire la transformation et soumettre le mot de passe calculé.
4. Vérifier la connexion et documenter la preuve.

**Outils** : DevTools, console JS, Burp Suite.

## 2. Vulnérabilité
- **Nom** : Stockage / dérivation du mot de passe côté client / sécurité par obscurité
- **Composants** : code JavaScript exposé, mécanisme d'authentification
- **Gravité** : élevée

## 3. Risques
- Compromission de comptes à cause d'une dérivation prévisible

## 4. Actions
- Ne jamais dériver/valider mot de passe côté client
- Utiliser hash salé côté serveur (bcrypt/argon2)

 