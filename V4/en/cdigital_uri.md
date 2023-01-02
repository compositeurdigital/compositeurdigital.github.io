# cdigital:// protocol

## launch
The cdigital:// protocol allows to launch the application and open a specific environment or event trigger specific actions in a given environment. These actions can be triggered from a webpage or an NFC tag event:
- `cdigital://launch` : Opens the Compositeur Digital application from a web browser
- `cdigital://launch?rootItem=Ma%20Banque` : Opens the "Ma Banque" environment in the Compositeur Digital 
- `cdigital://launch?firstName=Jean&lastName=Dupont` : positions context data [données de contexte](config.md#valueKeys) in the current environment.
- `cdigital://launch?action=showmenu_recents` : opens the environment's recent documents. Other possible values are :
	- showmenu_home,
	- showmenu_search,
	- showmenu_recents,
	- showmenu_mostused,
	- showmenu_papers,
	- showmenu_profile,
	- showmenu_basket,
	- showmenu_about
	
## goback
Set `cdigital://goback` as a hypertext link in an interactive Powerpoint to leave the current universe and come back to the universe selection page. Optionally add the `ignoreSave` parameter to avoid the dialog message asking to save your project: `cdigital://goback?ignoreSave=true`.

## exit
Set `cdigital://exit` as a hypertext link in an interactive Powerpoint instantly leave Compositeur Digital.
