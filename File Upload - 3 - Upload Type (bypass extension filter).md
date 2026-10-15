# File Upload - 3 - Upload Type (bypass extension filter)

## 1. Méthodologie (étapes)
1. Préparer un fichier ZIP contenant un fichier texte (ex : `test.txt.zip`).
2. Upload via l'UI.
3. Intercepter la requête et modifier le nom du fichier dans la requête en `test.txt` avant d'envoyer.
4. Vérifier si le serveur accepte le fichier et le stocke avec l'extension modifiée.

**Outils** : Burp Suite, éditeur hex, curl.

## 2. Vulnérabilité
- **Nom** : Insecure file upload / insufficient server-side validation
- **Composants** : endpoint d'upload, vérification type/extension mal implémentée
- **Gravité** : élevée

## 3. Risques
- Upload de webshells, exécution de code arbitraire

## 4. Actions
- Valider type MIME et vérifier magic bytes côté serveur
- Stocker hors racine web, renommer fichiers uploadés
- Scanner contenu (antivirus)

## 5. Preuves
- Capture : ![Preuve : upload size](./captures/preuve-uploadtype.png)

- Capture : ![Preuve : upload size](./captures/preuve-uploadsize.png)