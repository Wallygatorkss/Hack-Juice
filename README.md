# Hack-Juice

> Collection de write-ups de sécurité réalisés sur [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/), un laboratoire volontairement vulnérable dédié à l'apprentissage de la cybersécurité applicative.

[![OWASP Juice Shop](https://img.shields.io/badge/OWASP-Juice%20Shop-orange?logo=owasp)](https://owasp.org/www-project-juice-shop/)
[![Burp Suite](https://img.shields.io/badge/Outil-Burp%20Suite-red)](https://portswigger.net/burp)
[![Markdown](https://img.shields.io/badge/Documentation-Markdown-000000?logo=markdown)](https://www.markdownguide.org/)
[![Statut](https://img.shields.io/badge/Statut-p%C3%A9dagogique-blue)](#avertissement)

## Aperçu du projet

**Hack-Juice** regroupe 37 write-ups documentant l'identification, l'exploitation contrôlée et la remédiation de vulnérabilités présentes dans OWASP Juice Shop.

Chaque fiche présente une méthodologie reproductible, la vulnérabilité concernée, ses risques, des recommandations de correction et, lorsque c'est pertinent, une capture de preuve. L'objectif est de transformer chaque challenge en une trace technique claire, exploitable dans un contexte d'apprentissage ou de portfolio.

## Fonctionnalités clés

- **37 write-ups structurés** couvrant notamment les contrôles d'accès, l'authentification, les injections, les XSS, l'OSINT et les erreurs de configuration.
- **Méthodologies reproductibles** avec étapes, endpoints et exemples de payloads lorsque cela est nécessaire.
- **Preuves visuelles** regroupées dans le dossier [`captures/`](./captures/).
- **Recommandations de remédiation** associées à chaque vulnérabilité pour relier exploitation et sécurisation.
- **Outils de test variés** : Burp Suite, navigateur, DevTools et requêtes HTTP manuelles.

## Périmètre couvert

| Catégorie | Nombre de write-ups |
| --- | ---: |
| Broken Authentication | 7 |
| Broken Access Control | 4 |
| Business Logic | 4 |
| Information Disclosure | 4 |
| Cross-Site Scripting | 3 |
| OSINT | 3 |
| File Upload | 2 |
| Injection | 2 |
| Security Misconfiguration | 2 |
| Cryptography, DoS, Input Validation, Logic, Security through Obscurity, Sensitive Data Exposure | 6 |

## Prérequis

- [Docker](https://docs.docker.com/get-docker/) et Docker Compose, ou une installation locale d'OWASP Juice Shop.
- Un navigateur web récent.
- [Burp Suite](https://portswigger.net/burp) Community ou Professional pour intercepter et modifier les requêtes.
- Des notions de base en HTTP, JSON et sécurité web.

## Installation et utilisation

### 1. Récupérer le projet

```bash
git clone git@github.com:Wallygatorkss/Hack-Juice.git
cd Hack-Juice
```

### 2. Démarrer OWASP Juice Shop

Le dépôt contient les write-ups et leurs preuves ; l'application vulnérable se lance séparément dans un environnement local :

```bash
docker pull bkimminich/juice-shop
docker run -d --name juice-shop -p 3000:3000 bkimminich/juice-shop
```

Ouvrir ensuite [http://localhost:3000](http://localhost:3000).

Pour arrêter puis supprimer le conteneur :

```bash
docker stop juice-shop
docker rm juice-shop
```

### 3. Préparer Burp Suite

1. Lancer Burp Suite et son navigateur intégré, ou configurer le proxy du navigateur sur `127.0.0.1:8080`.
2. Ouvrir Juice Shop sur `http://localhost:3000`.
3. Choisir un write-up dans la liste des fichiers Markdown.
4. Reproduire les étapes uniquement sur l'instance locale.
5. Vérifier le résultat et consulter la capture associée dans [`captures/`](./captures/).

> Les payloads présents dans les write-ups sont destinés à un laboratoire local et autorisé. Ne pas les utiliser contre un service tiers sans autorisation explicite.

## Organisation du projet

```text
Hack-Juice/
├── README.md
├── Broken Access Control - 3 - *.md
├── Broken Authentication - 3 - *.md
├── Business Logic - 3 - *.md
├── Cross Site Scripting - 3 - *.md
├── Cryptography - 3 - *.md
├── Denial of Service - 3 - *.md
├── File Upload - 3 - *.md
├── Information Disclosure - 3 - *.md
├── Injection - 3 - *.md
├── Input Validation - 3 - *.md
├── Logic - 3 - *.md
├── OSINT - 3 - *.md
├── Security Misconfiguration - 3 - *.md
├── Security through Obscurity - 3 - *.md
├── Sensitive Data Exposure - 3 - *.md
└── captures/
    └── preuve-*.png
```

Chaque write-up suit une structure commune :

1. Méthodologie et étapes de reproduction.
2. Nom et composant vulnérable.
3. Risques associés.
4. Actions de correction recommandées.
5. Preuve ou annexe.

## Ce que j'ai appris / Défis techniques

- **Analyser une application web de bout en bout** : relier l'interface, les endpoints REST, les paramètres HTTP et les réponses du serveur.
- **Intercepter et modifier des requêtes** avec Burp Suite pour comprendre les contrôles d'accès, l'authentification et la validation des entrées.
- **Raisonner comme un attaquant puis comme un défenseur** : identifier l'impact d'une faille et proposer une correction côté serveur.
- **Différencier les familles de vulnérabilités** : séparer une faille de logique métier d'une injection, d'un défaut d'authentification ou d'une fuite d'information.
- **Documenter une preuve technique** : produire des étapes reproductibles et des captures lisibles plutôt qu'une simple description théorique.
- **Travailler dans un cadre contrôlé** : utiliser une application volontairement vulnérable en local afin de pratiquer sans exposer de système tiers.

## Avertissement

Ce projet est exclusivement pédagogique. OWASP Juice Shop est volontairement vulnérable : il ne doit pas être exposé sur Internet ni utilisé pour tester une application sans autorisation explicite.