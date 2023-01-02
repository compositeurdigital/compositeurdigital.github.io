# Protocole cdigital://
## Usages
Le protocole cdigital:// déclenche l'ouverture ou une action dans le Compositeur Digital depuis un lien web ou un tag NFC :
- `cdigital://launch` : démarrage du Compositeur Digital depuis un navigateur web
- `cdigital://launch?rootItem=Ma%20Banque` : démarre le Compositeur Digital dans la déclinaison Ma Banque
- `cdigital://launch?firstName=Jean&lastName=Dupont` : positionne des [données de contexte](config.md#valueKeys) dans la déclinaison courante.
- `cdigital://launch?action=showmenu_recents` : affiche le menu projet dans le panneau des documents récents. Valeurs possibles :
	- showmenu_home,
	- showmenu_search,
	- showmenu_recents,
	- showmenu_mostused,
	- showmenu_papers,
	- showmenu_profile,
	- showmenu_basket,
	- showmenu_about

[Revenir au menu](home.md)