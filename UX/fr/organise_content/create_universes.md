# Créer vos univers

Le Compositeur Digital UX traite les documents stockés dans un endroit spécifique de votre ordinateur. Ces documents peuvent être organisés en dossiers pour faciliter la présentation.

## Résumé
* [Compétences et ressources requises](#Compétences-et-ressources-requises)
* [Extensions de fichiers](#extensions-de-fichiers)
* [Univers](#univers)
* [Fond](#fond)
* [Fond interactif](#fond-interactif)
* [Dossiers](#dossiers)
  * [Fonctionnalité des dossiers cachés](#fonctionnalité-des-dossiers-cachés)
* [Documents](#documents)
* [Ordre de visualisation du contenu](#ordre-de-visualisation-du-contenu)
* [Vignettes](#vignettes)
  * [Vignette de dossier ](#vignette-de-dossier)
  * [Vignette de document](#vignette-de-document)
* [Personnaliser l'espace de travail](#personnaliser-lespace-de-travail)
* [Univers de démonstration](#univers-de-démonstration) 


## Compétences et ressources requises

La préparation d'un univers se fait à l'aide de l'explorateur de fichiers de Microsoft Windows

Vous devez être à l'aise avec : 

- La création et l'organisation de dossiers 
- Le renommage des fichiers et des dossiers

## Extensions de fichiers

Compositeur Digital UX utilise l'extension de fichier pour configurer les différents éléments d'un univers.  L'extension de fichier indiquant le type de document est généralement un ensemble de 3 à 4 caractères suivant le point dans le nom du fichier :

- Images : par exemple `photo1.jpg`, `photo2.png`.
- Présentation : par exemple `pres1.pptx`, `pres2.pdf`.
- Fichier texte : par exemple `tableau de contenu.txt`.

Par défaut, l'explorateur de fichiers de Microsoft Windows cache les extensions de fichiers. Nous vous recommandons vivement de modifier ce paramètre.


![Activer les extensions de fichiers](../../en/img/enable_file_extensions.JPG)

## Univers

Techniquement, un univers se matérialise sous la forme d'un dossier sur votre ordinateur. Par défaut, Compositeur Digital UX recherche le contenu situé dans `Documents\Compositeur Digital UX`

![Dossier univers](../../en/img/universe_folder.JPG)

Pour créer votre propre univers, vous pouvez dupliquer un univers existant dans l'emplacement par défaut : `Documents\Compositeur Digital UX`.

## Fond

Vous pouvez personnaliser votre univers en changeant l'image de fond. Pour ce faire, il suffit d'ajouter un fichier image (`.png` ou `.jpg`) nommé `_background` dans le dossier de l'univers.

![Dossier fond de l'univers](../../en/img/universe_background.JPG) 

![Universe background Compositeur Digital UX](../../en/img/universe_background_cdux.JPG)

### Ratio de manipulation de votre écran

Différents arrière-plans peuvent être définis, adaptés à différents formats d'écran. Par exemple, un fichier nommé `_background3_2` sera sélectionné si l'application est exécutée sur un périphérique qui correspond à un écran 3:2.

Voici une liste de tous les formats d'écran pris en charge.

| Format| Nom du fichier     | Tailles (exemples en pixels, FullHD) |
|:-----:|:------------------:|:----------------------------:|
| 3:2   | `_background3_2`   | 2496x1664 |
| 4:3   | `_background4_3`   | 2500x1875 |
| 5:4   | `_background5_4`   | 2500x2000 |
| 16:9  | `_background16_9`  | 1920×1080 |
| 16:10 | `_background16_10` | 1920x1280 |

L'utilisation de différents fichiers de fond, adaptés à différents formats d'écran, vous permet de vous assurer que vous pouvez visualiser votre univers sur n'importe quel format d'écran.

## Fond interactif

Si vous souhaitez avoir un fond interactif, qui contient des hyperliens pour afficher votre contenu, c'est également possible. Préparez un fichier powerpoint, avec une diapositive contenant votre image de fond. Dans cette diapositive, n'oubliez pas de créer des [Hot Spots](../supported_content/powerpoint.md#hot-spots) pour afficher vos menus, ou vos fichiers. Le nom du fichier doit être `_background.pptx`. 

![Dossier fond interactif](../../en/img/interactive_background.JPG)

## Dossiers

Vous pouvez organiser vos documents dans des dossiers et des sous-dossiers. 

Le premier niveau de dossiers est affiché dans le Compositeur Digital UX dans le dock situé en bas de la vue de l'univers. 

![Dossier univers](../../en/img/universe_background.JPG)
![Dock univers](../../en/img/universe_dock.JPG)

>### Fonctionnalité des dossiers cachés
>
>Les dossiers dont le nom se termine par `.content` ou `.hidden` ne seront pas affichés dans le Compositeur Digital UX.
>Voir [Powerpoints Hot Spots](supported_content/powerpoint.md#hot-spots) pour voir l'utilisation courante de cette fonctionnalité.

## Documents

Il suffit de glisser et de déposer vos documents dans les dossiers et sous-dossiers pour remplir votre univers.

Consultez les [contenus pris en charge](supported_content/index.md) pour obtenir une liste exhaustive des types de fichiers pris en charge.

## Ordre de visualisation du contenu

Le Compositeur Digital UX affichera les dossiers et les documents par ordre alphabétique. Vous pouvez toutefois forcer une séquence d'affichage spécifique pour les documents et les dossiers en préfixant le nom du fichier ou du dossier par un numéro. Compositeur Digital UX n'affichera pas les numéros mais organisera les éléments en conséquence.


## Vignettes 

Le Compositeur Digital UX crée automatiquement des vignettes pour tous les documents. Vous pouvez personnaliser la vignette de chaque document ou dossier de votre univers.

### Vignette de dossier 

Si une vignette n'a pas été définie pour un dossier, le Compositeur Digital UX créera automatiquement une vignette basée sur le premier document du dossier.

![Pas de miniature](../../en/img/universe_no_preview.JPG) 
![Pas de doc miniature](../../en/img/universe_no_preview_dock.JPG)

Pour créer une vignette pour un dossier, il suffit de déposer un fichier image nommé `_preview` (`.png` ou `.jpg`) directement dans le dossier :


![Avec miniature](../../en/img/universe_preview.JPG) 
![Avec doc miniature](../../en/img/universe_preview_dock.JPG)

### Vignette de document

Pour personnaliser la vignette d'un document, déposez un fichier image portant le même nom mais avec le suffixe `_preview` dans le même dossier.

![Avec miniature de document](../../en/img/universe_document_preview.JPG) 
![Avec miniature de document doc](../../en/img/universe_document_preview_dock.JPG)

## Personnaliser l'espace de travail

Il est possible de changer l'icône du menu. Par défaut, nous utilisons une icône de menu "hamburger". Vous pouvez fournir votre propre icône. Il suffit d'ajouter un fichier `.png` nommé `_sidemenuicon.png` à la racine de votre univers.

Vous pouvez également cacher les trois points de la barre du bas lorsque la barre est réduite. Ajoutez un fichier `_meta.txt` avec une ligne `hideBottomBarDots = true`.


![Espace de travail personnalisé](../../en/img/universe_custom_ui.JPG)

## Univers de démonstration

Un univers de démonstration est disponible et peut être [téléchargé ici](../../en/organise_content/Demo-Universe.zip). Une fois téléchargé, dézippez le fichier et placez le contenu dans votre dossier `Compositeur Digital UX`. Cet univers de démonstration comprend des exemples pour chaque type de contenu que vous pouvez créer dans le Compositeur Digital UX.

Suivant : [Contenus](supported_content/index.md)

[Retour à Organiser vos contenus](index.md)
