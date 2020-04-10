# Raccourcis, hyperliens : CDURL

## Résumé
* [Description](#description)
* [Extension de contenu](#extension-de-contenu)
* [Créer un cdurl](#créer-un-cdurl)
* [Téléchargez un échantillon](#télécharger-un-échantillon)

## Description

Ce contenu vous permet de créer des liens vers des documents à l'intérieur de vos univers. Imaginez que vous ayez une image ou un document que vous souhaitez voir dans deux dossiers différents. En utilisant un fichier "cdurl", vous pouvez créer un lien hypertexte vers le fichier qui se trouvera à l'intérieur d'un dossier différent.

L'utilisation du fichier `.cdurl` vous permet de gérer la quantité de mémoire et d'espace disque consommée par votre univers. 

## Extension du contexte

Pour créer un raccourci vers un document, ajoutez l'extension " .cdurl " à la fin d'un fichier texte.

## Créer un cdurl

1. Dans votre dossier univers, créez un fichier nommé `<Nom de votre fichier>.cdurl` (par exemple `Fichier raccourci.cdurl`).
1. Ouvrez le fichier et ajoutez la ligne suivante pour indiquer le chemin d'accès au fichier existant : <br/>
`url = <chemin relatif vers le document>`

Le 'chemin' doit être [relatif] (https://docs.microsoft.com/en-US/dotnet/standard/io/file-path-formats).  

## Télécharger un exemple

Un univers de démonstration qui contient un exemple pour le livre d'or est disponible, [Essayez !](../Demo-Universe.zip) &#x1f604 ;

Suivant : [Création de modèles](templates.md)

[Retour au contenu pris en charge].



