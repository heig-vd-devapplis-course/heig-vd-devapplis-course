---
marp: true
theme: custom-marp-theme
size: 16:9
paginate: true
author: L. Delafontaine, avec l'aide de GitHub Copilot
description:
  Identifier et structurer les pages d'une application PHP pour le cours
  DévAppliS à la HEIG-VD, Suisse
url: https://heig-vd-devapplis-course.github.io/heig-vd-devapplis-course/01-contenus-du-cours/04-identifier-et-structurer-les-pages-dune-application-php/presentation.html
header:
  "[**Identifier et structurer les pages d'une application
  PHP**][contenu-complet-sur-github]"
footer:
  "[**HEIG-VD**](https://heig-vd.ch) - [DévAppliS Course
  2025-2026](https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course)
  - [CC BY-SA 4.0][license]"
headingDivider: 6
math: mathjax
---

# Identifier et structurer les pages d'une application PHP

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

## État actuel de la maquette Figma

- La maquette Figma
  ([accessible ici](https://www.figma.com/make/Qmx2twEcduvA7RMt4LYosG/Destins-climatiques--Copy-?code-node-id=0-9&p=f&t=o6TagGM02iiodq4I-0&fullscreen=1))
  présente une application réactive : lorsque vous cliquez sur un élément,
  l'application s'adapte en conséquence (changement de section, couleurs, etc.).
- Ce comportement réactif peut être réalisé en utilisant JavaScript pour
  afficher ou masquer les différentes sections de l'application.
- Ce comportement n'est pas possible à réaliser uniquement avec PHP, car PHP est
  un langage qui génère du HTML statique.
- Cette introduction a pour but de pouvoir adapter la maquette Figma pour être
  en mesure de la réaliser avec PHP.

## Identifier les fonctionnalités actuelles

La maquette Figma présente plusieurs sections avec des fonctionnalités
distinctes :

1. Une page d'accueil décrivant le but de l'application.
2. Une section pour sélectionner un personnage.
3. Une section pour sélectionner un scénario climatique.
4. Un bouton pour démarrer le scénario sélectionné avec le personnage
   sélectionné.

Comment peut-on adapter ces aspects pour les utiliser avec PHP ?

## Solution 1 : une page PHP par aspect (1/3)

On peut structurer l'application en plusieurs pages PHP.

Chaque page peut être dédiée à une fonctionnalité spécifique :

- `index.php` : page d'accueil avec la description de l'application.
- `select_character.php` : page pour sélectionner un personnage.
- `select_scenario.php` : page pour sélectionner un scénario climatique.
- `view_scenario.php` : page pour démarrer le scénario sélectionné avec le
  personnage sélectionné.

## Solution 1 : une page PHP par aspect (2/3)

La page d'accueil (`index.php`) propose un bouton pour accéder à la page de
sélection du personnage (`select_character.php`).

La page `select_character.php` affiche les différents personnages disponibles,
qui sont des liens vers la page de sélection du scénario climatique, avec un
paramètre du personnage sélectionné (par exemple, via l'URL :
`select_scenario.php?character=1`).

La page `select_scenario.php` s'attend à trouver un paramètre du personnage
sélectionné dans l'URL pour afficher les scénarios climatiques disponibles pour
ce personnage.

## Solution 1 : une page PHP par aspect (3/3)

En utilisant le paramètre du personnage sélectionné dans l'URL, la page de
sélection du scénario climatique peut utiliser les informations de la base de
données pour adapter le contenu affiché.

La page de sélection du scénario climatique propose à son tour un bouton pour
démarrer le scénario sélectionné avec le personnage sélectionné, qui redirige
vers la page `view_scenario.php` en passant les paramètres du personnage et du
scénario sélectionnés (par exemple, via l'URL :
`view_scenario.php?character=1&scenario=2`).

## Solution 1 : une page PHP par aspect (4/4)

La page `view_scenario.php` s'attend à trouver les paramètres du personnage et
du scénario sélectionnés dans l'URL pour afficher le scénario sélectionné avec
le personnage sélectionné.

Chaque page peut ainsi utiliser les informations de la base de données pour
adapter le contenu affiché en fonction des paramètres reçus.

Le concept reste le même pour les autres aspects de l'application (par exemple,
naviguer entre les sections du scénario).

## Solution 2 : utiliser des formulaires (1/2)

La seconde solution pour adapter la maquette Figma pour être réalisable avec PHP
est d'utiliser des formulaires HTML.

Un formulaire permet de sélectionner les différentes options (personnage,
scénario climatique, etc.) et de soumettre ces informations à une page PHP pour
traitement.

La page reçoit du formulaire les informations sélectionnées et peut les utiliser
pour afficher le résultat correspondant.

## Solution 2 : utiliser des formulaires (2/2)

Cette solution permet de garder une seule page PHP pour l'ensemble de
l'application.

Elle nécessite néanmoins de gérer les différentes étapes de l'application à
travers les données reçues du formulaire.

Une fois le scénario affiché, il est possible de proposer un nouveau formulaire
pour naviguer entre les différentes sections du scénario ou utiliser la solution
précédente pour naviguer entre les différentes sections du scénario.

## Quelle solution choisir ?

Les deux solutions sont valides pour être réalisables avec PHP :

- La première solution est plus simple à mettre en place et à comprendre, mais
  elle peut entraîner une duplication de code et une navigation moins fluide
  pour l'utilisateur.trice.
- La seconde solution est plus complexe et demande plus de logique à mettre en
  place mais elle permet de garder une seule page PHP pour l'ensemble de
  l'application.

A vous de choisir la solution qui vous convient le mieux !

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
	https://github.com/heig-vd-devapplis-course/heig-vd-devapplis-course/blob/main/01-contenus-du-cours/04-identifier-et-structurer-les-pages-dune-application-php/README.md

<!-- Illustrations -->

[illustration-principale]:
	https://images.unsplash.com/photo-1669023414162-5bb06bbff0ec?fit=crop&h=720
