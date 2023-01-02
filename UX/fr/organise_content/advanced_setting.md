# Paramètres avancés : métadonnées

Vous pouvez modifier le comportement d'un document ou les actions associées en utilisant des paramètres spécifiques décrits dans un fichier nommé `_meta.txt`.

Pour modifier le comportement d'un dossier, le méta-fichier doit être placé dans le dossier cible, et nommé `_meta.txt`.

Pour modifier le comportement d'un document, le méta-fichier doit être nommé d'après le nom du fichier du document suivi du suffixe `_meta` et de l'extension `txt`. Il doit être enregistré au même endroit que le document cible.

> Exemple : pour un fichier nommé `1 - image.jpg`, le méta-fichier correspondant doit être nommé comme suit : `1 - image_meta.txt`.

Dans le méta-fichier, chaque ligne (appelée `meta`) doit décrire un paramètre en utilisant la structure suivante : `metaName = valeur`

Une valeur binaire (vrai ou faux) est décrit comme suit :  `metaName = true`. Sa valeur par défaut est "faux". Les valeurs `1` (true) et `0` (false) peuvent également être utilisées.

Pour appliquer un comportement spécifique à un ensemble de documents, utilisez le préfixe `*.` sur ll paramètre et enregistrez le fichier méta dans le dossier contenant l'ensemble des documents visés

>  Exemple : `*.table.hideCommands = true`

