# Broken Authentication - 3 - Login Jim

## 1. Méthodologie (étapes)
1. Aller sur la page de login.
2. Injecter l'email `jim@juice-sh.op' --` (ou `jim@juice-sh.op'--`) dans le champ email.
3. Fournir n'importe quel mot de passe et soumettre ; la portion commentée (`--`) peut faire ignorer la vérification côté SQL si le backend concatène la requête.
4. Vérifier que la session est ouverte sous l'utilisateur Jim (profil, actions autorisées).

**Outils** : navigateur, DevTools, Burp Suite.

## 2. Vulnérabilité
- **Nom** : SQL Injection / Authentication Bypass
- **Composants** : écran d'authentification, requêtes SQL non paramétrées
- **Gravité** : élevée / critique

## 3. Risques
- Usurpation d'identité, accès aux données personnelles de Jim, actions malveillantes au nom de Jim.

## 4. Actions (remédiation)
- Paramétrer les requêtes SQL et échapper les entrées.
- Implémenter contrôles côté serveur (rate limiting, lockout après échecs).
- Journaliser et détecter patterns d'attaques.
