# Broken Authentication - 3 - Login Bender

## 1. Méthodologie (étapes)
1. Ouvrir la page de login.
2. Entrer `bender@juice-sh.op' --` dans le champ email.
3. Fournir n'importe quel mot de passe et soumettre.
4. Vérifier l'accès au compte Bender.

**Outils** : navigateur, Burp Suite.

## 2. Vulnérabilité
- **Nom** : SQL Injection (Authentication bypass)
- **Composants** : formulaire login, backend SQL non sécurisé
- **Gravité** : élevée

## 3. Risques
- Usurpation d'identité, actions illicites sous le compte.

## 4. Actions
- Requêtes préparées, validation d'entrée, log & monitoring.

## 5. Reproductibilité / Preuves
- **Payload testé** : `bender@juice-sh.op' --`