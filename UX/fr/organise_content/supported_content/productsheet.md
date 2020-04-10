# Fiche produit

## Résumé
* [Description](#description)
* [Actions au sein du Compositeur Digital UX] (#actions-au-sein-du-compositeur-digital-ux)
* [Métadonnées disponibles](#métadonnées-disponibles)

## Description

Une fiche produit vous permet de visualiser les informations relatives à un article. Elle est généralement utilisée en combinaison avec une [interface de recherche] (search.md). À partir d'une fiche produit, vous pouvez lier des documents ou un dossier. 

! [Fiche produit](../../../en/img/contenu_fiche_produit.JPG)

## Actions au sein du Compositeur Digital UX

Les éléments de la fiche-projet prennent en charge l'action suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter | Capturer | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |


| &#x2716 ; | &#x2716 ; | &#x2714 ; | &#x2714 ; | &#x2714 ; | &#x2714 ; | &#x2714 ; |

**Interaction avec l'article**

| Lancez les articles |
|:------------:|
| &#x2714 ; | 

## Extension du contexte

Pour utiliser une fiche produit, ajoutez l'extension '.productsheet' à la fin du nom de votre dossier.

## Créer une fiche produit

1. Dans votre dossier univers, créez un dossier nommé `<Nom de votre fiche produit>.fiche produit` (par exemple `304.fiche produit`).
1. Mettez tous les documents que vous voulez lier à cette fiche produit dans votre dossier. 
1. Pour ajouter des informations qui seront affichées dans la fiche produit, créez un fichier `_meta.txt`. Remplissez ce fichier avec deux lignes par information. Il doit être :<br/>
`key.label = <L'étiquette à afficher>` <br/>
`key.value = < la valeur associée à cette étiquette>`

! [Fiche produit meta](../../../en/img/content_product_sheet_meta.JPG)

## Télécharger un exemple

Un univers de démonstration contenant diverses fiches produits est disponible, [essayez-le](../Demo-Universe.zip) &#x1f604 ;

Suivant : {Séquences : Vue 360° pré-rendue (orbital, format Compositeur Digital UX)](sequences.md)

[Retour au contenu pris en charge](index.md)