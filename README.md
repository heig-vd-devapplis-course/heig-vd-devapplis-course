# HEIG-VD DévAppliS Course

[![Licence](https://img.shields.io/github/license/heig-vd-devapplis-course/heig-vd-devapplis-course)](./LICENSE.md)

Bienvenue sur le dépôt principal du cours _"Développer une application web
simple (DévAppliS)"_ enseigné à la
[Haute Ecole d'Ingénierie et de Gestion du Canton de Vaud (HEIG-VD)](https://heig-vd.ch),
Suisse !

## 🎯 Objectifs généraux

À l'issue de ce cours, les personnes devraient être capables de :

- Organiser son travail à l'aide d'un workflow de développement professionnel au
  sein d'une équipe.
- Modéliser et mettre en place une base de données à partir de données brutes.
- Traiter, nettoyer et importer des données dans une base de données à partir de
  données brutes.
- Réaliser les pages de visualisation des données à partir d'une maquette.
- Afficher les données issues d'une base de données dans des pages web.
- Déployer une application web simple sur un hébergement en ligne.

Grâce à ces compétences, les personnes qui étudient seront en mesure de
développer des applications web simples liées à une base de données en
respectant les bonnes pratiques de développement en équipe.

Un projet amené par un.e mandant.e externe permettra de mettre en pratique les
concepts acquis jusqu'ici dans le cursus dans un contexte réaliste.

## 📅 Programme

Les détails de chaque séance composant le cours sont disponibles ci-dessous.

|     Jour | Matin (8:30-12:00)                                                                                                                                                                | Après-midi (13:00-16:15)                                                                                                                                                                                                                                                                                                                      |
| -------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    Lundi | -                                                                                                                                                                                 | [Introduction et organisation du cours](./01-contenus-du-cours/01-introduction-et-organisation-du-cours/README.md) + [Workflow Git et GitHub](./01-contenus-du-cours/02-workflow-git-et-github/README.md) + Formation des groupes + Mise en place du projet sur Git/GitHub + Organisation/répartition du travail avec le workflow Git/GitHub. |
|    Mardi | Réalisation du modèle de la base de données à partir des données brutes.                                                                                                          | Création de la base de données.                                                                                                                                                                                                                                                                                                               |
| Mercredi | [Déployer une application PHP sur Infomaniak](./01-contenus-du-cours/03-deployer-une-application-php-sur-infomaniak/README.md) + Importation des données dans la base de données. | Identification des différentes pages à réaliser avec leur interaction et mise en page (HTML + CSS uniquement).                                                                                                                                                                                                                                |
|    Jeudi | Réalisation des pages avec interaction avec la base de données (HTML + CSS + PHP/PDO).                                                                                            | Réalisation des pages avec interaction avec la base de données (HTML + CSS + PHP/PDO).                                                                                                                                                                                                                                                        |
| Vendredi | Finalisation de l'application avec déploiement sur Infomaniak.                                                                                                                    | Rendu du travail à 15:00 + Discussions collectives sur l'expérience.                                                                                                                                                                                                                                                                          |

## 🏗️ Données à disposition

Les données suivantes sont à votre disposition pour réaliser le projet :

- Données brutes : <TODO>.
- Maquette Figma : <TODO>.

Vous devrez exploiter ces données pour réaliser le projet.

## 🫂 Organisation des groupes

- Par équipe de deux personnes.
- Les équipes sont libres. Les personnes inscrivent leur groupe dans un GitHub
  Classroom dédié : <TODO>.
- S'il y a un nombre impair de personnes, un seul groupe de trois personnes est
  autorisé. Si plusieurs personnes veulent former des groupes de trois, un seul
  groupe final sera tiré au sort et les personnes restantes devront former des
  groupes de deux.

## 📊 Grille d'évaluation

- 0 point – Les critères ne sont pas respectés : la production est absente, hors
  sujet ou témoigne d'une compréhension très limitée du sujet.
- 1 point – Les critères sont partiellement respectés : certains éléments
  essentiels sont manquants, imprécis ou incorrectement mis en œuvre.
- 2 points – Les critères sont pleinement respectés : l'ensemble des éléments
  attendus est présent, précis et démontre une compréhension claire et
  approfondie du sujet.

Note maximale : (nombre de points obtenus / nombre de points totaux) × 5 + 1.

## 📋 Critères d'évaluation

|   # | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Rendu(s) attendu(s)                                                                                |
| --: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------- |
|   1 | Le développement est clair, structuré et utilise un workflow professionnel pour organiser le travail tout au long du projet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Workflow Git/GitHub (issues/branches/PRs/fusion/gestion des conflits Git) et travail collaboratif. |
|   2 | Un README permet de comprendre le but du projet, sa structure et la documentation nécessaire pour reprendre le projet.<br><br>Ce README fait office de rapport final à l'aide d'un journal de travail et d'une conclusion finale<br><br>Chaque jour, une pull request (PR) indique ce qui a été fait durant la journée et ce qui est prévu de réaliser le lendemain. À faire de façon individuelle, une PR par membre du groupe en nous (Ludovic et Noemi) mettant en tant que reviewer avant fusion.<br><br>A la fin de la semaine (rendu selon le calendrier ci-dessus), une conclusion avec une rétrospective de l'expérience permet de comprendre comment l'expérience s'est déroulée pour vous (ce qu'il s'est bien passé, moins bien passé, ce qui serait fait différemment une prochaine fois et le travail d'équipe effectué). Cette conclusion doit comporter un aspect individuel et un aspect de groupe.<br><br>Le README se veut structuré et agréable à lire. | Fichier README.md.                                                                                 |
|   3 | Le modèle des données est cohérent avec les données brutes de l'application.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Diagramme du modèle de données (png, jpeg, svg, etc.).                                             |
|   4 | La base de données est correctement créée et respecte les contraintes du contexte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Script(s) SQL et PHP.                                                                              |
|   5 | Les données sont correctement traitées pour pouvoir les insérer ensuite dans la base de données.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Script(s) SQL et PHP.                                                                              |
|   6 | Les données traitées sont correctement importées dans la base de données.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Script(s) SQL et PHP.                                                                              |
|   7 | Les pages de l'application web sont réalisées en prenant en compte que l'application se veut attractive et agréable à utiliser. Les liens entre les pages/interactions sont cohérents.<br><br>Note : essayez de suivre au mieux l'esthétique du site de la maquette mais vous pouvez modifier si besoin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Pages PHP avec HTML et CSS associé.                                                                |
|   8 | Les pages de l'application web sont implémentées de telle manière à utiliser les informations issues de la base de données pour les afficher à l'utilisateur.trice final.e.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Pages PHP avec intéraction avec la base de données (PDO).                                          |
|   9 | L'application web est correctement déployée sur un hébergement en ligne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Lien vers l'application en ligne.                                                                  |
|  10 | L'application web est fonctionnelle et répond aux besoins du mandat.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Application web en ligne fonctionnelle.                                                            |

## 🚨 Contraintes

> [!CAUTION] Attention
>
> Le non-respect de ces contraintes peut engendrer l'échec du cours (les notes
> peuvent être différentes entre les membres de l'équipe si jugé nécessaire).

- Toutes les personnes de l'équipe contribuent de manière équitable.
- La documentation du projet/de l'application doit permettre à une personne
  externe à votre projet de comprendre et reprendre le travail effectué.
- Votre travail doit mentionner qu'il s'agit d'un projet réalisé dans le
  contexte de vos études à la [HEIG-VD](https://heig-vd.ch) en partenariat avec
  [WattEd](https://www.watted.ch/).
- Le travail est rendu dans les temps.
- L'utilisation de code généré par des outils d'intelligence artificielle ou
  copié depuis des sources externes est autorisé selon les règles suivantes :
  - Vous **devez indiquer quand, pourquoi et comment vous avez utilisé une aide
    externe** (la raison, outils, sources, etc.), **soit dans le code, soit dans
    un rapport annexe** (le README principal).
  - Vous **devez expliquer le fonctionnement du code que vous avez utilisé**,
    que ce soit du code généré par des outils d'intelligence artificielle ou du
    code copié depuis des sources externes, **et comment il s'intègre dans votre
    travail**.
  - En cas de doutes de notre part, vous pourriez être questionné.e.
  - **Si vos explications ne sont pas convaincantes, injustifiées dans le
    contexte ou si vous n'êtes pas transparent.e sur l'utilisation de ces
    outils**, nous considérons que vous n'avez pas acquis les compétences
    nécessaires du cours. **Vous serez alors pénalisé.e avec la note 1 pour le
    travail effectué**.
  - En cas de doutes, n'hésitez pas à nous contacter pour discuter de votre
    utilisation de ces outils.

## 📜 Licence

Ce travail est sous licence
[Creative Commons Attribution-ShareAlike 4.0 International](./LICENSE.md).
