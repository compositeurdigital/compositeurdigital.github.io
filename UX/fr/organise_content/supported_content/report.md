# Rapport

## Résumé
* [Description](#description)
* [Actions au sein du Compositeur Digital UX] (#actions-au-sein-du-compositeur-digital-ux)
* [Extension de contenu](#extension-de-contenu)
* [Créer un rapport](#créer-un-rapport)
* [Étiquettes spéciales](#étiquettes-spéciales)
* [Téléchargez un exemple](#télécharger-un-exemple)

## Description

Les rapports sont utilisés pour résumer toutes les informations recueillies par le biais des [formulaires](form.md) et des [quiz](quiz.md). 

! [Rapport](../../../en/img/content_report_ui.JPG)

## Actions au sein du Compositeur Digital UX

Les rapports prennent en charge les actions suivantes. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter   | Capturer  | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager | Diapositives |

| &#x2714 ; | &#x2714 ; | &#x2714 ; | &#x2714 ;                | &#x2714 ;        | &#x2714 ; | &#x2714 ; | &#x2714 ; | 

**Interaction avec l'article**

| Mode capture | Hyperliens | Zones actives | Suivant   | Précédent | 

| &#x2714 ;    | &#x2714 ;  | &#x2714 ;     | &#x2714 ; | &#x2714 ; |

## Extension du contenu

Un rapport est placé dans un dossier appelé '<nom de votre rapport>.rapport'. Dans ce dossier, il y a un fichier nommé `Template.pptx`. Ce fichier contient le modèle de votre rapport.

## Créer un rapport

Créez un dossier qui se termine par '.report '. Dans ce dossier, créez un fichier nommé 'Template.pptx'. Ce fichier contient des champs de texte individuels qui commencent par "@@ ". 

[Report pptx](../../../en/img/content_report_template.JPG)

Le texte qui suit le double '@@ ' indique le nom d'une clé. Cette clé doit exister dans un formulaire [form](form.md) ou un quiz [quiz](quiz.md).

[rapport et formulaires](../../../en/img/content_report_forms.JPG)

Enfin, lorsque les [formulaires](form.md) sont édités via le Compositeur Digital UX, le rapport est mis à jour avec les informations fournies.

! [Rapport en ui](../../../en/img/content_report_ui.JPG)

## Étiquettes spéciales

| Nom de l'étiquette | Description |
|:---------------------------:|:------------|
| @@@creationdate | Remplie automatiquement avec la date du jour. |

## Télécharger un exemple

Un univers de démonstration contenant un rapport est disponible, [essayez-le](../Demo-Universe.zip) &#x1f604 ;

Suivant : [Raccourcis & hyperliens : cdurl](cdurl.md)

[Retour au contenu pris en charge](index.md)
