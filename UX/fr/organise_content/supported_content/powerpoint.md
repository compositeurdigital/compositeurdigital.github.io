# Powerpoint

## Résumé
* [Description](#description)
* [Extensions de fichiers](#extensions-de-fichiers)
* [Actions dans Compositeur Digital UX](#actions-dans-compositeur-digital-ux)
* [Hot Spots](#hot-spots)
* [Diaporama](#diaporama)
* [Métadonnées disponibles](#métadonnées-disponibles)

## Description

Les Powerpoints sont pris en charge nativement par Compositeur Digital UX.

![Powerpoints affichés dans le Compositeur Digital UX](../../../en/img/content_powerpoint.JPG)

## Extensions de fichiers

Les formats pris en charge sont `.pptx` et `.ppsx`.

## Actions dans Compositeur Digital UX

Les Powerpoints prennent en charge les actions suivantes. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md).

**Menu des actions**

| Capturer | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager | Diapositives |
|:--------:|:---------:|:------------------------:|:----------------:|:---------:|:--------:|:------------:|
| &#x2714; | &#x2714;  | &#x2714;                 | &#x2714;         | &#x2714;  | &#x2714; | &#x2714;     | 

**Interaction avec le contenu**

| Annoter  | Mode extraction d'image | Hyperliens | Hot spots | Suivant  | Précédent | 
|:--------:|:-----------------------:|:----------:|:---------:|:--------:|:---------:|
| &#x2714; | &#x2714;                | &#x2714;   | &#x2714;  | &#x2714; | &#x2714;  |

## Hot spots

Vous pouvez créer un Hot spot sur un document pour ouvrir un autre document lorsqu'on vient toucher le Hot spot. Cette interaction est créée à l'aide de l'éditeur Powerpoint de Microsoft.

![Hot spots](../../../en/img/content_powerpoint_hot_spots.JPG)

1. Créez une forme transparente au-dessus de la zone active sélectionnée. La forme doit couvrir toute la zone active.

**Avertissement : Si la zone est une zone de texte, sélectionnez la zone de texte. Ne pas sélectionner le TEXTE**

2. Sélectionnez la forme, et allez dans INSÉRER 
3. Allez sur HyperLink et définissez l'emplacement du document cible.

> Note 1 : Le document cible doit se trouver quelque part dans votre dossier univers. Vous pouvez utiliser la fonction de dossier `.content` si vous ne souhaitez pas afficher le dossier cible dans votre univers.

> Note 2 : Vous pouvez également faire un clic droit sur la forme et aller dans le menu HyperLink
	
4. Enregistrez votre présentation Powerpoint à l'endroit souhaité dans votre dossier univers.

## Métadonnées disponibles

| Paramètre                         | Type      | Default | Description |
|:--------------------------------- |:----------|:--------|:-|
| `video.controls.position`         | `auto|bottom|left|right|leftandright` | auto   | définit la position ou s'affichent les boutons page suivante/précédente |
| `video.controls.hide`             | `boolean` | false   | cache les boutons page suivante/précédente |

[Accéder aux métadonnées communes](../advanced_setting.md#résumé)

Lorsque la position est paramétré `auto`, la position sera `leftandright` si la rotation des documents est activée, sinon `bottom`.
![Slideshow controls position](../../../en/img/slideshow_controls.jpg)

## Diaporama

Par défaut, les fichiers Powerpoint sont gérés par Compositeur Digital UX comme l'extension `.slideshow` ([voir la section Diaporama](slideshows.md)).

Suivant : [Fichiers vidéo](video.md)

[Retour aux Contenus pris en charge](index.md)
