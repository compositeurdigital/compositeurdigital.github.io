# Collection de biens immobiliers

Utiliser ce type de contenu pour proposer une recherche par critères dans une collection de biens immobilier (appartements, etc.)

## Utilisation

Vous pouvez :

- Sélectionner vos critères de recherche : surface, prix, nombre de pièces, etc.
- Lancer une recherche
- Ouvrir un résultat de recherche (ex : plan d'appartement)

![Aperçu du module de recherche](img/immo_preview.jpg)

## Administration

- Extension de dossier : `apartments`
- Extension de fichier dans le dossier : `csv` 

Le dossier contient :
- L'ensemble des contenus correspondant aux biens immobilier (généralement les plans). Si besoin, ils peuvent être organisés dans des sous-dossiers.
- Un tableau contenant la liste des biens immobilier et leurs caractéristiques. Le document est au format CSV (avec séparateur `;`) : vous pouvez utiliser un tableur comme Microsoft Excel pour l'éditer.

Voici le tableau qui permet d'obtenir l'aperçu précédent :

![Aperçu du fichier _questions.csv](img/immo_csv.jpg)

### Format du tableau :

- 1ère ligne : type de la colonne
- 2ème ligne : nom de la colonne
- lignes suivantes : biens immobiliers

### Types de colonnes

- `id` : nom du fichier associé au bien immobilier (sans l'extension). Une colonne unique de ce type est obligatoire.
- `floor` : niveau (étage).
- `type` : typologie (T1, T2, etc.)
- `surface` : surface du bien ou d'une partie spécifique du bien (balcon, parking, etc.). Valeur en m², sans unité dans la cellule.
- `price` : prix du bien immobilier. Plusieurs colonnes de ce type peuvent être présentes (TVA différente, libre/aidé, etc.).
- `multiple` : autre critère de filtre avec possibilité de sélectionner plusieurs valeurs à la fois.
- `single` : autre critère de filtre, une seule valeur sélectionnée à la fois.


[Revenir au différents Types de contenus](content_types.md)