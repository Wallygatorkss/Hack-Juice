# Information Disclosure - 3 - Forgotten Developer Backup

## 1. Méthodologie (étapes)
1. Parcourir répertoires publics `/ftp`.
2. Lister fichiers et repérer backups developers (ex : `package-json.bak`).
3. Utiliser un encodage (ex : `%2500.md`) pour forcer lecture si l'extension est bloquée.

**Outils** :Burp Suite, outils d'archivage.

## 2. Vulnérabilité
- **Nom** : Exposition de sauvegarde oubliée
- **Composants** : fichiers backup exposés publiquement
- **Gravité** : critique

## 3. Risques
- Accès à clés privées, variables d'environnement, dumps → compromission infra

## 4. Actions
- Retirer backups du web public
- Stocker chiffré et restreint, rotation des clés si exposées

## 5. Preuves
- Liste des fichiers extraits: ![Preuve : forgotten dev backup](./captures/preuve-ftp-signaturefile.png)