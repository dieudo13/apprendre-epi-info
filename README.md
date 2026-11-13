# Apprendre Epi Info 7

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24182020.svg)](https://doi.org/10.5281/zenodo.24182020)
[![Licence : CC BY-NC-SA 4.0](https://img.shields.io/badge/Licence-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr)

Guide pratique en français pour apprendre à concevoir un questionnaire, saisir des données et les analyser avec **Epi Info 7**, le logiciel gratuit des Centers for Disease Control and Prevention (CDC).

**Auteur :** OUEDRAOGO Ahmed Dieudonné (2026)

## Contenu du livre

| Chapitre | Fichier | Sujet |
|---|---|---|
| — | `00auteur.tex` | À propos de l'auteur |
| — | `01preambule.tex` | Préambule et organisation du livre |
| 1 | `02installationEpi.tex` | Installation et passage d'Epi Info 7 en français |
| 2 | `03creerQuestionnaire.tex` | Créer les champs d'un questionnaire (inclut `remarque.tex` : modèles de projet) |
| 3 | `04codeValidation.tex` | Le code de contrôle (Assign, If, Dialog, Enable, Disable…) |
| 4 | `05saisirDonnees.tex` | Saisir des données et tester le questionnaire |
| 5 | `06statTableauBord.tex` | Module Tableau de bord visuel : statistiques descriptives, tableau 2x2, filtres, graphiques |
| 6 | `07statClassic.tex` | Module Classique : commandes, recodage, tableaux stratifiés, régression logistique |
| 7 | `08statCalc.tex` | Module StatCalc : taille d'échantillon et calculatrices |
| — | `09conclusion.tex` | Conclusion |

Le fichier principal est `00bookEpiinfo.tex`. Les captures d'écran sont dans le dossier `img/`.

## Télécharger le PDF

Le PDF est archivé sur Zenodo : https://doi.org/10.5281/zenodo.24182020

Il est aussi disponible dans la section **Releases** de ce dépôt.

## Citer ce guide

OUEDRAOGO AD. Apprendre Epi Info 7 : guide pratique d'analyse épidémiologique et statistique. Zenodo; 2026. doi:10.5281/zenodo.24182020

## Licence

© 2026 OUEDRAOGO Ahmed Dieudonné. Ce guide est diffusé sous licence [Creative Commons Attribution – Pas d'utilisation commerciale – Partage dans les mêmes conditions 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr) : vous pouvez le partager et l'adapter en citant l'auteur, sans usage commercial, et en diffusant vos adaptations sous la même licence. Voir le fichier `LICENSE`.

## Compiler le livre

Le document doit être compilé avec **LuaLaTeX** (le paquet `emoji` l'exige), deux à trois fois pour mettre à jour la table des matières et les renvois :

```bash
lualatex 00bookEpiinfo.tex
lualatex 00bookEpiinfo.tex
lualatex 00bookEpiinfo.tex
```

Compilation testée avec TeX Live sous Linux. Avec MiKTeX (Windows), les paquets manquants s'installent automatiquement à la première compilation.

Polices utilisées (incluses dans TeX Live et MiKTeX) :

- TeX Gyre Pagella (texte) et TeX Gyre Pagella Math (formules) ;
- TeX Gyre Adventor (titres sans empattement) ;
- Inconsolata (codes).

## Conventions typographiques

Le fichier principal définit des macros pour garder une mise en forme homogène :

| Macro | Usage | Rendu |
|---|---|---|
| `\module{...}` | nom d'un module d'Epi Info | gras, petites capitales |
| `\kw{...}` | menus, boutons, fenêtres, valeurs | gras |
| `\var{...}` | variables, fichiers, chemins | machine à écrire |
| `\commande{...}` | commandes et code Epi Info | machine à écrire gras |
| `\question{...}` | libellé d'une question, message | « ... » |
| `\terme{...}` | notion définie dans le texte | italique |

## Avertissement

Ce guide est un travail indépendant. Il n'est ni publié ni approuvé par les CDC. Epi Info est une marque des CDC.
