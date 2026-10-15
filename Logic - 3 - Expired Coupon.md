# Logic - 3 - Expired Coupon (modification date local)

## 1. Méthodologie (étapes)
1. Rechercher la logique client (`main.js`) qui contient dates des campagnes/coupons.
2. Modifier la date système locale du navigateur/OS ou intercepter la vérification pour la contourner.
3. Appliquer le coupon expiré et vérifier s'il est accepté.

**Outils** : DevTools, Burp Suite.

## 2. Vulnérabilité
- **Nom** : Client-side trust / incorrect server-side validation of coupon validity
- **Composants** : code client, logique de validation
- **Gravité** : moyenne à élevée

## 3. Risques
- Usage de coupons expirés, perte de revenus

## 4. Actions
- Vérifier validité côté serveur en se basant sur l'horodatage serveur
- Ne pas dépendre de l'heure client

 