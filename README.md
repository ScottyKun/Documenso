# Documenso personnalisé – Signature électronique avec autorité de certification propre

Ce projet contient la base de déploiement d’une version personnalisée de Documenso pour la gestion de signatures électroniques, adaptée à un usage de départ avec une autorité de certification propre et un environnement maîtrisé.

L’objectif est de fournir une solution de travail initiale pour :

- signer des documents électroniquement ;
- centraliser les flux de signature ;
- intégrer une chaîne de confiance locale avec une autorité de certification propre ;
- permettre un déploiement simple via Docker Compose.

---

## 1. Présentation

Documenso est une plateforme de signature électronique open source. Cette version est adaptée à votre contexte pour servir de base à une implémentation plus avancée, avec un focus sur :

- une première mise en place opérationnelle ;
- une gouvernance de signature maîtrisée ;
- une intégration possible avec une infrastructure de certification nationale ou propre ;
- une préparation pour une évolution vers un environnement plus robuste.

---

## 2. Objectifs du projet

Ce dépôt a pour but de :

- déployer rapidement une instance de Documenso ;
- fournir un socle technique prêt à évoluer ;
- faciliter l’intégration d’un environnement de confiance pour les signatures ;
- offrir une base claire pour un premier lancement avec une autorité de certification propre.

---

## 3. Prérequis

Avant de commencer, assurez-vous d’avoir installé :

- Docker
- Docker Compose
- Un accès réseau suffisant pour télécharger les images nécessaires

---

## 4. Structure du projet

Le dépôt contient actuellement :

- compose.documenso.yaml : configuration Docker Compose du projet
- .env : variables d’environnement locales
- .env.example : modèle de variables d’environnement

---

## 5. Démarrage rapide

### Étape 1 : copier les variables d’environnement

```bash
cp .env.example .env
```

Puis renseignez les valeurs nécessaires dans le fichier .env.

### Étape 2 : démarrer les services

```bash
docker compose -f compose.documenso.yaml up -d
```

### Étape 3 : vérifier l’état des conteneurs

```bash
docker compose -f compose.documenso.yaml ps
```

### Étape 4 : accéder à l’application

Ouvrez l’URL fournie par votre configuration locale, selon la valeur définie dans votre environnement.

---

## 6. Configuration

Le fichier .env doit contenir les paramètres essentiels pour votre environnement, par exemple :

- informations de base de données ;
- secrets applicatifs ;
- identifiants d’accès ;
- paramètres liés à l’architecture de signature et à la certification.

> À adapter selon la configuration réelle de votre déploiement.

---

