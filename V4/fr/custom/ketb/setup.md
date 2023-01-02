# Kaufman & Broad : procédure de déploiement du Compositeur Digital

*Cette procédure est valable pour la phase de production à partir de S2 2017*

## Prérequis matériel et réseau
- Ordinateur / tablette tactile, Intel Core i5 ou supérieur, SSD 128 Go minimum.
- Windows 10 (Anniversary update ou supérieur).
- Connexion internet, lors de l'installation, mais aussi lors de l'utilisation pour la mise à jour des contenus.

## Prérequis mode "kiosque"
- Verouillage de l'environnement shell Windows (exemple de logiciel : Frontface Lockdown).
- Logiciel de type watchdog pour surveiller et relancer le Compositeur Digital en cas d'arrêt non prévu (exemple de logiciel : restartoncrash).
- Arrêt/démarrage automatique matin et soir (*heures à déterminer avec K&B*).
- Pas de mise en veille en journée (l'économiseur d'écran est intégré au Compositeur Digital).

## Installation
### 1. Configurer OneDrive
Se rendre sur la page de la [bibliothèque Sharepoint](https://insideso.sharepoint.com/sites/KetB/Documents%20partages/Forms/AllItems.aspx) et utiliser le compte. ketb@compositeurdigital.com (mot de passe fourni par votre contact excense). Cliquer `Synchronisation` et conserver la configuration par défaut proposée par l'assistant.

Si la version de OneDrive est récente, la fonctionnalité "Fichiers à la demande" est activée par défaut. Se rendre dans les paramètres et décocher la case intitulée `Libérez de l'espace et téléchargez les fichiers quand vous avez besoin de les utiliser`.

**_Remarque : la synchronisation initiale provoque le téléchargement de plusieurs dizaines de Go de données : elle ne doit pas être faite sur site K&B. Seules les mises à jour différentielles sont faites sur site K&B.**

### 2. Installer Compositeur Digital
En ligne à partir de l'adresse [http://www.compositeurdigital.com/deploy/ketb](http://www.compositeurdigital.com/deploy/ketb).

### 3. Configurer démarrage/watchdog
Démarrage automatique du Compositeur Digital et/ou du watchdog à l'ouverture quotidienne de session du PC.

**_Remarque 1 : il est important que le Compositeur Digital démarre 1 fois par jour._**

**_Remarque 2 : le chemin vers l'exécutable principal peut changer lors d'une mise à jour._**

- Processus à surveiller : Compositeur Digital KetB.exe
- Démarrage : utiliser le lien généré lors de l'installation (raccourci dynamique) situé à l'adresse ci-dessous :

"%appdata%\Microsoft\Windows\Start Menu\Programs\EXCENSE\Compositeur Digital\Compositeur Digital KetB.appref-ms"

Utiliser au besoin .bat si le watchdog ne peut démarrer un fichier de type .appref-ms. (nécessaire pour restartoncrash).

## Exploitation
### Arrêt
ALT+F4 ou à travers le gestionnaire des tâches.

### Mise à jour manuelle
Procédure identique à l'installation.

### Correction des erreurs de synchronisation OneDrive

L'erreur suivante peut parfois survenir :

![Erreur OneDrive](img/onedrive_sync_error.jpg)

Pour corriger ces erreurs il faut réinitialiser OneDrive en suivant les étapes suivantes :

1. Dans l'onglet `Compte` des paramètres OneDrive, cliquer sur `arrêter la synchronisation`.
2. **Attendre quelques minutes** la fin de la désynchronisation. Une invite de connexion OneDrive s'affiche à l'issue de la désynchronisation ; fermer la fenêtre.
3. Supprimer les contenus synchronisés (répertoire `C:\Users\\[USER]\Excense\Kaufman & Broad - Documents` par défaut)
4. Refaire la configuration OneDrive comme indiqué dans la section 'Installation'.


### Version
Sur la page d'accueil en bas à droite.

### Répertoire d'installation
Modèle du chemin vers le répertoire, celui-ci peut varier d'une installation à l'autre et lors d'une mise à jour :

C:\Users\\[USER]\AppData\Local\Apps\2.0\\[F1]\\[F2]\comp..tion_[ID]

### Traces
%appdata%\Compositeur Digital\log app




