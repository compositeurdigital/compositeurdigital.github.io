# Notes de publication


### 4.1.5507 - 8 juillet 2024

- [FIX] L'application ne se lance pas pour les nouvelles installations à partir du lien "en ligne" 

### 4.1.5501 - 5 juillet 2024

#### Nouvelles fonctionnalités

- Nouvelle expérience de partage, le souvenir en ligne est unifié avec le partage de fichier et peut être partagé par Outlook ou Thunderbird
- Nouvel outil de capture : capturer une sélection ou toute la vue du document
- Activation automatique du partage Outlook si l'application est installée et configurée (Office 15 ou 16)
- Nouvelle expérience d'import de pages web
- Editeur : nouvelle interface d'ajout de lien web 
- Nouveau connecteur de partage réseau, garde les documents synchronisés comme pour Teams/SharePoint

#### Améliorations et correctifs

- Utilisation des icônes de pages web en vignette
- Le partage Outlook MS365 n'est proposé que si l'utilisateur est connecté dans le Compositeur Digital
- Raccourci pour cacher la barre de documents en option : `bottombar.showQuickHideAction=true`
- Facteur de zoom réduit à la molette de souris
- Editeur : possibilité de définir des modèles supplémentaires à partir d'un emplacement réseau
- Editeur : paramétrage des actions d'ajout, suppression, déplacement, renommage par les metas `editor.disableAdd`,  `editor.disableMove`, `editor.disableRename`, `editor.disableDelete`
- Editeur : possibilité de rendre des éléments de modèles invisibles
- [FIX] Clic intempestif après avoir déplacé une vue HTML
- [FIX] Icône de fichiers mp3 invisible
- [FIX] Export de projet en erreur
- [FIX] Crash lors de l'utilisation des raccourcis claviers dans certaines conditions
- [FIX] Taille d'écran de la visualisation d'univers incorrecte 
- [FIX] Crash de la Webview2 du designer d'application dynamiques
- [FIX] La diffusion Miracast ne démarre pas
- [FIX] Nom d'affichage Miracast de forme 'CDUX  machine' pour une meilleure identification
- [FIX] Le partage à proximité Windows n'aboutit pas
- [FIX] La création d'élément à partir d'un modèle est incomplète après un renommage ou déplacement
- [FIX] Zoom dans l'éditeur
- [FIX] Designer HTMLApp ne suit pas toujours la sélection
- [FIX] Panorama et objets 3D : des crashs peuvent survenir lorsque l'action de manipulation ne suit plus l'état réel
- [FIX] Crash lors de fermeture/mise au premier plan de documents


### 4.0.5387 - 27 mai 2024

- [FIX] Configuration avancée de l'apparence de la page d'accueil


### 4.0.5297 - 15 avril 2024

- [FIX] Le texte saisi dans des modèles PowerPoint est manquant si le document n'est pas affiché au moment du partage 

### 4.0.5263 - 2 avril 2024

- [FIX] Impossible d'importer certains liens web à partir du presse-papier
- [FIX] Erreur d'accès lors de l'édition de documents MS365 en ligne

### 4.0.5207 - 14 mars2024

- [FIX] Résultats de recherche manquants après changement de casse

### 4.0.5193 - 5 mars 2024

- Support des sélecteurs d'univers PowerPoint de plusieurs pages
- Bouton Lecture/Pause de vidéo toujours visible, sauf si explicitement désactivé avec `actions.playpause.disabled=1`
- [FIX] Erreur lors du rafraichissement automatique de l'univers par défaut en mode kiosque
- [FIX] Etat d'activation incorrect pour les installations multi-utilisateur avec données applicatives partagées
- [FIX] Sélecteur d'univers PowerPoint non mis à jour après modification du fichier
- [FIX] Le panneau de conception d'univers ne peut pas êre désactivé
- [FIX] Activités: la capture des résultats de votes pour un dessin ne correspond pas à l'affichage pendant le vote
- [FIX] L'éditeur n'affiche pas l'interface de configuration de fond d'écran au chargement d'un univers
- [FIX] Appel systématique au service d'activation par les installations enregistrées sans abonnement
- [FIX] Fermeture intempestive des éléments après un appui court
- [FIX] Le script d'installation ferme l'invite de commande après installation


### 4.0.5082 - 14 février 2024

#### Nouvelles fonctionnalités

- Nouvelle gestion des présentations PowerPoint, améliore le rendu de certains graphiques et polices de caractères
- Nouvelle interface graphique du menu de documents et des actions
- Recherche intégrée au menu de documents
- Nouvelle interface graphique de l'éditeur
- Nouveau mode d'interaction des vues web :
  - Possibilité d'interagir par simples appuis et au clavier sans entrer en mode interaction tactile
  - Possibilité de déplacer la vue web par une bordure en mode interaction tactile
- Nouvelles activités en ligne et interface graphique unifiée :
  - Plusieurs types de votes rapides (Oui/Non, Vrai/Faux, ❤️/💔, Note de 1 à 5)
  - Vote pour un croquis
  - Diffusion de documents à tous les participants
- Souvenir en ligne : tableau de suivi des souvenirs partagés sur la page d'accueil en option


#### Améliorations et correctifs