## Résumé 
* [Types de valeurs](#types-de-valeurs)
* [Métadonnées prises en charge](#métadonnées-prises-en-charge)
    * [Annotations](#annotations)
    * [Actions du menu](#actions-du-menu)
    * [Actions configurables](#actions-configurables)
* [Valeurs partagées](#valeurs-partagées)

## Types de valeurs

|Type         | Description                          | Exemples|
|:------------|:-------------------------------------|:--------|
| `texte`     | une chaîne de caractères             | `du texte`, `Mon document` |
| `nombre`    | un nombre entier ou décimal          | `123`, `123.45` |
| `dimension` | taille, en pixels ou un pourcentage, de la visualisation du contenu | `400`, `75%` |
| `booléen`   | vrai ou faux / actif ou inactif      | `true`/`false`, `1`/`0` |
| `couleur`   | code couleur hexadécimal ou code rgb | `#AAAAAA`, `#f03b5e`, `112, 12, 67` |


## Métadonnées prises en charge

| Paramètre                         | Type         | Par défaut   | Description |
|:--------------------------------- |:-------------|:-------------|:------------|
| `culture`                         | `texte`      | -            | indique la langue utilisée dans l'univers. Les valeurs prises en charge sont "fr" ou "en" |
| `canStick`                        | `booléen`    | false        | que l'objet peut être collé comme une note |
| `canWrite`                        | `booléen`    | false        | indique que du texte peut être tapé sur cet objet |
| `desiredHeight`                   | `dimension`  | 400          | définit la hauteur par défaut du document |
| `desiredWidth`                    | `dimension`  | 400          | définit la largeur par défaut du document |
| `desiredPosition(.x|.y)`          | `position`   | auto         | contrôle l'endroint d'apparition du cocument. Définir une valeur relative pour `desiredPosition.x` et `desiredPosition.y` (ex `desiredPosition.x=50%`) une une valeur prédéfinie parmis `center`, `top`,`left`, `right`,`bottom`, `topleft`, `topright`, `bottomleft`, `bottomright` (ex `desiredPosition=center`) |
| `isPaper`                         | `booléen`    | false        | supprime le fond des boutons du document (boutons d'action et de fermeture)|
| `hideBottomBarDots`               | `booléen`    | false        | cache le bouton de la barre inférieure lorsque celle-ci est réduite |
| `hideBottomBar`                   | `booléen`    | false        | cache la barre inférieure lorsque celle-ci est réduite |
| `maxHeight`                       | `dimension`  | -            | définit la hauteur maximale |
| `maxWidth`                        | `dimension`  | -            | définit la largeur maximale |
| `minHeight`                       | `dimension`  | -            | définit la hauteur mimimale |
| `minWidth`                        | `dimension`  | -            | définit la largeur minimale |
| `name`                            | `texte`      | nom du fichier | change le nom affiché du document en "nom A" (exemple) |
| `hidden`                          | `booléen`    | false        | change le nom affiché du document en "nom A" (exemple) |
| `noChromeButtons`                 | `boolean`    | false        | cache les boutons d'action (fermer, menu).|
| `noChromeShadow`                  | `boolean`    | false        | désactive l'ombre sous le document.|
| `noChrome`                        | `booléen`    | false        | cache les boutons d'action (fermer, menu), et l'ombre sous le document.|
| `orientation`                     | `nombre`     | 0            | fait pivoter le document : `-90` pour tourner à gauche, `90` pour tourner à droite ou `180` pour retourner le document |
| `table.noClose`                   | `booléen`    | false        | empêche la fermeture du document (le bouton de fermeture est désactivé et la projection hors de l'écran ne se ferme pas) |
| `table.hideCommands`              | `booléen`    | false        | cache les boutons de contrôle d'un document (page précédente/suivante, contrôles de lecture vidéo...) |
| `table.noRotate`                  | `booléen`    | false        | empêche la rotation du document |
| `table.viewer`                    | `cdux` ou `externe` | non défini  | L'utilisation de `cdux` assure que le lien `cdurl` sera affiché dans le Compositeur Digital UX. Avec `extern`, le document est ouvert en utilisant le viewer natif. |
| `themeColor`                      | `couleur`      | -          | force un thème couleur pour l'univers/élément et son contenu | 
| `table.showOnStart`               | `booléen`    | false        | ouvre le document automatiquement au lancement de l'univers | 
| `noHistory`                       | `boolean`    | false        | le document ne sera pas enregistré dans la corbeille à sa fermeture | 
| `hideLinkLabel`                   | `booléen`    | false        | cache le nom du document dans la barre inférieure de l'univers |
| `hideLinkTypeIcon`                | `boolean`    | false        | cache l'icone de type de document dans les vues de dossier |
| `table.alwaysBehind`              | `boolean`    | false        | force le document à rester en arrière plan |
| `table.alwaysOnTop`               | `boolean`    | false        | force le document à rester au premier plan |
| `toolbox.startOpened`             | `boolean`    | false        | les élement de la boite à outils seront visibles lors de l'affichage de la barre latérale |


### Annotations

Définissez la couleur et la taille du stylet à l'aide des paramètres suivants :

| Metadata Key      | Type         | Default   | Description |
|:----------------- |:-------------|:----------|:-|
| `ink.color`       | `red|orange|yellow|green|turquoise|blue|pink|violet|black|white` | black | définit le couleur par défaut |
| `ink.penName`     | `fine|thick|marker` | fine | définit la taille du stylet |



### Actions du menu

Les actions disopnibles dans le menu de chaque documents sont configurable individuellement. Définissez les paramètres suivant en utilisant `<key>` parmis les actions listées ci-après. 
> Example: 
>
>`actions.saveas.disabled = true`  to hide the "Save as" action
>
>`actions.selection.location = shortcut` to give quick access to the selection action


| Paramètre                  | Type         | Default   | Description |
|:-------------------------- |:-------------|:----------|:-|
| `actions.disabled`         | `boolean`    | false     | cache les bouton d'accès au menu |
| `actions.<key>.disabled`   | `boolean`    | false     | cache l'action `<key>` |
| `actions.<key>.location`   | `menu` or `shortcut`    | menu     | définit si l'action `<key>` doit apparître dasn le menu ou en accès rapide à côté du menu |

### Actions configurables :

| Clef d'action | Description |
|:--------------|-------------|
|`capture`      | Crérer une image de capture du document tel qu'affiché | 
|`selection`    | Ajouter ou retirer le document de la sélection | 
|`duplicate`    | Dupliquer le document | 
|`share`        | Partager le docuement |
|`saveas`       | Enregistrer le document sur l'ordinateur |
|`open`         | Ouvrir le docuement en dehors de l'application |

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

[Retour à Organiser vos contenus](index.md)
