# Vidéo

## Résumé
* [Description](#description)
* [Extensions de fichiers](#extensions-de-fichiers)
* [Actions au sein du Compositeur Digital UX] (#actions-au-sein-du-compositeur-digital-ux)
* [codecs A/V] (#av-codecs)
* [Vidéos 360°](#vidéos-360)
* [Métadonnées disponibles](#métadonnées-disponibles)

## Description

Les vidéos sont prises en charge nativement par le Compositeur Digital UX.

[Vidéo affichée dans le Compositeur Digital UX](../../../en/img/content_video.JPG)

## Extensions de fichiers 

Le Compositeur Digital UX prend en charge les fichiers '.avi', '.flv', '.m4v', '.mov', '.mp4', '.mpeg', '.mpg', '.ts' et '.wmv'.

## Actions au sein du Compositeur Digital UX

Les vidéos prennent en charge l'action suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter   |  Capturer | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager  | Boucle |

| &#x2716 ; | &#x2714 ; | &#x2714 ; | &#x2714 ;                | &#x2714 ;        | &#x2714 ; | &#x2714 ; | &#x2714 ; | 

**Interaction avec l'article**

| Commandes vidéo |
|:--------------:|
| &#x2714 ; | 

## Codecs A/V

Un format de fichier vidéo peut intégrer différentes normes de codage/décodage. Ces normes appelées "codecs" doivent être installées sur votre ordinateur. Le K-Lite Codec Pack comprend une grande variété de codecs. Veuillez noter que certains codecs peu courants peuvent ne pas être pris en charge par le Compositeur Digital UX.

Nous vous recommandons d'utiliser les formats WMV et MP4(H264) pour une utilisation sûre.

## Vidéos à 360°

Les vidéos à 360° peuvent être visionnées avec un contrôleur qui permet à l'utilisateur de changer la position de la caméra. Voir la [section Panorama] (panorama.md#vidéo-projection).

## Métadonnées disponibles

| Clé de métadonnées             | Type      | Par défaut | Description |

| `video.autoplay`               | `booléen` | vrai       | démarre la lecture de la vidéo sur l'écran |
| `video.autoplay.delay`         | `nombre ` | 0          | retarde la lecture automatique du nombre de secondes spécifié |
| `video.autoclose`              | `booléen` | faux       | ferme la vidéo lorsque la lecture arrive à son terme |
| `video.autoclose.delay`        | `nombre ` | 0          | retarde la fermeture automatique du nombre de secondes spécifié |
| `video.rewind`                 | `booléen` | faux       | revient à la première image lorsque la vidéo se termine |
| `video.loop`                   | `booléen` | faux       | reprend depuis le début quand la vidéo se termine |
| `video.mute`                   | `booléen` | faux       | force la vidéo à être muette |
| `video.controls.alwaysvisible` | `booléen` | faux       | force l'affichage des commandes de lecture vidéo en permanence |
| `video.controls.hide`          | `booléen` | faux       | cache les contrôles de lecture vidéo en permanence |

Suivant : [Audio (format du Compositeur Digital UX)](audio.md)

[Retour au contenu pris en charge](index.md)
