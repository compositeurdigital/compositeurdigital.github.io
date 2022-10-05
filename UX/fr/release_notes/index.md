# Notes de publication

### 3.6.3226 - 5 octobre 2022

#### Nouvelles fonctionnalités

- Nouvelle interface harmonisée avec Windows 11 : bords des documents arrondis et nouvelle apparence des dossiers
- Mode Studio TV et autres 'packs' de fonctionalités
- Support des flux vidéos des webcams et périphériques de captures
- Souvenir en ligne: option pour générer un lien à partager plutôt qu' mail envoyé par la plateforme
- Affichage sans fil Miracast (sous Windows 11)
- Webview2 en déploiement progressif

#### General improvements and fixes
 
- New `noHistory=true` parameter to prevent documents from appearing in the recycle bin
- Surface pen button support: press to advance to the next slide, long press to return to previous 
- Powerpoint backgrounds now export in Web memory & Companion apps
- Slideshow: Create multiple version of a document with parameter `?newInstance=true` in hypertext links
- Webview: new apis  ([see documentation](../organise_content/supported_content/web_page.html)))
- Videos: Timestamp & playlist hints

- [FIX] Web memory: display aspect ratio lost on 
- [FIX] Video thumbnails missing in some cases
- [FIX] sticked/taped documents restored at the wrong size when opening a project- [FIX] Video loop state lost after project reload
- [FIX] Fallback to closest aspect ratio background when no exact match
- [FIX] Source settings not applied when swithcing sources
- [FIX] empty universe projects thumbnail show trasparent background
- [FIX] Escape key does not gracefully exit the Share dialog
- [FIX] Menu appears at the top left after unpin
- [FIX] exception when loading video thumbnail in history
- [FIX] Activities appear centered, as opposed to templates/notes that appear on the side
- [FIX] File upload activity 'file type not supported' error


### 3.5.3069 - 31 août 2022

- [FIX] Webview2: crash à la fermeture d'un projet avec un fond HTML

### 3.5.3047 - 11 août 2022

- Nouveau paramètre `hideBottomBar` pour cacher complètement la barre de documents lorsque réduite
- [FIX] PowerBI: rapports non affichés

### 3.5.3016 - 8 août 2022

- WebView : `CDUX.FindItems()` fournit les chemins vers les vignettes et icônes du document
- WebView : ajout de `CUDX.ClearWorkspace()`

### 3.5.2965 - 25 juillet 2022

- [FIX] Paramètres de compte non appliqués au démarrage de l'application

### 3.5.2928 - 5 juillet 2022

- Webview2: lien pour télécharger et installer Microsoft Webview2 Runtime si non trouvé
- [FIX] Les vidéos de veille ne sont pas lues en boucle
- [FIX] SharePoint: documents non mis à jour

### 3.3.2871 - 17 juin 2022
- [FIX] Paramètre d'univers `themeColor` non pris en compte

### 3.3.2856 - 10 juin 2022

