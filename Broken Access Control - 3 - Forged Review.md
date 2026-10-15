# Broken Access Control - 3 - Forged Review

## 1. Méthodologie (étapes)
1. Intercepter la requête `PUT /rest/products/1/reviews`.
2. Modifier l'ID du produit et le corps JSON (`{"message":"...","author":"jim@juice-sh.op"}`).
3. Forward et vérifier que la review est acceptée et affichée.

**Outils** : Burp Suite (Interceptor / Repeater), éditeur JSON.

## 2. Vulnérabilité
- **Nom** : Broken Access Control / Improper Authorization
- **Composants** : API produit, validation d'auteur inexistante
- **Gravité** : moyenne

## 3. Risques
- Perte d'intégrité des avis, réputation manipulée

## 4. Actions
- Valider côté serveur que l'auteur correspond à l'utilisateur authentifié
- Authentifier et autoriser les requêtes CRUD

## 5. Preuves
- Capture requête/réponse : ![Preuve : forged review](./captures/preuve-forgedreview.png)
