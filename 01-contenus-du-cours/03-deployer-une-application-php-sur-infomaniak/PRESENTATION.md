---
marp: true
theme: custom-marp-theme
size: 16:9
paginate: true
author: L. Delafontaine, avec l'aide de GitHub Copilot
description:
  Déployer une application PHP sur Infomaniak pour le cours DévAppliS à la
  HEIG-VD, Suisse
url: https://heig-vd-devapplis-course.github.io/heig-vd-devapplis-course/01/contenus-du-cours/03-deployer-une-application-php-sur-infomaniak/presentation.html
header:
  "[**Déployer une application PHP sur Infomaniak**][contenu-complet-sur-github]"
footer:
  "[**HEIG-VD**](https://heig-vd.ch) - [DévAppliS Course
  2025-2026](https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course)
  - [CC BY-SA 4.0][license]"
headingDivider: 6
math: mathjax
---

# Déployer une application PHP sur Infomaniak

<!--
_class: lead
_paginate: false
-->

<https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course>

Visualiser le contenu complet sur GitHub [à cette
adresse][contenu-complet-sur-github].

<small>L. Delafontaine, avec l'aide de
[GitHub Copilot](https://github.com/features/copilot).</small>

<small>Ce travail est sous licence [CC BY-SA 4.0][license].</small>

![bg opacity:0.05][illustration-principale]

## Environnements locaux et productions

- Votre environnement de développement local met à disposition tous les outils
  nécessaires pour développer votre application web.
- Cet environnement vous permet de développer, tester et déboguer votre
  application.
- Un environnement de production est un environnement où votre application est
  déployée et accessible aux utilisateur.trices..
- Dans ce cours, nous allons apprendre à déployer une application PHP sur
  Infomaniak, un hébergeur web suisse.

## Déployer une application PHP sur Infomaniak

Un guide complet est disponible à l'adresse suivante :
[Déployer un site ou une application web sur Internet](https://github.com/heig-vd-progserv-course/heig-vd-progserv1-course/blob/main/01-contenus-du-cours/06.02-deployer-un-site-ou-une-application-web-sur-internet/README.md).

Il est recommandé de suivre ce guide pas à pas pour déployer votre application
PHP sur Infomaniak. Un déploiement par groupe est suffisant.

Nous nous attendons à ce que vous ayez une application web PHP fonctionnelle et
accessible en ligne à la fin de ce processus.

## Infomaniak

- Infomaniak est un hébergeur web suisse qui propose des services d'hébergement
  de sites web.
- Infomaniak propose une offre étudiante qui permet de déployer des applications
  web PHP facilement et gratuitement.
- Nous allons utiliser cette offre pour déployer notre application web.

![bg right:40%][illustration-principale]

## Transfert via FTP/SFTP

- Le transfert de fichiers vers Infomaniak se fait généralement via FTP ou SFTP.
- Vous pouvez utiliser des clients FTP comme FileZilla, WinSCP ou Cyberduck pour
  transférer vos fichiers.
- Assurez-vous de configurer correctement les paramètres de connexion FTP/SFTP
  fournis par Infomaniak.
- Transférez les fichiers de votre application web vers le répertoire racine de
  votre hébergement.
- Le document mentionné fournit toutes les instructions.

## Résumé

- Infomaniak offre une solution d'hébergement web qui permet de déployer des
  sites et des applications web sur Internet.
- Les étapes pour déployer une application web incluent :
  1. Avoir un hébergement web sur Infomaniak (offre étudiante disponible)
     configurer pour héberger une application PHP.
  2. Transférer les fichiers de l'application sur le serveur.
  3. Votre application est maintenant déployée et accessible !

Le
[document associé](https://github.com/heig-vd-progserv-course/heig-vd-progserv1-course/blob/main/01-contenus-du-cours/06.02-deployer-un-site-ou-une-application-web-sur-internet/README.md)
décrit toute la marche à suivre pour déployer votre application et la rendre
accessible au reste du monde !

## Questions

<!-- _class: lead -->

Est-ce que vous avez des questions ?

## Sources

- [Illustration principale][illustration-principale] par
  [Growtika](https://unsplash.com/@growtika) sur
  [Unsplash](https://unsplash.com/photos/a-computer-with-a-keyboard-and-mouse-yGQmjh2uOTg)

<!-- URLs -->

[license]:
	https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course/blob/main/LICENSE.md
[contenu-complet-sur-github]:
	https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course/blob/main/03-deployer-une-application-php-sur-infomaniak/README.md

<!-- Illustrations -->

[illustration-principale]:
	https://images.unsplash.com/photo-1669023414162-5bb06bbff0ec?fit=crop&h=720
