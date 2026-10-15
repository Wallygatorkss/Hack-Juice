# Business Logic - 3 - Manipulate Basket

## 1. Méthodologie (étapes)
1. Ajouter un article au panier.
2. Intercepter la requête (ex : `PUT /api/basket/...`).
3. Modifier `basketId` ou `id` pour manipuler le panier d'un autre utilisateur.
4. Vérifier que l'article apparaît dans le panier ciblé.

**Outils** : Burp Suite, DevTools.

## 2. Vulnérabilité
- **Nom** : IDOR / Insecure Direct Object Reference / Broken Access Control
- **Composants** : endpoint panier, vérification propriétaire manquante
- **Gravité** : élevée

## 3. Risques
- Vol / modification d'achats, fraude

## 4. Actions
- Lier panier à session utilisateur côté serveur
- Vérifier propriétaire et utiliser tokens non prévisibles
