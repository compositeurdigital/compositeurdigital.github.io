# Plan interactif

Utilisez ce type de contenu pour afficher un plan ou un visuel avec des points d'intérêts, ces derniers pointant sur d'autres contenus. Exemple : ouvrir un plan d'appartement depuis un point d'intérêt sur un plan d'étage.

## Utilisation

Vous pouvez :

- Afficher / masquer un calque
- Ouvrir un contenu à partir d'une pastille (point d'intérêt)


## Administration

- Extension de dossier : `map`
- Extension de fichier dans le dossier : `jpg`, `png`
- Extension de sous-dossier : `layer`

### Calques

Un plan interactif est constitué d'un dossier qui contient des calques : chaque calque constitue une couche d'information (un ensemble de points d'intérêt ou une image) qui peut être affichée ou masquée dans le Compositeur Digital :

- Le premier calque est constitué d'un fichier image (fond de carte), il est toujours affiché et ne peut être masqué.
- Les autres calques peuvent être un fichier image (généralement avec transparence pour obtenir un effet de superposition) ou un dossier de points d'intérêt (layer).

Exemple d'arborescence :

![explorer sequence](img/explorer_map_l1.jpg)

### Points d'intérêt

Un point d'intérêt est constitué d'un pictogramme à un emplacement précis sur le fond de carte. Un point d'intérêt déclenche l'ouverture d'un contenu.
Pour créer un point d'intérêt :

- Créez un sous-dossier calque (extension layer) qui contiendra un ou plusieurs points d'intérêt.
- Ajoutez le contenu que vous souhaitez associer au point d'intérêt dans le sous-dossier (une image, un diaporama, etc.)
- Utilisez l'outil [Compositeur Digital Editor](editor.md) pour positionner visuellement le point d'intérêt sur le fond de carte.

Exemple d'arborescence :

![explorer sequence](img/explorer_map_l2.jpg)

[Revenir au différents Types de contenus](content_types.md)