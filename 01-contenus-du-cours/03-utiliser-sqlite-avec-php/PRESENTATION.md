---
marp: true
theme: custom-marp-theme
size: 16:9
paginate: true
author: L. Delafontaine, N. Romano avec l'aide de GitHub Copilot
description:
  Utiliser SQLite avec PHP pour le cours DévAppliS à la HEIG-VD, Suisse
url: https://heig-vd-devapplis-course.github.io/heig-vd-devapplis-course/01-contenus-du-cours/03-utiliser-sqlite-avec-php/presentation.html
header: "[**Utiliser SQLite avec PHP**][contenu-complet-sur-github]"
footer:
  "[**HEIG-VD**](https://heig-vd.ch) - [DévAppliS Course
  2025-2026](https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course)
  - [CC BY-SA 4.0][license]"
headingDivider: 6
math: mathjax
---

# Utiliser SQLite avec PHP

<!--
_class: lead
_paginate: false
-->

<https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course>

Visualiser le contenu complet sur GitHub [à cette
adresse][contenu-complet-sur-github].

<small>L. Delafontaine, N. Romano avec l'aide de
[GitHub Copilot](https://github.com/features/copilot).</small>

<small>Ce travail est sous licence [CC BY-SA 4.0][license].</small>

## Vous connaissez déjà PostgreSQL

- Dans les cours _Modélisation de données_ et _Infrastructure de données_, vous
  avez travaillé avec **PostgreSQL** : un système de gestion de base de données
  (SGBD) complet
- PostgreSQL est un serveur : il tourne en arrière-plan, écoute sur un port
  réseau, et gère les connexions de plusieurs clients simultanément
- Dans ce cours, nous allons utiliser une base de données différente :
  **SQLite**

## PostgreSQL vs SQLite - Architecture (1/2)

PostgreSQL fonctionne en mode **client-serveur** :

- Un processus serveur (`postgres`) tourne en permanence sur une machine
- Les clients (PHP, psql, pgAdmin etc.) se connectent via TCP/IP avec un nom
  d'utilisateur et un mot de passe
- Les données sont stockées dans un répertoire géré par le serveur

## PostgreSQL vs SQLite - Architecture (2/2)

SQLite fonctionne de façon **embarquée** :

- Il n'y a **aucun serveur** à démarrer ou à configurer
- La base de données entière est un **fichier unique** (ex. `database.sqlite`)
- PHP lit et écrit directement dans ce fichier via une bibliothèque intégrée

## Comparaison des deux approches

|                        | PostgreSQL          | SQLite              |
| ---------------------- | ------------------- | ------------------- |
| Architecture           | Client-serveur      | Embarqué (fichier)  |
| Installation           | Serveur requis      | Aucune              |
| Connexion              | TCP/IP, auth réseau | Chemin vers fichier |
| Utilisateurs multiples | Oui (concurrent)    | Limité              |
| Taille des données     | Très grande échelle | Petite/moyenne      |
| Cas d'usage typique    | Production, API     | Prototypage, mobile |

## Pourquoi SQLite dans ce cours ? (1/2)

- SQLite est **intégré nativement à PHP** : aucune installation supplémentaire
  n'est nécessaire, il est disponible directement via la classe `PDO`
- Il est **idéal pour apprendre** : on se concentre sur la logique PHP et SQL,
  pas sur la configuration d'un serveur
- Le déploiement est **très simple** : copier le fichier de base de données
  suffit, pas besoin de migrer un serveur

## Pourquoi SQLite dans ce cours ? (2/2)

- Les applications que vous allez développer sont de **petite taille** : peu
  d'utilisateurs simultanés, pas de besoins de haute disponibilité
- SQLite est utilisé en production dans des millions d'applications (apps
  mobiles, appareils embarqués, petits sites web)
- Ce que vous apprenez avec SQLite est **directement transférable** à PostgreSQL
  : la syntaxe SQL est quasi identique

