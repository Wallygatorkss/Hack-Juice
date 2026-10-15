# Cryptography / Logic - 3 - Forged Coupon

## 1. Méthodologie (étapes)
1. Récupérer le fichier `coupon` ou la logique de génération depuis FTP ou code client.
2. Analyser le format/chiffrement des coupons.
3. Tenter de reproduire/générer un coupon valide (ex : format mois+année+valeur) ou trouver la clé HMAC si faible.
4. Tester le coupon généré dans l'application.

**Outils** : OSINT, scripts Python, outils de décodage.

## 2. Vulnérabilité
- **Nom** : Faible schéma de génération de coupon / chiffrement faible
- **Composants** : logique serveur-side des coupons
- **Gravité** : moyenne à élevée

## 3. Risques
- Fraude coupons, pertes financières

## 4. Actions
- Utiliser HMAC signé côté serveur, stocker validité côté serveur
- Ne pas implémenter logique prédictible côté client

 