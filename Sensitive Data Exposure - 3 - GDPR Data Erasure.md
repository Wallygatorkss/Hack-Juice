# Sensitive Data Exposure - 3 - GDPR Data Erasure (Accès DB)

## 1. Méthodologie (étapes)
1. Explorer la base de données via injection.
2. Identifier les colonnes contenant email / données personnelles.
3. Bypasser check mot de passe si nécessaire et lire les données d'utilisateur.

Outils : Burp Suite, requêtes manuelles (Union SELECT).

## 2. Vulnérabilité
- Nom : Fuite de données / mauvaise protection des données personnelles.
- Composants : base de données.
- Gravité : critique.

## 3. Risques
- Non conformité GDPR, amendes, atteinte réputationnelle, fuite d'identifiants.

## 4. Actions
- Chiffrer données sensibles, restreindre accès DB.
- Mettre en place des contrôles RBAC, audits réguliers.
- Supprimer / anonymiser données personnelles inutiles, implémenter politiques d'effacement.

