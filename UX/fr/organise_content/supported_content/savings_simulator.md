# Simulateur d'épargne

## Résumé
* [Description](#description)
* [Actions au sein de Compositeur Digital UX] (#actions-au-sein-du-compositeur-digital-ux)
* [Extension de contenu](#extension-du-content)
* [Créer un simulateur d'épargne] (#créer-un-simulateur-d'épargne)
* [Métadonnées disponibles](#métadonnées-disponibles)
* [Téléchargez un exemple] (#télécharger-un-exemple)

## Description

Ce type de contenu vous permet d'afficher un simulateur d'épargne interactif avec des paramètres modifiables.

[Simulateur d'épargne de contenu](../../../en/img/content_savings_simulator.JPG)

## Actions au sein de Compositeur Digital UX

Le simulateur d'épargne prend en charge l'action suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter   | Capturer  | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |

| &#x2716 ; | &#x2714 ; | &#x2714 ; | &#x2714 ;                | &#x2714 ;        | &#x2714 ; | &#x2714 ; |

## Extension du contenu

Pour utiliser un simulateur d'épargne, ajoutez l'extension '.simuinvest' à la fin du nom de votre dossier.

## Créer un simulateur d'épargne

1. Dans votre dossier environnement, créez un dossier nommé `<Nom de votre simulateur d'épargne>.simuinvest` (par exemple `Mon simulateur.simuinvest`).
1. (Facultatif) Vous pouvez modifier l'aperçu du simulateur d'épargne. Dans votre dossier `.simuinvest`, mettez une image (`.jpg` ou `.png`) nommée `_preview`. Si vous ne fournissez pas de `_preview`, l'élément aura un aperçu par défaut (voir ci-dessous).

! [Dossier du simulateur d'économies](../../../en/img/contenu_économies_simulateur_dossier.JPG) ! [Aperçu du simulateur d'épargne](../../../en/img/contenu_économies_simulateur_preview.JPG)

## Métadonnées disponibles

| Clé de métadonnées                      | Type     | Par défaut | Description |

| `simulator.depositFrequencyDefault`     | `texte`  | `Mois`     | fixe la valeur par défaut de la fréquence de dépôt. Il peut s'agir de "mois", "trimestre" ou "année".
| `simulator.interestRateMinValue`        | `nombre` | 0          | fixe la valeur min du taux d'intérêt |
| `simulator.interestRateMaxValue`        | `nombre` | 10         | fixe la valeur maximale du taux d'intérêt |
| `simulator.interestRateDefaultValue`    | `nombre` | 2.75       | définit la valeur par défaut du taux d'intérêt |
| `simulator.regularDepositMinValue`      | `nombre` | 10         | fixe la valeur minimale du dépôt |
| `simulator.regularDepositMaxValue`      | `nombre` | 20000      | fixe la valeur maximale du dépôt |
| `simulator.regularDepositTickFrequency` | `nombre` | 100        | fixe l'intervalle entre deux valeurs pour un dépôt |
| `simulator.savingsTermMinValue`         | `nombre` | 0          | fixe la durée la plus courte d'un plan d'épargne |
| `simulator.savingsTermMaxValue`         | `nombre` | 30         | fixe la durée la plus longue d'un plan d'épargne |
| `simulator.savingsTermDefaultValue`     | `nombre` | 20         | fixe la durée par défaut d'un plan d'épargne |
| `simulator.savingsTermTickFrequency`    | `nombre` | 1          | fixe l'intervalle entre deux valeurs pour une durée de plan d'épargne |
| `simulator.startingDepositMinValue`     | `nombre` | 0          | fixe la valeur min pour le montant du dépôt de départ |
| `simulator.startingDepositMaxValue`     | `nombre` | 800000     | fixe la valeur maximale du montant du dépôt de départ |
| `simulator.startingDepositTickFrequency`| `nombre` | 5000       | fixe l'intervalle entre deux valeurs pour un montant de dépôt de départ |

## Télécharger un exemple

Un univers de démonstration contenant des exemples de simulateur d'épargne est disponible, [essayez-le !](../Demo-Universe.zip) &#x1f604 ;


suivant : [Calculatrice](calculateur.md)

[Retour au contenu pris en charge](index.md)