- Nouveau paramètre `desiredPosition` ([voir documentation](../organise_content/advanced_setting.html##métadonnées-prises-en-charge)))
- [FIX] Video : bouton play/pause toujours visible même si désactivés par le paramètre `video.controls.hide`
- [FIX] Powerpoint : problèmes de rendu
- [FIX] SharePoint: documents non mis à jour lors d'une actualisation
- [FIX] Les liens PowerPoint vers des documents en dehors de l'univers déclenchent un import


### 3.3.2813 - 16 mai 2022

- Video : add .video folder extension to play a list of videos in sequence
- Video : rework video controls. Play/Pause action will always be available at the bottom right corner of the video. Full control can be shown on tap.
- 3D objects : handle shadows and ground textures.
- 3D objects : rework object orientation (.obj) for better positionning
- Product sheet : add `disableExport` to prevent an area from being exported
- PowerPoint : improve rendering of images
- Start Page : handles Category names and previews
- Slideshow : PowerPoint ratio extension is not ignored when the file is defined as the background.
- [FIX] Web view crashes when used a background.
- [FIX] Importing a URL won't load the web page


### 3.2.2769 - 5 mai 2022
	
- Support de la migration des projets enregistrés localement lorsqu'un univers change d'emplacement


### 3.2.2622 - 21 mars 2022
		
- PowerPoint : amélioration du rendu des images découpées
- Fiche produit : export des documents associés après une page de garde lors d'un partage
- Catalogue : filtre numérique permettant la définition d'une valeur minimum ou maximum uniquement
- Catalogue : invite sur les champs texte
- Catalogue : rappel de la sélection pour les filtres groupés
- PDF/PowerPoint : ajustements de l'orientation sauvegardés pour l'utilisateur
- SharePoint : amélioration de la stabilité et du délai de synchronisation
- Activité présentation de document plus simple à démarrer
- Pages web locales exportables en PDF
- [FIX] Dynamics CRM : impossible de partager la sélection


### 3.2.2469 - 21 février 2022

- Catalogue : saisie manuelle des valeurs numériques minimum et maximum	
- Catalogue : tri par valeurs "Oui/Non", "Yes/No", ...
- Support des fonctionnalités et packs de fonctionnalités activés par licence	
- Souvenir en ligne : export des pages web sous forme de PDF avec un lien	
- [FIX] Blocage aléatoire du chargement des pages des PDF ou PowerPoint après actualisation d'un univers
- [FIX] Stickers partagés même si non collés	
- [FIX] Stickers affichés en noir	
- [FIX] Impossible de charge un panorama indexé	
- [FIX] Séquences : polygones interactifs non visibles
- [FIX] Stickers : la définition d'une taille relative (ex 5%) empêche le fonctionnement de la meta `isSticker`
- [FIX] Powerpoint : liens "signet" non reconnus pour les fichiers gérés par MS365
- [FIX] Catalogue : texte tronqué dans certains filtres numériques
- [FIX] OneDrive/SharePoint avec cache usb : metadonnées manquantes à partir de la 2ème session 
- [FIX] Slideshow : les zones interactives ne suivent pas la rotation

### 3.2.2371 - 28 décembre 2021

- [FIX] Demande d'autorisation d'accèes aux informations utilisateur systématique sur les dispositifs partagés tels que les Surface Hub
- [FIX] Catalogue: crash lors de l'utilisation du format d'affichage des résultats `round`

### 3.2.2307 - 6 décembre 2021

#### Nouveautés
- Souvenir en ligne : enregistrez un aperçu de votre session en ligne et partagez un lien personalisé vers une page web contenant vos documents et notes

- Catalogue : nouvelle interface pour une meilleure lisibilité
- Catalogue avec cartographie : manipulation tactile directe sur la vue carte des résultats de recherche

#### Améliorations générales et correctifs
- Présentations & images: nouvelle action du menu pour pivoter le docuemnt
- Presentations : possibilité de spécifier l'emplacement des boutons de navigation page précédente/suivante avec `slideshow.controls.position` ([voir la documentation](../organise_content/advanced_setting.html#slideshow))
- Vignettes :  possibilité de définir une taille plus petite avec le paramètre `desiredWidth`, valeur suggérée `desiredWidth=40`
- Web : nouveau paramètre `action.manipulation.location` pour de repositionner l'invite de manipulation
- Sharepoint & OneDrive: nouveaux connecteurs avec comparaison différentielle pour des synchronisation plus rapides
- Paramètres : informations détaillées sur l'application
- Amélioration générale des performances
- [FIX] Modèles : les modèles personnalisés de s'affichent pas si les modèles par défaut sont désactivés
- [FIX] Panorama : les panoramas sphériques s'affichent avec une mauvaise orientation
- [FIX] PowerPoint : les liens définis dans des SmartArt ne sont pas reconnus
- [FIX] "Ouvrir avec Compositeur Digital UX" à partir de l'explorateur de fichier ne fonctionne pas
- [FIX] Chronomètre : L'indicateur de progression ne reflète pas le temps écoulé/restant


[Retour à la documentation](../index.md)