- Support des liens interactifs dans les PDF/PowerPoint importés
- Activités : nouvelle présentation du lien/QRCode avec action de partage
- Activités : ouverture automatique du lien/QRCode au démarrage 
- Partage avec MS365 Outlook : sélection d'un rendez-vous en cours ou proche comme sujet d'email
- Souvenir en ligne : nouvelle présentation du lien de souvenir
- Souvenir en ligne : enregistrement des destinataires lors d'un partage par mail
- Notes et pages blanches : détection des liens web dans le texte saisi ou collé
- Animation de déplacement lorsque `desiredposition` est défini
- Coins arrondis en proportion des dimensions du document avec le paramètre `cornerRadius` 
- [FIX] Vignettes non affichées au premier chargement d'un univers Teams/SharePoint
- [FIX] Les sous-dossiers sélectionnés ne sont pas rétablis au chargement/rafraichissement d'un projet
- [FIX] Souvenir en ligne : la composition de mail ne permet de saisir que 2 destinataires
- [FIX] Catalogue : Impossible d'effacer complètement une limite haute/basse d'un filtre de prix
- [FIX] Catalogue - filtre régions : sélection incorrecte lorsque des régions ne contiennent pas de résultats
- [FIX] Editeur : impossible de supprimer un répertoire sur un lecteur réseau
- [FIX] Editeur : impossible de faire défiler certains éléments des applis web intégrées



### 3.7.4525 - 10 octobre 2023

- [FIX] Certains documents PDF partagés sans annotations deviennent illisibles


### 3.7.4373 - 19 septembre 2023

- [FIX] Partage avec Outlook bloqué sur une page blanche

### 3.7.4149 - 13 juin 2023

- Les annotations et notes des documents de l'univers ou importés sont conservés à l'enregistrement d'un projet
- [FIX] Crash sur certains affichages mis à l'échelle de 175% 
- [FIX] Vignettes de documents et univers non centrés
- [FIX] Les documents sont affichés flous pendant la durée de l'animation d'apparition
- [FIX] Pièces jointes du partage MS 365 Outlook


### 3.7.3987 - 13 avril 2023

- [FIX] Erreur lors du partage de souvenir en langue française 
- [FIX] Partage Outlook MS365 non interactive
- [FIX] Orientation interne aux pages PDF perdue lors de l'export si le document est annoté
- [FIX] Activité transfert de fichier refuse les fichiers
- [FIX] Couleur de fond vidéo non appliquée

### 3.7.3879 - 24 mars 2023

- [FIX] Menu de document toujours visible avec le paramètre `nochromebuttons=true`

### 3.7.3800 - 13 mars 2023

- [FIX] Capture de fenêtre et photo inactifs dans le menu importer 
- [FIX] Documents ajoutés manquants lors d'une actualisation de l'univers


### 3.7.3779 - 7 mars 2023

#### Nouvelles fonctionnalités

- Amélioration du temps de démarrage de l'application et du temps de chargement des univers
- Webview2 utilisée par défaut si le runtime est présent
- Webview : nouvelle appel disponible `getSessionSettings()` pour intérroger la position du présentateur
- Partage par Microsoft 365 Outlook avec fenêtre de composition intégrée à l'expérience de partage
- Partage par Microsoft 365 Outlook disponible pour le partage des souvenirs en ligne
- Partage par l'application Outlook dans la version disponible sur le Microsoft Store
- Activités : Nouveau service (serverless) excen.se
- Activités : Nouvelle activité de vote 
- Sélecteur d'univers : support des PowerPoint interactifs pour la sélection d'univers 
- Éditeur : Sélection des vignettes de documents par un menu, et support du copier-coller
- Éditeur : Édition des paramètres communs
- Éditeur : Powerpoint/PDF : Visualisation des zones interactives
- Éditeur : Vidéos : paramétrages de la lecture (en boucle, automatique, sourdine)
- Éditeur : Barre de navigation avec le chemin courant et actions précédent/suivant/parent 
- Éditeur : Ajout de documents par glisser-déposer 
- Éditeur : Zoom sur le document sélectionné 

#### Améliorations et correctifs

- Souvenir en ligne : gestion des gros volumes de documents partagés
- Interface de sélection de la position du présentateur revue 
- Powerpoint et PDF : amélioration des performance de chargement et de l'affichage
- Fiches produit : style des icônes similaire aux dossiers
- Chargement des fichiers de données .csv autres qu'encodés en UTF8
- Support des écrans Samsung Flip version 4
- [FIX] PDF : Ouverture de documents en erreur pour les liens fichier absolus 
- [FIX] Manipulations bloquées sur certains dispositifs tactiles avec reconaissance du stylet
- [FIX] Vidéos : bouton lecture/pause visible malgré le paramètrage `video.controls.hide=true`
- [FIX] Souvenir : fichiers comptés en double dans l'interface
- [FIX] L'action `ouvrir` génère un PDF pour des images
- [FIX] Interface spécialisée de la page d'accueil non appliquée lors du changement de source
- [FIX] Webview: Manipulation bloquées
- [FIX] Le chargement des projets externes ne se fait pas si leur nom comporte certains caractères spéciaux
- [FIX] Crash peu après l'ouverture de certains univers contenant des panoramas 
- [FIX] Panoramas : le rendu des vignettes peut provoque le blocage et l'export de tous les documents
- [FIX] Catalogue : erreur lorsque la zone de saisie textuelle reste ouverte
- [FIX] Catalogue : Manipulation tactile impossible à partir 
- [FIX] Les vidéos en fond d'écran ne sont pas jouées en boucle
- [FIX] Menu document: indicateur de sélection tronqué



### 3.6.3619 - 2 février 2023

- [FIX] Consommation mémoire excessive pour les univers contenants de nombreux documents PowerPoint

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
