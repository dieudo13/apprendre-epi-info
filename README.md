# Apprendre Epi Info 7

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24182020.svg)](https://doi.org/10.5281/zenodo.24182020)
[![Licence : CC BY-NC-SA 4.0](https://img.shields.io/badge/Licence-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr)

Guide pratique en français pour apprendre à concevoir un questionnaire, saisir des données et les analyser avec **Epi Info 7**, le logiciel gratuit des Centers for Disease Control and Prevention (CDC).

**Lire le livre en ligne : <https://dieudo13.github.io/apprendre-epi-info/>**

Ce dépôt contient les sources du livre au format [Quarto](https://quarto.org). Elles produisent un site web publié sur GitHub Pages. La version PDF n'est pas générée ici : elle est archivée sur Zenodo (https://doi.org/10.5281/zenodo.24182020), et le site y renvoie par un lien dans la barre latérale et en pied de page.

**Auteur :** OUEDRAOGO Ahmed Dieudonné (2026)

## Contenu du livre

| Chapitre | Fichier | Sujet |
|---|---|---|
| — | `index.qmd` | Accueil, citation, conventions typographiques, licence |
| — | `auteur.qmd` | À propos de l'auteur |
| — | `preambule.qmd` | Préambule et organisation du livre |
| 1 | `01-installation.qmd` | Installation et passage d'Epi Info 7 en français |
| 2 | `02-creer-questionnaire.qmd` | Créer les champs d'un questionnaire, pages, ordre de tabulation, modèles |
| 3 | `03-code-controle.qmd` | Le code de contrôle (Assign, If, Dialog, Enable, Disable…) |
| 4 | `04-saisir-donnees.qmd` | Saisir des données et tester le questionnaire |
| 5 | `05-tableau-de-bord.qmd` | Module Tableau de bord visuel : statistiques descriptives, tableau 2x2, filtres, graphiques |
| 6 | `06-module-classique.qmd` | Module Classique : commandes, recodage, tableaux stratifiés, régression logistique |
| 7 | `07-statcalc.qmd` | Module StatCalc : taille d'échantillon et calculatrices |
| — | `conclusion.qmd` | Conclusion |

Autres fichiers :

- `_quarto.yml` : configuration du livre (chapitres, format HTML, lien vers le PDF Zenodo, renvois croisés en français) ;
- `styles/custom.scss` : couleurs et mise en forme du site ;
- `styles/epiinfo.xml` : coloration syntaxique du code de contrôle et des programmes Epi Info ;
- `img/` : couverture et captures d'écran ;
- `.github/workflows/publish.yml` : construction et publication automatiques sur GitHub Pages.

## Construire le livre sur son ordinateur

1. Installer [Quarto](https://quarto.org/docs/get-started/) (version 1.4 ou plus récente).
2. Dans le dossier du dépôt :

```bash
quarto preview          # aperçu du site, mis à jour à chaque enregistrement
quarto render           # site web dans le dossier _book/
```

## Publier sur GitHub Pages

1. Dans le dépôt : **Settings > Pages > Build and deployment > Source**, choisir **GitHub Actions**.
2. Chaque envoi sur `main` lance le workflow `Publier le livre`, qui construit le site puis le met en ligne à l'adresse <https://dieudo13.github.io/apprendre-epi-info/>.

## Conventions d'écriture

| Élément | Écriture Markdown | Rendu |
|---|---|---|
| Module d'Epi Info | `**[classique]{.smallcaps}**` | gras, petites capitales |
| Menu, bouton, fenêtre, valeur | `**Nouveau projet**` | gras |
| Variable, fichier, chemin | `` `date_naissance` `` | machine à écrire |
| Commande ou code Epi Info | ``**`ASSIGN`**`` | machine à écrire gras |
| Libellé d'une question | `« Êtes-vous vacciné(e) ? »` | guillemets français |
| Notion définie dans le texte | `*odds ratio*` | italique |

Encadrés : `::: {.callout-note title="À retenir"}`, `.callout-important` (Important), `.callout-warning` (Avertissement), `.callout-tip` (Conseil).

Renvois : `@fig-nom` pour une figure, `@lst-nom` pour un code, `@tbl-nom` pour un tableau, `[-@sec-nom]` pour le numéro d'un chapitre ou d'une section.

Codes Epi Info numérotés :

````markdown
::: {#lst-exemple}

```epiinfo
FREQ ILL STRATAVAR=Sex
```

Légende du code

:::
````

## Version LaTeX

Les sources LaTeX de la version déposée sur Zenodo sont archivées dans la branche [`latex`](https://github.com/dieudo13/apprendre-epi-info/tree/latex), téléchargeable en [archive ZIP](https://github.com/dieudo13/apprendre-epi-info/archive/refs/heads/latex.zip).

## Citer ce guide

OUEDRAOGO AD. Apprendre Epi Info 7 : guide pratique d'analyse épidémiologique et statistique. Zenodo; 2026. doi:10.5281/zenodo.24182020

## Licence

© 2026 OUEDRAOGO Ahmed Dieudonné. Ce guide est diffusé sous licence [Creative Commons Attribution – Pas d'utilisation commerciale – Partage dans les mêmes conditions 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr) : vous pouvez le partager et l'adapter en citant l'auteur, sans usage commercial, et en diffusant vos adaptations sous la même licence. Voir le fichier `LICENSE`.

## Avertissement

Ce guide est un travail indépendant. Il n'est ni publié ni approuvé par les CDC. Epi Info est une marque des CDC.
