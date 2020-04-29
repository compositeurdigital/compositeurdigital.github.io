# Paramètres avancés : métadonnées

Vous pouvez modifier le comportement d'un document ou les actions associées en utilisant des paramètres spécifiques décrits dans un fichier nommé `_meta.txt`.

Pour modifier le comportement d'un dossier dans l'application, le méta-fichier doit être placé dans le dossier cible, et nommé `_meta.txt`.

Pour modifier le comportement d'un document dans l'application, le méta-fichier doit être nommé d'après le nom du fichier du document suivi du suffixe `_meta` et de l'extension `txt`. Il doit être enregistré au même endroit que le document cible.

> Exemple : pour un fichier nommé `1 - image.jpg`, le méta-fichier correspondant doit être nommé comme suit : `1 - image_meta.txt`.

Dans le méta-fichier, chaque ligne (appelée `meta`) doit décrire un paramètre en utilisant la structure suivante : `metaName = valeur`

Un méta binaire (vrai ou faux) est décrit comme suit :  `metaName = vrai`. Sa valeur par défaut est "faux". Les valeurs `1` (vrai) et `0` (faux) peuvent également être utilisées.

Pour appliquer un comportement spécifique à un ensemble de documents, utilisez le préfixe `*.` sur la description du méta et enregistrez le fichier méta dans le dossier contenant l'ensemble des documents visés

>  Exemple : `*.table.hideCommands = true`

