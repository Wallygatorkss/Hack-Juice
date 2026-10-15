# Information Disclosure - 3 - Forgotten Sales Backup (fichier coupons via FTP)

## 1. Méthodologie (étapes)
1. Aller dans le dossier `ftp` ou autre répertoire public.
2. Identifier le fichier de backup/coupons (coupon_2013.md.bak).
3. Utiliser un encodage (ex : `%2500.md`) pour forcer lecture si l'extension est bloquée.
4. Extraire les coupons listés.

**Outils** : navigateur, Burp Suite, URL encoding.

## 2. Vulnérabilité
- **Nom** : Information Disclosure / misconfiguration FTP
- **Composants** : serveur FTP/HTTP, fichiers publics
- **Gravité** : moyenne

## 3. Risques
- Divulgation de coupons valides, pertes financières

## 4. Actions
- Restreindre accès dossier FTP, appliquer ACLs
- Stocker backups hors web public

## 5. Preuves
- Capture : ![Preuve : forgotten sales backup](./captures/preuve-ftp-signaturefile.png)