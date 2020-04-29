# Minuteurs

## Résumé
* [Description](#description)
* [Extension de contenu](#extension-de-contenu)
* [Créer un chronomètre] (#créer-un-chronomètre)
* [Créer un compte à rebours] (#créer-un-compte-à-rebours)
* [Créer un minuteur](#créer-un-minuteur)
* [Métadonnées disponibles](#métadonnées-disponibles)

## Description

Ce type de contenu vous permet d'afficher une minuterie. Il peut s'agir soit d'une minuterie, soit d'un chronomètre.

Voici un chronomètre :

! [Chronomètre](../../../en/img/content_stopwatch.jpg)

Et voici une minuterie :

! [Compte à rebours](../../../en/img/content_timer.jpg)

La durée de la minuterie peut être modifiée en cliquant sur l'icône du stylo :

! [édition du compte à rebours](../../../en/img/content_timer_edit.jpg)

Une fois que la minuterie a été activée, elle clignote :

! [Le compte à rebours clignote](../../../en/img/content_timer_ticked.jpg)


## Extension du contenu

Pour utiliser un chronomètre, ajoutez l'extension '.chronomètre ' ou 'chrono' à la fin du nom de votre dossier.
Pour utiliser un compte à rebours, ajoutez l'extension '. countdown' ou '. minuteur' à la fin du nom de votre dossier.
Pour utiliser un chronomètre ou un compte à rebours, ajoutez l'extension 'timer' ou 'horloge'à la fin du nom de votre dossier.

## Créer un chronomètre

1. Dans votre dossier environnement, créez un dossier nommé `<nom de votre chronomètre>.chronomètre` (par exemple `Mon chronomètre.chronomètre`).
1. (Facultatif) Vous pouvez modifier l'aperçu du chronomètre. Dans votre dossier `.chronomètre`, mettez une image (`.jpg` ou `.png`) nommée `_preview`. Si vous ne fournissez pas de `_preview`, l'élément aura une prévisualisation par défaut (voir ci-dessous).

## Créer un compte à rebours

1. Dans votre dossier environnement, créez un dossier nommé `<(heures)h(minutes)m(secondes)s>.countdown` (par exemple `5m30s.countdown`). Il créera un compte à rebours initialisé pour une durée de 5 minutes et 30 secondes.
1. (Facultatif) Vous pouvez également définir la durée de votre minuteur dans un fichier `_meta.txt`. Ajoutez la valeur : 
   * `timer.duration = 5m30s` pour créer un minuteur qui doit durer 5 minutes et 30 secondes.
   * `timer.format = HH:mm` combiné avec `timer.duration = 05:30` crée également un minuteur qui doit durer 5 minutes et 30 secondes.
1. (Facultatif) Votre minuterie peut être silencieuse. Ajoutez la ligne `timer.silent = true` dans un fichier `_meta.txt`.
1. (Facultatif) La sonnerie peut être personnalisée. Ajoutez un fichier nommé `_alarm.mp3` ou `_alarm.wav` dans votre dossier `.countdown`.
1. (Optionnel) Vous pouvez changer l'aperçu du minuteur. Dans votre dossier `.timer`, mettez une image (`.jpg` ou `.png`) nommée `_preview`. Si vous ne fournissez pas de `_preview`, l'élément aura un aperçu par défaut (voir ci-dessous).

## Créer un minuteur 

1. Dans votre dossier environnement, créez un dossier nommé `<(heures)h(minutes)m(secondes)s>.timer` (par exemple `5m30s.tilmer`). Il créera un compte à rebours initialisé pour une durée de 5 minutes et 30 secondes. Vous pouvez également le changer en chronomètre en cliquant sur l'icône du chronomètre.

! [Chronomètre](../../../en/img/content_timer2.jpg)

1. (Facultatif) Vous pouvez également définir la durée de votre minuteur dans un fichier `_meta.txt`. Ajoutez la valeur : 
   * `timer.duration = 5m30s` pour créer un minuteur qui doit durer 5 minutes et 30 secondes.
   * `timer.format = HH:mm` combiné avec `timer.duration = 05:30` crée également un minuteur qui doit durer 5 minutes et 30 secondes.
1. (Facultatif) Votre minuterie peut être silencieuse. Ajoutez la ligne `timer.silent = true` dans un fichier `_meta.txt`.
1. (Facultatif) La sonnerie peut être personnalisée. Ajoutez un fichier nommé `_alarm.mp3` ou `_alarm.wav` dans votre dossier `.countdown`.
1. (Optionnel) Vous pouvez changer l'aperçu du Timer. Dans votre dossier `.timer`, mettez une image (`.jpg` ou `.png`) nommée `_preview`. Si vous ne fournissez pas de `_preview`, l'élément aura un aperçu par défaut (voir ci-dessous).

[Aperçu du minuteur](../../../en/img/content_timer_preview.png)

## Métadonnées disponibles

| Clé de métadonnées | Type   | Par défaut | Description |

| `timer.silent`     | `bool` | faux       | met le minuteur en mode silencieux |
| `timer.duration`   | `texte`| 0          | définit la durée de la minuterie (par exemple 1h5m30s pour 1 heure, 5 minutes et 30 secondes). Si un `timer.format` est défini, il essaie d'analyser la durée avec le format. |
| `timer.format`     | `text` | -          | définit le format à utiliser lors de l'analyse de la durée (par exemple `hhh:mm:ss`) |

suivant : [Diaporamas (Compositeur Digital UX format)](slideshows.md)





[Retour au contenu pris en charge](index.md)
