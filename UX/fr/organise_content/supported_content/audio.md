# Audio

## Résumé
* [Description](#description)
* [Extensions de fichiers](#extensions-de-fichiers)
* [Actions dans Compositeur Digital UX](#actions-au-sein-du-compositeur-digital-ux)
* [Métadonnées disponibles](#métadonnées-disponibles)

## Description

Les fichiers audio sont pris en charge nativement par Compositeur Digital UX.

![Fichier audio lu dans Compositeur Digital UX](../../../en/img/content_audio.JPG)

## Extensions de fichiers 

Compositeur Digital UX prend en charge les fichiers `.mp3`.

## Actions dans Compositeur Digital UX

Le lecteur audio prend en charge les actions suivantes. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Capturer | Dupliquer | Lire en boucle | Ouvrir dans l'app | Enregistrer sous | Sélection | Partager | 
|:--------:|:---------:|:--------------:|:-----------------:|:----------------:|:---------:|:--------:|
| &#x2716; | &#x2716;  | &#x2714;       | &#x2714;          | &#x2714;         | &#x2714;  | &#x2714; |

**Interaction avec le contenu**

| Contrôle de l'audio |
|:-------------------:|
| &#x2714;            | 


## Métadonnées disponibles

| Clé de métadonnées                | Type      | Par défaut | Description                                                      |
|:--------------------------------- |:----------|:-----------|:-----------------------------------------------------------------|
| `video.autoplay`                  | `booléen` | vrai       | lire automatiquement le fichier audio à l'ouverture du contenu   |
| `video.autoplay.delay`            | `nombre ` | 0          | retarder la lecture automatique du nombre de secondes spécifié   |
| `video.autoclose`                 | `booléen` | faux       | fermer le player audio lorsque la lecture est terminée           |
| `video.autoclose.delay`           | `nombre ` | 0          | retarder la fermeture automatique du nombre de secondes spécifié |
| `video.rewind`                    | `booléen` | faux       | rembobiner lorsque la lecture du fichier audio est terminée      |
| `video.loop`                      | `booléen` | faux       | lire le fichier audio en boucle                                  |
| `video.controls.alwaysvisible`    | `booléen` | faux       | forcer l'affichage des commandes du player audio                 |

Suivant: [Livre d'or (format Compositeur Digital UX)](guestbook.md)

[Retrour aux Contenus pris en charge](index.md)
