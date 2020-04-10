# Interface de recherche

## Résumé
* [Description](#description)
* [Actions au sein du Compositeur Digital UX] (#actions-au-sein-du-compositeur-digital-ux)
* [Extension de contenu](#extension-de-contenu)
  * [Tableur : \_list.csv ou \_catalog.csv](#tableur--_listcsv-ou-_catalogcsv)
  * [extension '.recherche'] (#extension-search)
  * [Extension`.filtres`](#extension-filtres)
  * [extensions '.appartements'](#extension-appartements)
* [Créer une interface de recherche] (#créer-une-interface-de-recherche)
* [Métadonnées disponibles](#métadonnées-disponibles)
* [Téléchargez un exemple] (#télécharger-un-exemple)


## Description 

Ce type de contenu vous permet d'afficher une interface de recherche pour tout élément (par exemple, appartements, plans, voitures, etc.) qui est placé dans le même dossier.

! [Interface de recherche : filtres](../../../en/img/content_filters.JPG)

Les interfaces de recherche peuvent également inclure des zones de texte qui permettront à l'utilisateur de trouver des éléments en fonction de leur nom ou de leurs mots clés.

! [Interface de recherche : texte (nom de l'élément)](../../../en/img/content_filters_text_items_name.JPG)

! [Interface de recherche : texte (mots-clés)](../../../en/img/content_filters_text_keywords.JPG)

## Actions au sein du Compositeur Digital UX

Les interfaces de recherche prennent en charge l'action suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter   | Capturer  | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |

| &#x2716 ; | &#x2716 ; | &#x2714 ; | &#x2716 ;                | &#x2716 ;        | &#x2714 ; | &#x2716 ; |

**Interaction avec l'article**

| Filtres  | Lancez les articles |
|:--------:|:------------:|
| &#x2714 ;| &#x2714 ; | 

## Extension du contenu

Pour utiliser une interface de recherche, mettez tous les éléments dont vous avez besoin dans un dossier, et ajoutez l'extension '.filtres' ou '.recherche' ou '.appartements' (pour les besoins immobiliers) à la fin du nom de votre dossier.

À l'intérieur de votre dossier, fournissez un fichier nommé `_list.csv` ou `_catalog.csv`. Il n'y a pas de différences entre ces fichiers, mais seuls ces noms sont pris en charge par le Compositeur Digital UX.

### Tableur : \_list.csv ou \_catalog.csv

Ce fichier contient l'ensemble des données qui seront utilisées pour les critères de recherche. Ce document est un fichier `.csv`, utilisant `;` comme délimiteurs. Il peut être édité en utilisant Microsoft Excel. 

![\_list.csv sample](../../../en/img/content_search_csv.JPG)

**Format**

La première ligne de la feuille de calcul représente le *type de critères*. Sélectionnez l'un des critères suivants :

| Clés          | Description                |
|:--------------|:------------------------------------------------------------------------------------------------------|
| `id`          | ** OBLIGATOIRE**. Cette colonne doit correspondre à un nom de document dans le dossier. Elle ne sera pas affichée comme critère mais sera utilisée pour ouvrir un résultat.                                                                                          |
| `double`      | Critères d'affichage d'un nombre décimal.                                                             |
| `float`       | Critères d'affichage d'un nombre décimal.                                                             |
| `int`         | Critères de sélection d'un nombre entier.                                                                        |
| `itemName`    | Colonne blanche. Crée une zone de texte où l'utilisateur peut filtrer les éléments en fonction de leur nom.                       |
| `multiple`    | Critères de sélection multiple.                                                                      |
| `price`       | Représente un prix. Ne pas préciser l'unité.                                                              |
| `single`      | Critères pour le choix unique.                                                                          |
| `surface`     | Représente une surface. Tapez "m²". Ne précisez pas l'unité.                                             |
| `text`        | rempli de mots-clés associés à chaque ligne. Crée une zone de texte où l'utilisateur peut filtrer les éléments en fonction des mots clés qui leur sont associés. Les mots-clés sont séparés par ' \| ' dans le fichier " .csv ". |
| `floor`       | Niveau du sol (cas d'utilisation d'un bien immobilier).                                                                   |
| `orientation` | Critères de sélection d'une orientation (par exemple "Nord", "Sud"... cas d'utilisation de biens immobiliers).                    |
| `state`       | Critères de sélection d'un état (cas d'utilisation de biens immobiliers).                                                    |
| `type`        | Nombre de pièces (cas d'utilisation d'un bien immobilier).                                                                |
| `visual`      | Critères de sélection d'un visuel (cas d'utilisation d'un bien immobilier).                                                   |

La deuxième ligne de la feuille de calcul représente le nom du critère, qui sera affiché dans l'interface de recherche.

À partir de la troisième ligne, chaque ligne représente un élément qui peut être recherché à l'aide de l'interface de recherche.

### Extension`.recherche` 

L'extension '.recherche ' est utile pour afficher une interface de recherche qui n'est pas dynamique. L'utilisateur sélectionne tous les filtres qu'il souhaite appliquer, puis appuie sur un bouton intitulé "Recherche". Les résultats de la recherche sont calculés et les éléments correspondant aux critères sont affichés.

Si l'utilisateur appuie sur la flèche de retour située dans le coin supérieur gauche de l'écran, les filtres peuvent être modifiés.

![.filtres de recherche](../../../en/img/content_search1.JPG) ![.résultats de recherche](../../../en/img/content_search2.JPG)

La conception d'un élément de résultat correspond à une vignette de l'élément, et à son nom.

![.élément de résultat de la recherche](../../../en/img/content_search_default_item.JPG)

### Extension `.filtres`

L'extension `.filtres` fournit une interface de recherche dynamique. Chaque fois que l'utilisateur modifie un filtre, les résultats affichés sur le côté droit de la vue sont automatiquement mis à jour pour correspondre à la sélection actuelle.

![extension .filtre](../../../en/img/content_filters.JPG)

La conception d'un élément de résultat correspond à une vignette de l'élément, et à son nom.

### Extension`.appartements` 

L'extension ' .appartements ' utilise la même interface que l'extension ' .recherche '. La seule différence est l'apparence du résultat.

![résultats min .appartements](../../../en/img/content_appartments.JPG)

La conception d'un élément de résultat indique diverses informations sur l'élément : surface, orientation, type, sol, etc...

![min élément . appartements](../../../en/img/contenu_appartements_item_min.JPG) ![plein élément .appartements](../../../en/img/contenu_appartements_item_full.JPG)

## Créer une interface de recherche

1. Dans votre environnement, créez un dossier nommé '">Nom de votre interface de recherche>. recherche" ou '>Nom de votre interface de recherche>. filtres' ou '>Nom de votre interface de recherche>. appartements' selon le type de vue que vous préférez (par exemple 'Recherche.recherche' ou 'Recherche.filtres').
1. Dans ce dossier, créez un fichier appelé `_list.csv` (ou `_catalog.csv`). 
1. Remplissez la feuille de calcul avec les critères que vous voulez, et décrivez votre article.
1. Pour chaque élément qui appartient à la colonne `id` de votre `_list.csv` (ou `_catalog.csv`), ajoutez un élément dans votre dossier de recherche (image, pdf, ect...)

## Métadonnées disponibles

Les métadonnées vous aideront à personnaliser le comportement de votre interface de recherche.

| Clé de métadonnées        | Type    | Par défaut | Description |

| `catalog.resultsMaxCount` |`nombre` | 40         | Le nombre maximum de résultats qui peuvent être visualisés dans la page de résultats. |


## Télécharger un exemple

Un univers de démonstration qui contient des exemples d'interfaces de recherche est disponible, [essayez-le](../Demo-Universe.zip) &#x1f604 ;


Suivant : [Fiche produit](fiche produit.md)

[Retour au contenu pris en charge](index.md)
