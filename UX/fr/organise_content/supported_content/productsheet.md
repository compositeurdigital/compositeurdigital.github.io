# Fiche produit

## Résumé
* [Description](#description)
* [Actions dans Compositeur Digital UX](#actions-dans-compositeur-digital-ux)
* [Extension de dossier](#extension-de-dossier)
* [Créer une fiche produit](#créer-une-fiche-produit)
* [Télécharger un exemple](#télécharger-un-exemple)

## Description

Une fiche produit vous permet de visualiser les informations relatives à un article. Elle est généralement utilisée en combinaison avec une [interface de recherche](search.md). À partir d'une fiche produit, vous pouvez lier des documents ou un dossier. 

! [Fiche produit](../../../en/img/contenu_fiche_produit.JPG)

## Actions dans Compositeur Digital UX

Les éléments de la fiche-produit prennent en charge les actions suivantes. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Capturer | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |
|:--------:|:---------:|:------------------------:|:----------------:|:---------:|:--------:|
| &#x2716; | &#x2714;  | &#x2714;                 | &#x2714;         | &#x2714;  | &#x2714; |

**Interaction avec le contenu**

| Ouvrir un document |
|:------------------:|
| &#x2714;           | 

## Extension de dossier

Pour utiliser une fiche produit, ajoutez l'extension `.productsheet` à la fin du nom de votre dossier.

## Créer une fiche produit

1. Dans votre dossier univers, créez un dossier nommé `<Nom de votre fiche produit>.productsheet` (par exemple `304.productsheet`).
1. Mettez tous les documents que vous voulez lier à cette fiche produit dans votre dossier. 
1. Pour ajouter des informations qui seront affichées dans la fiche produit, créez un fichier `_meta.txt`. Remplissez ce fichier avec deux lignes par information. Il doit être :<br/>
`key.label = <L'étiquette à afficher>` <br/>
`key.value = <la valeur associée à cette étiquette>`

![Fiche produit meta](../../../en/img/content_product_sheet_meta.JPG)

## Télécharger un exemple

Un univers de démonstration contenant diverses fiches produits est disponible, [essayez-le!](../../../en/organise_content/Demo-Universe.zip) &#x1f604;

Suivant : [Séquence - vue orbitale (format Compositeur Digital UX)](sequences.md)

[Retour aux Contenus pris en charge](index.md)
