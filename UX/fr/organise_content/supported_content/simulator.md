# Simulateur de prêt

## Résumé
* [Description](#description)
* [Actions dans Compositeur Digital UX](#actions-dans-compositeur-digital-ux)
* [Extension de dossier](#extension-de-dossier)
* [Créer un simulateur de prêt](#créer-un-simulateur-de-prêt)
* [Métadonnées disponibles](#métadonnées-disponibles)
* [Téléchargez un exemple](#télécharger-un-exemple)

## Description

Ce type de contenu vous permet d'afficher un simulateur de prêt interactif avec des paramètres modifiables.

![Contenu du simulateur de prêt](../../../en/img/content_mortgage_simulator.JPG)

## Actions dans Compositeur Digital UX

Le simulateur de prêt permet les actions suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Capturer | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |
|:--------:|:---------:|:------------------------:|:----------------:|:---------:|:--------:|
| &#x2714; | &#x2714;  | &#x2714;                 | &#x2714;         | &#x2714;  | &#x2714; |

**Interaction avec le contenu**

| Montant global | Montant remboursement mensuel | Taux du prêt | Taux assurance | Nombre d'années de remboursement | In Fine  |
|:--------------:|:-----------------------------:|:------------:|:--------------:|:--------------------------------:|:--------:|
| &#x2714;       | &#x2714;                      | &#x2714;     | &#x2714;       | &#x2714;                         | &#x2714; |

## Extension du contenu

Pour utiliser un simulateur de prêt, ajoutez l'extension `.simupret` à la fin du nom de votre dossier.

## Créer un simulateur de prêt

1. Dans votre univers, créez un dossier nommé `<Nom de votre simulateur de prêt>.simupret` (par exemple `Mon simulateur.simupret`).
1. (Facultatif) Vous pouvez modifier la vignette du simulateur de prêt. Dans votre dossier `.simupret`, mettez une image (`.jpg` ou `.png`) nommée `_preview`. Si vous ne fournissez pas de vignette, l'élément en aura une par défaut (voir ci-dessous).

![dossier simulateur de prêt](../../../en/img/content_mortgage_simulator_folder.JPG) 

![aperçu du simulateur de prêt](../../../en/img/content_mortgage_simulator_preview.JPG)

## Métadonnées disponibles

| Clé de métadonnées                             | Type     | Par défaut           | Description                                      |
|:-----------------------------------------------|:---------|:---------------------|:-------------------------------------------------|
| `simulator.additionalCostsRateDefaultValue`    | `nombre` | 0                    | fixe la valeur par défaut du taux des coûts additionnels |
| `simulator.additionalCostsRateLabel`           | `texte`  | `Coûts additionnels` | fixe l'étiquette de la ligne des coûts additionnels | 
| `simulator.additionalCostsRateMinValue` 	     | `nombre` | 0                    | fixe la valeur minimale du taux de coûts additionnels |
| `simulator.additionalCostsRateMaxValue`        | `nombre` | 50                   | fixe la valeur maximale du taux de coûts additionnels |
| `simulator.additionalCostsRateTickFrequency`   | `nombre` | 1                    | fixe l'intervalle entre deux valeurs pour le taux des coûts additionnels |
| `simulator.creditMaxValue`                     | `nombre` | 800000               | fixe la valeur maximale d'un prêt                 |
| `simulator.creditTickFrequency`                | `nombre` | 5000                 | fixe l'intervalle entre deux valeurs pour un prêt |
| `simulator.creditDefaultValue`                 | `nombre` | 300000               | fixe la valeur du prêt par défaut                 |
| `simulator.durationMinValue`                   | `nombre` | 5                    | fixe la durée la plus courte d'un prêt            |
| `simulator.durationMaxValue`                   | `nombre` | 30                   | fixe la durée la plus longue d'un prêt            |
| `simulator.durationTickFrequency`              | `nombre` | 1                    | fixe l'intervalle entre deux valeurs pour une durée de prêt |
| `simulator.durationDefaultValue`               | `nombre` | 20                   | fixe la durée par défaut d'un prêt                |
| `simulator.hideInfine`                         | `nombre` | faux                 | cacher l'option "in Fine"                         |
| `simulator.infineDefaultValue`                 | `nombre` | faux                 | fixe la valeur par défaut d'une option In Fine    |

## Télécharger un exemple

Un univers de démonstration contenant des exemples de simulateurs de prêts hypothécaires est disponible, [essayez-le !](../../../en/organise_content/Demo-Universe.zip) &#x1f604;

Suivant : [Simulateur d'épargne](savings_simulator.md)

[Retour aux Contenus pris en charge](index.md)
