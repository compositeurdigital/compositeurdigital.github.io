# Rapport

## Résumé
* [Description](#description)
* [Actions dans Compositeur Digital UX](#actions-dans-compositeur-digital-ux)
* [Extension de dossier](#extension-de-dossier)
* [Créer un rapport](#créer-un-rapport)
* [Clés spéciales](#clés-spéciales)
* [Téléchargez un exemple](#télécharger-un-exemple)

## Description

Les rapports sont utilisés pour résumer toutes les informations recueillies par le biais des [formulaires](form.md) et des [quiz](quiz.md). 

![Rapport](../../../en/img/content_report_ui.JPG)

## Actions dans Compositeur Digital UX

Les rapports prennent en charge les actions suivantes. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Capturer  | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager | Diapositives |
|:---------:|:---------:|:------------------------:|:----------------:|:---------:|:--------:|:------------:|
| &#x2714;  | &#x2714;  | &#x2714;                 | &#x2714;         | &#x2714;  | &#x2714; | &#x2714;     | 

**Interaction avec le contenu**

| Annotation | Mode capture | Hyperliens | Zones actives | Suivant   | Précédent | 
|:----------:|:------------:|:----------:|:-------------:|:---------:|:---------:|
| &#x2714;   | &#x2714;     | &#x2714;   | &#x2714;      | &#x2714;  | &#x2714;  |

## Extension de dossier

Un rapport est placé dans un dossier appelé `<nom de votre rapport>.report`. Dans ce dossier, il y a un fichier nommé `Template.pptx`. Ce fichier contient le modèle de votre rapport.

## Créer un rapport

Créez un dossier qui se termine par `.report`. Dans ce dossier, créez un fichier nommé `Template.pptx`. Ce fichier contient des champs de texte individuels qui commencent par `@@`. 

![Report pptx](../../../en/img/content_report_template.JPG)

Le texte qui suit le double `@@` indique le nom d'une clé. Cette clé doit exister dans un formulaire [form](form.md) ou un quiz [quiz](quiz.md).

![rapport et formulaires](../../../en/img/content_report_forms.JPG)

Enfin, lorsque les [formulaires](form.md) sont édités via le Compositeur Digital UX, le rapport est mis à jour avec les informations fournies.

![Rapport](../../../en/img/content_report_ui.JPG)

## Clés spéciales

| Clé               | Description                                   |
|:-----------------:|:----------------------------------------------|
| `@@@creationdate` | Remplie automatiquement avec la date du jour. |

## Télécharger un exemple

Un univers de démonstration contenant un rapport est disponible, [essayez-le!](../../../en/organise_content/Demo-Universe.zip) &#x1f604;

Suivant : [Raccourcis & hyperliens : cdurl](cdurl.md)

[Retour aux Contenu pris en charge](index.md)
