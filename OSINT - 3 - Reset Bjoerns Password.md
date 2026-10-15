# OSINT / Broken Authentication - 3 - Reset Bjoern's Password

## 1. Méthodologie (étapes)
1. Rechercher OSINT pour trouver détails personnels utiles (ex : code postal, dates, références publiques).
2. Lancer le flow de reset et soumettre la valeur trouvée.
3. Vérifier la réinitialisation et l'accès.

**Outils** : OSINT, Burp Suite.

## 2. Vulnérabilité
- **Nom** : Reliance on OSINT data for security flows
- **Composants** : flow reset password
- **Gravité** : élevée

## 3. Risques
- Compromission de compte via données publiques

## 4. Actions
- Remplacer questions par token email sécurisé
- Implémenter MFA

 