## Ce que PostgreSQL apporte en plus

En situation de production réelle ou avec de nombreux utilisateurs, PostgreSQL
offre des fonctionnalités que SQLite ne propose pas :

- **Accès concurrent** : plusieurs utilisateurs en écriture simultanément
- **Rôles et permissions** : gestion fine des droits d'accès par utilisateur
- **Réplication et sauvegarde** : haute disponibilité et tolérance aux pannes
- **Types avancés** : JSON natif, tableaux, géométrie, etc

Vous avez étudié ces aspects dans le cours _Infrastructure de données_.

## Comparaison de syntaxe SQL - Types (1/3)

PostgreSQL impose des types **stricts** avec une sémantique précise :

```sql
CREATE TABLE utilisateurs (
  id        SERIAL PRIMARY KEY,
  nom       VARCHAR(100) NOT NULL,
  actif     BOOLEAN DEFAULT TRUE,
  solde     NUMERIC(10, 2),
  cree_le   TIMESTAMP DEFAULT NOW()
);
```

Le serveur **refuse** toute valeur qui ne correspond pas au type déclaré.

## Comparaison de syntaxe SQL - Types (2/3)

SQLite utilise un système d'**affinité de types** : il ne stocke que 5 classes
internes (`NULL`, `INTEGER`, `REAL`, `TEXT`, `BLOB`).

```sql
CREATE TABLE utilisateurs (
  id        INTEGER PRIMARY KEY AUTOINCREMENT,
  nom       TEXT NOT NULL,
  actif     INTEGER DEFAULT 1,   -- 0 = false, 1 = true
  solde     REAL,
  cree_le   TEXT DEFAULT (datetime('now'))
);
```

SQLite **accepte** n'importe quel nom de type — `VARCHAR(100)` est stocké comme
`TEXT`.

## Comparaison de syntaxe SQL - Types (3/3)

| Besoin        | PostgreSQL             | SQLite                     |
| ------------- | ---------------------- | -------------------------- |
| Entier auto   | `SERIAL` / `BIGSERIAL` | `INTEGER PK AUTOINCREMENT` |
| Texte         | `VARCHAR(n)` / `TEXT`  | `TEXT`                     |
| Booléen       | `BOOLEAN`              | `INTEGER` (0 / 1)          |
| Décimal       | `NUMERIC(p, s)`        | `REAL`                     |
| Date et heure | `DATE` / `TIMESTAMP`   | `TEXT` (ISO 8601)          |
| JSON          | `JSON` / `JSONB`       | `TEXT`                     |

> SQLite est **permissif** : écrire `VARCHAR(100)` fonctionne, mais c'est du
> `TEXT` sous le capot.

## Comparaison de syntaxe SQL - Requêtes

Les requêtes `SELECT`, `INSERT`, `UPDATE`, `DELETE` et les jointures sont
**identiques** dans les deux systèmes :

```sql
-- Fonctionne aussi bien avec PostgreSQL qu'avec SQLite
SELECT u.nom, COUNT(c.id) AS nb_commandes
FROM utilisateurs u
LEFT JOIN commandes c ON c.utilisateur_id = u.id
WHERE u.actif = 1
GROUP BY u.nom
ORDER BY nb_commandes DESC;
```

Les différences se limitent aux **types**, à quelques **fonctions** (`NOW()` →
`datetime('now')`) et aux **séquences automatiques**.

## Questions ?

<!-- _class: lead -->

## Sources

- [SQLite Documentation](https://sqlite.org/docs.html) : documentation
  officielle de SQLite
- [SQLite vs PostgreSQL - Detailed Comparison](https://www.datacamp.com/blog/sqlite-vs-postgresql-detailed-comparison)
  par DataCamp

<!-- URLs -->

[license]:
	https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course/blob/main/LICENSE.md
[contenu-complet-sur-github]:
	https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course/blob/main/01-contenus-du-cours/03-utiliser-sqlite-avec-php/README.md
