# OSINT / Information Disclosure - 3 - Bjoern's Favorite Pet

## 1. Méthodologie (étapes)
1. Aller sur la page d’administration pour récupérer l'email (ex : `bjoern@owasp.org`).
2. Rechercher en OSINT (conférences, posts, GitHub) le nom associé à ses publications/démonstrations.
3. Identifier les indices menant au nom du pet (ex: conférence, dépôt, tweet).

**Outils** : navigateur, moteur de recherche, GitHub.

## 2. Vulnérabilité
- **Nom** : Information Disclosure / OSINT facilitation
- **Composants** : pages publiques, admin panel exposant emails
- **Gravité** : faible à moyenne (contexte challenge)

## 3. Risques
- Reconnaissance facilitée pour attaques ciblées (spear phishing)

## 4. Actions
- Minimiser exposition d'emails et masquer données personnelles en admin.
- Restreindre accès et filtrer les informations publiées.