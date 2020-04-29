# Audio

## Résumé
* [Description](#description)
* [Extensions di fichier](#extensions-de-fichiers)
* [Actions au sein du Compositeur Digital UX](#actions-au-sein-du-compositeur-digital-ux)
* [Metadata available](#metadata-available)

## Description

Les fichiers audio sont pris en charge en natif par le Compositeur Digital UX.

[Fichier audio affiché dans le Compositeur Digital UX](../../../en/img/content_audio.JPG)

## Extensions de fichiers 

Le Compositeur Digital UX prend en charge les fichiers `.mp3`.

## Actions dans le Compositeur Digital UX

Le lecteur audio prend en charge l'action suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**


| Annoter  | Capturer | Dupliquer | Boucle   | Ouvrir dans l'app | Enregistrer sous | Sélection | Partager | 
|:--------:|:--------:|:---------:|:--------:|:-----------------:|:----------------:|:---------:|:--------:|
| &#x2716; | &#x2716; | &#x2714;  | &#x2714; | &#x2714;          | &#x2714; | &#x2714;  | &#x2714; | 

**Interaction avec l'élément**

| Contrôles de l'audio |
|:--------------:|
| &#x2714;       | 


## Métadonnées disponibles

| Clé de métadonnées                | Type      | Par défaut | Description |
|:--------------------------------- |:----------|:--------|:-|
| `video.autoplay`                  | `booléen` | vrai    | lancer la lecture de la vidéo à l'écran |
| `video.autoplay.delay`            | `nombre ` | 0       | retarder la lecture automatique du nombre de secondes spécifié |
| `video.autoclose`                 | `booléen` | faux    | fermer la vidéo lorsque la lecture est terminée |
| `video.autoclose.delay`           | `nombre ` | 0       | retarder la fermeture automatique du nombre de secondes spécifié |
| `video.rewind`                    | `booléen` | faux    | revenir à la première image lorsque la vidéo se termine |
| `video.loop`                      | `booléen` | faux    | reprise au début à la fin de la vidéo |
| `video.mute`                      | `booléen` | faux    | forcer la vidéo à être muette |
| `video.controls.alwaysvisible`    | `booléen` | faux    | forcer l'affichage des commandes de lecture vidéo |

Suivant: [Livre d'or (format du Compositeur Digital UX)](guestbook.md)

[Retrour à Contenu pris en charge](index.md)
