# Cross Site Scripting (XSS) - 3 - Product Tampering (description modifiée)

## 1. Méthodologie (étapes)
1. Identifier l'endpoint API produit.
2. Faire `PUT /rest/products/<id>` avec `Content-Type: application/json`.
3. Modifier `description` pour y inclure HTML/JS malveillant.
4. Vérifier le rendu côté UI.

**Outils** : Burp Suite, éditeur JSON.

## 2. Vulnérabilité
- **Nom** : Stored XSS / content injection
- **Composants** : API produit, rendu sans échappement
- **Gravité** : élevée

## 3. Risques
- Phishing interne, exécution JS, compromission d'utilisateurs

## 4. Actions
- Assainir HTML côté serveur, utiliser CSP, valider champs

## 5. Preuves
- Capture : ![Preuve : product tampering](./captures/preuve-tamporing.png)