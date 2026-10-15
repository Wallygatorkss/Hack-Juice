# Broken Authentication - 3 - Reset Jim's Password

## 1. Méthodologie (étapes)
1. Récupérer l'email de Jim via admin ou DB.
2. Lancer le flux "mot de passe oublié" pour Jim.
3. Identifier la question de sécurité ou vecteur de réinitialisation.
4. Utiliser OSINT ou indices disponibles pour répondre et obtenir un token de réinitialisation.

**Outils** : navigateur, OSINT, Burp Suite.

## 2. Vulnérabilité
- **Nom** : Validation insuffisante des questions de sécurité / reset flow vulnérable
- **Composants** : endpoint "forgot password", stockage questions/réponses
- **Gravité** : élevée

## 3. Risques
- Prise de contrôle du compte Jim via réponse prévisible / exposée

## 4. Actions
- Ne pas utiliser questions basées sur info publique
- Mettre en place tokens à usage unique envoyés par mail et MFA
