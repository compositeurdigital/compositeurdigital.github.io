# Formulaire

## Résumé
* [Description](#description)
* [Actions au sein du Compositeur Digital UX] (#actions-au-sein-du-Compositeur-Digital-ux)
* [Extension de contenu](#extension-de-contenu)
* [Contenus : `_questions.xml`](#contenus)
* [Organiser les éléments] (#organiser-les-éléments)
* [Types d'entrée](#types-d'entrée)
   * [Choix unique](#choix-unique)
   * [Choix multiple](#choix-multiple)
   * [texte sur une seule ligne](#texte-sur-une-seule-ligne)
   * [texte sur plusieurs lignes](#texte-sur-plusieurs-lignes)
   * [Curseur](#curseur)
   * [Numéro](#numéro)
   * [Liste déroulante](#liste-déroulante)
* [types de présentateurs] (# types-de-présentateurs)
   * [Documents](#documents)
* [Autres valeurs](#autres-valeurs)
* [Visibilité des éléments] (# visibilité-des-éléments)
* [Téléchargez un exemple](#télécharger-un-exemple)

## Description

Ce type de contenu vous permet d'afficher un formulaire interactif qui vous aidera à collecter des informations.

![formulaire](../../../en/img/content_form.jpg)

## Actions au sein du Compositeur Digital UX

Les formulaires prennent en charge l'action suivante. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter  | Capturer | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |
|:--------:|:--------:|:---------:|:------------------------:|:----------------:|:---------:|:--------:|
| &#x2716; | &#x2716; | &#x2714;  | &#x2716;                 | &#x2716;         | &#x2714;  | &#x2716; |

**Interaction avec l'élément**

| Lancez les éléments | Questions |
|:------------:|:---------:|
| &#x2714 ; | &#x2714 ; |


## Extension du contenu

Pour créer un formulaire, placez tous les éléments dont vous avez besoin dans un dossier, et ajoutez l'extension ".form" à la fin du nom de votre dossier.

À l'intérieur de votre dossier, fournissez un fichier appelé `_questions.xml`.

## <a name="contents"></a>Contents : `_questions.xml`

Un formulaire est composé de petits éléments pour présenter ou collecter des informations : 
* `<input>` pour collecter des informations
* `<présentater>` pour afficher les informations

Ils peuvent tous deux être décrits avec les attributs suivants :
* `type` : à quoi ressemblera l'élément (voir les sections [Types d'entrée](#input-types) et [Types de présentateur](#presenter-types))
* 'texte' : le titre ou la question affiché au-dessus de l'élément
* ' info-bulle ' : ajoute un point d'interrogation à côté du titre pour afficher le texte donné ici
* 'valuekey' : stocker et récupérer la valeur d'une entrée sous cette clé
* 'visiblewhen' : ne montrer l'élément que lorsque la condition donnée est remplie (voir la section [Visibilité des éléments] (#elements-visibility))

## Organiser les éléments
Les entrées et les présentateurs peuvent être écrits dans l'ordre d'apparition à l'intérieur de la balise 'formulaire' ou organisés en colonnes grâce à la balise '<section>'.

*Exemples
Quatre entrées affichées dans une seule colonne :
```xml
<formulaire>
    <saisie />
    <saisie />
    <saisie />
    <saisie />
</formulaire>
```

Quatre éléments affichés dans deux colonnes :
```xml
<formulaire>
    <section>
        <saisie />
        <saisie />
    </section>
    <section>
        <saisie />
        <saisie />
    </section>
</formulaire>
```

## <a nom="types-saisie"></a>Types Saisie

### Choix unique

![choix unique](../../../en/img/content_form_singlechoice.jpg)

```xml
<type de saisie="choixunique" texte="État civil">
    <choix texte="célibataire" />
    <choix texte="union libre" />
    <choix texte="marrié" />
</saisie>
```
Ajoutez autant de balises 'choix' que vous avez de réponses dans l'entrée.
Les réponses peuvent aussi être des images si vous mettez des images dans le dossier du formulaire, en utilisant leurs noms pour remplir l'attribut 'image'.
Si les deux attributs 'texte' et 'image' sont remplis, le texte sera affiché en bas de l'image.

[choix d'une seule image](../../../en/img/content_form_singlechoiceImage.jpg)

```xml
<type de saisie ="choixunique" texte="Civilité" >
    <choix image="homme.png" />
    <choix image="femme.png" />
</saisie>
```

### Choix multiple

![choix multiples](../../../en/img/content_form_multiplechoice.jpg)

```xml
<type de saisie ="choixmultiple" texte="Qui sera concerné par ce contrat ?">
    <choix texte="Moi" />
    <choix texte="Mon partenaire" />
    <choix texte="Mes enfants" />
</saisie>
```
### Texte sur une seule ligne
A zone de texte libre sur une seule ligne.

![une seule ligne](../../../en/img/content_form_singlelinetext.jpg)

```xml
<type de saisie ="texteuneligne" texte="Nom" />
```
### Texte sur plusieurs lignes

![lignes multiples](../../../en/img/content_form_multiplelinetext.jpg)

```xml
<type de saisie ="texteplusieurslignes" texte="Adresse" />
```
### Curseur

![curseur](../../../en/img/content_form_slider.jpg)

```xml
<type de saisie ="curseur" texte="Revenus mensuels" minvalue="0" maxvalue="8000" format="# ##0 €" minlabel="pas de revenu" maxlabel="+ 8 000 €" />
```

* Les attributs 'minlabel' et 'maxlabel' ne sont pas obligatoires mais permettent de personnaliser les valeurs affichées.
* Pour les valeurs possibles de 'format', voir [format standard] (https://docs.microsoft.com/en-gb/dotnet/standard/base-types/standard-numeric-format-strings) et [format personnalisé] (https://docs.microsoft.com/en-gb/dotnet/standard/base-types/custom-numeric-format-strings)
* l'attribut 'frequence' définit l'intervalle entre deux valeurs possibles

Vous pouvez également spécifier toutes les réponses possibles du curseur avec les balises 'choix' :

[choix du curseur](../../../en/img/content_form_sliderChoices.jpg)

```xml
<type de saisie="curseur" texte="Taxes annuelles">
    <choix texte="pas de taxes" />
    <choix texte="- 2 000 €" />
    <choix texte="+ 2 000 €" />
</saisie>
```

### Nombre
Pour saisir un nombre précis.

![nombre](../../../en/img/content_form_numeric.jpg)

```xml
<type de saisie="nombre" texte="Revenu" format="# ##0 €" minvalue="0" maxvalue="10000" />
```
* 'minvalue' et 'maxvalue' sont des attributs non obligatoires, la valeur saisie le sera.
* Pour les valeurs de 'format' possibles, voir [format standard] (https://docs.microsoft.com/en-gb/dotnet/standard/base-types/standard-numeric-format-strings) et [format personnalisé] (https://docs.microsoft.com/en-gb/dotnet/standard/base-types/custom-numeric-format-strings)
* Par défaut,cette entrée empêchera la saisie de caractères non numériques. Ajoutez `allowText="true"` pour permettre la saisie de caractères non numériques si vous préférez. 

### Liste déroulante
Pour lister une grande quantité de réponses dans un espace réduit, il est recommandé d'utiliser une 'liste déroulante' au lieu d'un 'choix unique'.
![liste déroulante](../../../en/img/content_form_combobox.jpg)

```xml
<type de saisie ="liste déroulante" texte="Situation professionnelle">
    <choix texte="employé" />
    <choix texte="chômeur" />
    <choix texte="indépendant" />
</saisie>
```

## <a nom="types-présentateur"></a>Types de présentateurs

### Documents

![documents](../../../en/img/content_form_documents.jpg)

```xml
<type de presenteur="documents" texte="Vos contrats">
    <texte de saisie ="Assurance vie" source="contract 1.pdf" />
    <Source de saisie="Savings.pdf" />
</presentateur>
```

## Autres valeurs

Un `<choix>` de type `novalue` ajoute une case à cocher sous l'entrée pour désélectionner toutes les autres réponses.

![novalue](../../../en/img/content_form_novalue.jpg)

```xml
<type d'entrée="curseur" texte="Revenus mensuels" minvalue="0" maxvalue="8000" format="# ##0 €">
    <type de choix="novalue" texte="Je ne veux pas répondre" />
</entrée>
```

Pour permettre à l'utilisateur de saisir une autre valeur que celles que vous présentez, ajoutez un 'choix' de type 'autre valeur'.

![autrevaleur](../../../en/img/content_form_othervalue.jpg)

```xml
<type de saisie="choixmultiple" texte="Qui sera concerné par ce contrat ?">
    <choix texte="Moi" />
    <choix texte="Mon partenaire" />
    <choix texte="Mes enfants" />
    <choix type="autrevaleur" texte="autre : " />
</saisie>
```


## <a nom="éléments-visibilité"></a>Visibilité des éléments
Vous pouvez choisir d'afficher un élément 'X' (entrée, présentateur ou section) basé sur la valeur d'une entrée 'Y' en utilisant l'attribut "visiblewhen".
Sa valeur doit avoir le motif "clé" "comparateur" "valeur(s)".

La clé est l'attribut "valueKey" de l'entrée "Y".

Les différents comparateurs permettent de tester :
* l'égalité `=`.
* différence "!=
* comparaisons numériques (`<`, `<=`, `>=`, `>`)
* Continuation non stricte

*Exemples
Si nous avons une entrée à choix multiples avec les réponses possibles 'A', 'B' et 'C', nous pouvons avoir les comportements de visibilité suivants sur un autre élément :
* `visiblewhen="myKey=A"` : visible si la réponse `A` est la seule sélectionnée
* `visiblewhen="myKey!=A"` : visible si `B`, `C` ou les deux sont sélectionnés
* `visiblewhen="myKey=*A"` : visible si au moins `A` est sélectionné (`B` et `C` peuvent également être sélectionnés)
* `visiblewhen="myKey=B&C"` : visible si `B` et `C` sont sélectionnés et que `A` n'est pas
* `visiblewhen="myKey=B|C"` : visible si `B`, `C` ou les deux sont sélectionnés et que `A` n'est pas

*exemple de visibilité complète xml :*

```xml
<type de saisie="choixmultiple" texte="Qui voulez-vous protéger ?" valuekey="CiblesprotectionT">
    <choix texte="Moi" />
    <choix texte="Mon partenaire" />
    <choix texte="Mes enfants" />
</saisie>

<type de presentateur="documents" texte="Contrats suggérés" visiblewhen="Ciblesprotection=*Mes enfants">
    <source d'entrée="Assurance scolaire.pdf" />
</presentateur>
```
Vous pouvez également ajouter un attribut 'value' à chaque choix et vous référer à cette valeur dans l'attribut "visiblewhen" :
``xmle
<type de saisie="choixmultiple" texte="Qui voulez-vous protéger ?" valuekey="Ciblesprotection">
    <choix texte="Moi" valeur="moi" />
    <choix texte="Mon partenaire" valeur="partenaire" />
    <choix texte="Mes enfants" valeur="enfants" />
</saisie>

<type de presentateur="documents" texte="Suggestions de contrats" visiblewhen=*enfants">
    <source de saisie="contrat 1.pdf" />
</presentateur>
```
## Télécharger un exemple

Un univers de démonstration contenant un formulaire est disponible, [essayez-le](../Demo-Universe.zip) &#x1f604 ;

Suivant : [Rapport](report.md)

[Retour au contenu pris en charge](index.md)