## Résumé 
* [Types de valeurs](#types-de-valeurs)
* [Métadonnées prises en charge] (#métadonnées-prises-en-charge)
* [Métadonnées spécifiques au contenu](#métadonnées-spécifiques-au-contenu)
  * [Vidéo et audio](#vidéo-et-audio)
  * [Web](#web)
  * [simulateur de prêt] (#simulateur-d'hypothèque)
  * [Simulateur d'épargne] (#simulateur-d'épargne)
  * [objets 3D] (#objets-3d)
  * [Interface de recherche](#interfaces-de-recherche)
* [Valeurs partagées](#valeurs-partagées)

## Types de valeurs

|Type         | Description                 | Exemples|
|:------------|:----------------------------|:--------|
| `texte`     | une chaîne de caractères    | `du texte`, `Mon document` |
| `nombre`    | un nombre entier ou décimal | `123`, `123.45` |
| `dimension` | une taille en pixels ou un pourcentage de la visualisation du contenu | `400`, `75%` |
| `booléen`   | vrai ou faux                | `vrai`/`faux`, `1`/`0` |
| `couleur`   | code couleur hexadécimal ou code rgb | `#AAAAAA`, `#f03b5e`, `112, 12, 67` |


## Métadonnées prises en charge

| Clé de métadonnées                | Type         | Par défaut   | Description |
|:--------------------------------- |:-------------|:-------------|:------------|
| `actions.disabled`                | `booléen`    | faux         | cache le bouton de menu sur un document. |
| `actions.capture.disabled`        | `booléen`    | faux         | cache l'action de capture. |
| `actions.duplicate.disabled`      | `booléen`    | faux         | cache l'action en double. |
| `actions.ink.disabled`            | `booléen`    | faux         | cache l'action de l'encre. |
| `actions.open.disabled`           | `booléen`    | faux         | cache l'action ouvrir. |
| `actions.saveas.disabled`         | `booléen`    | faux         | cache l'action enregistrer sous. |
| `actions.selection.disabled`      | `booléen`    | faux         | cache l'action de sélection. |
| `actions.selection.location`      | `texte`      | Menu         | définit si l'action de sélection doit se trouver dans le menu de l'élément ou être disponible comme raccourci. |
| `actions.share.disabled`          | `booléen`    | faux         |  cache l'action partager. |
| `culture`                         | `texte`      | non définit  | indique la langue utilisée dans l'univers. Les valeurs prises en charge sont "fr" ou "en" |
| `canStick`                        | `booléen`    |faux          | que l'objet peut être collé comme une note |
| `canWrite`                        | `booléen`    |faux          | indique que du texte peut être tapé sur cet objet |
| `desiredHeight`                   | `dimension`  | 400          | définit la hauteur par défaut du document |
| `desiredWidth`                    | `dimension`  | 400          | définit la largeur par défaut du document |
| `isPaper`                         | `booléen`    | faux         | supprime le fond des boutons du document (boutons d'action et de fermeture)|
| `hideBottomBarDots`               | `booléen`    | faux         | cache le bouton de la barre inférieure |
| `maxHeight`                       | `dimension`  | -            | définit la hauteur maximale |
| `maxWidth`                        | `dimension`  | -            | définit la largeur maximale |
| `minHeight`                       | `dimension`  | -            | définit la hauteur mimimale |
| `minWidth`                        | `dimension`  | -            | définit la largeur minimale |
| `name`                            | `texte`      | nom du fichier | change le nom affiché du document en "nom A" (exemple) |
| `noChrome`                        | `booléen`    | faux         |  cache tous les boutons chromés (fermer, menu), et l'ombre sous le document.|
| `orientation`                     | `nombre`     | 0            | fait pivoter le document : `-90` pour tourner à gauche, `90` pour tourner à droite ou `180` pour retourner le document |
| `table.noClose`                   | `booléen`    | faux         | empêche la fermeture du document (le bouton de fermeture est désactivé et la projection hors de l'écran ne se ferme pas) |
| `table.hideCommands`              | `booléen`    | faux         | cache les boutons de contrôle d'un document (page précédente/suivante, contrôles de lecture vidéo...) |
| `table.noRotate`                  | `booléen`    | faux         | empêche la rotation du document |
| `table.viewer`                    | `cdux` ou `externe` | non définit   | L'utilisation de `cdux` assure que le lien `cdurl` sera affiché dans le Compositeur Digital UX. Avec `extern`, le document est ouvert en utilisant le viewer natif. |
| `themeColor`                      | `couleur`      | -          | force un thème couleur pour l'univers/élément et son contenu | 
| `table.showOnStart`               | `booléen`    | faux         | ouvre le document automatiquement au lancement de l'univers | 
| `hideLinkLabel`                   | `booléen`    | faux         | cache le nom du document dans la barre inférieure de l'univers |

## Métadonnées spécifiques au contenu

### Video et audio

| Clé de métadonnées                | Type      | Par défaut | Description |
|:--------------------------------- |:----------|:-----------|:------------|
| `video.autoplay`                  | `booléen` | vrai       | démarre la lecture de la vidéo sur l'écran |
| `video.autoplay.delay`            | `nombre`  | 0          | retarde la lecture automatique du nombre de secondes spécifié |
| `video.autoclose`                 | `booléen` | faux       | ferme la vidéo lorsque la lecture arrive à son terme |
| `video.autoclose.delay`           | `nombre ` | 0          | retarde la fermeture automatique du nombre de secondes spécifié |
| `video.mute`                      | `booléen` | faux       | définit si une vidéo est mise en sourdine ou non  |
| `video.rewind`                    | `booléen` | faux       | revient à la première image quand la vidéo se termine |
| `video.loop`                      | `booléen` | faux       | reprend au début lorsque la vidéo se termine |
| `video.controls.alwaysvisible`    | `booléen` | faux       | force l'affichage des commandes de lecture vidéo |
| `video.controls.hide`             | `booléen` | faux       | cache les contrôles de lecture vidéo en permanence |

### Web

| Clé de métadonnées                | Type      | Par défaut | Description |
|:--------------------------------- |:----------|:-----------|:------------|
| `web.manipulationMode`            | `nombre`  | 0          | Si "1", l'utilisateur devra activer le mode de navigation, alors l'affichage se comportera comme un navigateur. Si `0`, le mode de navigation sera réduit. |
| `web.showChrome`                  | `booléen` | faux       | affiche une barre de navigation en haut de la vue |
| `web.viewport.width`              | `nombre`  | 1000       | Définit la largeur par défaut de la vue de la page |
| `web.viewport.height`             | `nombre`  | 800        | Définit la hauteur par défaut de la vue de la page |

### Simutateur d'hypothèque

| Clé de métadonnées                           | Type     | Par défaut         | Description |
|:-------------------------------------------- |:---------|:-------------------|:------------|
| `simulator.additionalCostsRateDefaultValue`  | `nombre` | 0                  | définit la valeur par défaut du taux des coûts additionnels |
| `simulator.additionalCostsRateLabel`         | `texte`  | `Coûts additionnels`| définit l'étiquette de la ligne des coûts additionnels | 
| `simulator.additionalCostsRateMinValue`      | `nombre` | 0                  | définit la valeur minimale du taux de coûts additionnels |
| `simulator.additionalCostsRateMaxValue`      | `nombre` | 50                 | définit la valeur maximale du taux des coûts additionnels |
| `simulator.additionalCostsRateTickFrequency` | `nombre` | 1                  | définit l'intervalle entre deux valeurs pour le taux des coûts additionnels |
| `simulator.creditMaxValue`                   | `nombre` | 800000             | définit la valeur maximale d'un prêt |
| `simulator.creditTickFrequency`              | `nombre` | 5000               | définit l'intervalle entre deux valeurs pour un prêt |
| `simulator.creditDefaultValue`               | `nombre` | 300000             | définit la valeur du prêt par défaut |
| `simulator.durationMinValue`                 | `nombre` | 5                  | définit la durée la plus courte d'un prêt |
| `simulator.durationMaxValue`                 | `nombre` | 30                 | définit la durée la plus longue d'un prêt |
| `simulator.durationTickFrequency`            | `nombre` | 1                  | définit l'intervalle entre deux valeurs pour une durée de prêt |
| `simulator.durationDefaultValue`             | `nombre` | 20                 | définit la durée par défaut d'un prêt |

### Simulateur d'épargne

| Clé de métadonnées                           | Type     | Par défaut         | Description |
|:-------------------------------------------- |:---------|:-------------------|:------------|
| `simulator.depositFrequencyDefault`          | `texte`  | `Mois`             | définit la valeur par défaut de la fréquence de dépôt. Il peut s'agir de "Mois", "Trimestre" ou "Année". |
| `simulator.interestRateMinValue`             | `nombre` | 0                  | définit la valeur minimale du taux d'intérêt |
| `simulator.interestRateMaxValue`             | `nombre` | 10                 | définit la valeur maximale du taux d'intérêt  |
| `simulator.interestRateDefaultValue`         | `nombre` | 2.75               | définit la valeur par défaut du taux d'intérêt |
| `simulator.regularDepositMinValue`           | `nombre` | 10                 | définit la valeur minimale des dépôts |
| `simulator.regularDepositMaxValue`           | `nombre` | 20000              | définit la valeur maximale des dépôts |
| `simulator.regularDepositTickFrequency`      | `nombre` | 100                | définit l'intervalle entre deux valeurs pour un dépôt |
| `simulator.savingsTermMinValue`              | `nombre` | 0                  | définit la durée la plus courte d'un plan d'épargne |
| `simulator.savingsTermMaxValue`              | `nombre` | 30                 | définit la durée la plus longue d'un plan d'épargne |
| `simulator.savingsTermDefaultValue`          | `nombre` | 20                 | définit la durée par défaut d'un plan d'épargne |
| `simulator.savingsTermTickFrequency`         | `nombre` | 1                  | définit l'intervalle entre deux valeurs pour la durée d'un plan d'épargne |
| `simulator.startingDepositMinValue`          | `nombre` | 0                  | définit la valeur minimale du montant du dépôt de départ |
| `simulator.startingDepositMaxValue`          | `nombre` | 800000             | définit la valeur maximale du montant du dépôt de départ |
| `simulator.startingDepositTickFrequency`     | `nombre` | 5000               | définit l'intervalle entre deux valeurs pour un montant de dépôt initial |

### Objets 3D

| Clé de métadonnées                | Type     | Par défaut | Description |
|:--------------------------------- |:---------|:-----------|:------------|
| `obj3D.backgroundcolor`           | `couleur | #dce1e1    | définit une couleur de fond unie |
| `obj3D.camera.h`                  | `nombre` | 0          | définit l'azimut par défaut (rotation horizontale) pour la position de la caméra |
| `obj3D.camera.v`                  | `nombre` | 0          | définit l'inclinaison par défaut (rotation verticale) pour la position de la caméra|
| `obj3D.renderingmode`             | `texte`  | Normal     | définit le mode de rendu de l'objet. Les modes pris en charge sont `Normal` (mode par défaut), `Transparent` et `Wireframe'. |

### Interfaces de recherche

| Clé de métadonnées                | Type     | Par défaut | Description |
|:----------------------------------|:---------|:-----------|:------------|
| `catalog.resultsMaxCount`         |`nombre`  | 40         | Le nombre maximum de résultats qui peuvent être visualisés dans la page de résultats. |

## Valeurs partagées

Certaines valeurs peuvent être partagées entre différents éléments, par exemple des informations sur un contact dans un quiz ou le résultat d'un prêt hypothécaire.

| Clé partagée                     | Type      | Description |
|:---------------------------------|:----------|:------------|
| `firstName`                      | `texte`   | définit le prénom du contact actuel |
| `lastName`                       | `texte`   | définit le nom du contact actuel |
| `email`                          | `texte`   | définit l'email du contact actuel |
| `phoneNumber`                    | `texte`   | définit le numéro de téléphone du contact actuel |
| `organization`                   | `texte`   | définit l'organisation du contact actuel |
| `finance.budget`                 | `nombre`  | définit le montant du prête hypothécaire du contact actuel |



[Back to Organise Content](index.md)
