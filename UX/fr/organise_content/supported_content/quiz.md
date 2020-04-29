# Quiz

## Résumé 
* [Description](#description)
* [Actions au sein de Compositeur Digital UX] (#actions-au-sein-du-compositeur-digital-ux)
* [Extension de contenu](#extension-de-contenu)
* [Questions : questions.xml](#questions--_questionsxml)
   * [Sections](#sections)
   * [Pages](#pages)
   * [Ordre des pages](#ordre-des-
   * [Types de page](#types-de-page)
      * [Question Page](#questionpage)
      * [Page](#page)
      * [Page d'information](#page-d'information)
      * [Page du curseur numérique](#pageducurseurnumérique)
      * [Page de Défilement Étiquette](#pagededéfilementétiquette)
      * [Page de Défilement Image](#pagededéfilementimage)
      * [Page de Document](#pagededocument)
      * [Page de commande](#pagedecommande)
      * [Page de scores](#pagedescores)
* [Créer un quiz](#créer-un-quiz)
* [Télécharger un exemple] (#télécharger-un-exemple)

## Description

Ce type de contenu vous permet d'afficher des quiz interactifs, qui vous aideront à comprendre les besoins de vos utilisateurs.

![Quiz affiché dans le Compositeur Digital UX](../../../en/img/content_quizz.JPG)   

## Actions au sein du Compositeur Digital UX

Les quiz prennent en charge les actions suivantes. Pour avoir un aperçu complet de chaque action, [voir la section Actions](actions.md)

**Menu des actions**

| Annoter   | Capturer  | Dupliquer | Ouvrir dans l'app native | Enregistrer sous | Sélection | Partager |

| &#x2716 ; | &#x2716 ; | &#x2714 ; | &#x2714 ;                | &#x2714 ;        | &#x2714 ; | &#x2714 ; |

**Interaction avec l'article**

| Lancer les articles | Suivant | Précédent | Questions |
|:-------------------:|:--------:|:--------:|:---------:|
| &#x2714;            | &#x2714; | &#x2714; | &#x2714;  |

## Extension du contenu

Pour utiliser un quiz, mettez tous les éléments dont vous avez besoin dans un dossier, et ajoutez l'extension '.quiz' à la fin du nom de votre dossier.

Dans votre dossier, fournissez un fichier appelé `_questions.xml`, et un dossier appelé `_meta` qui contiendra toutes les images utilisées dans le quiz.

### <a name="questions"></a>Questions : `_questions.xml`

Le fichier du quiz doit contenir deux parties : 'sections' et 'pages'.
Structure de fichier générique :
```xml
<quizz>
    <sections>
        liste de sections
    </sections>ˋ
    <pages>
        liste de pages
    </pages>
</quizz>
```

Chaque page décrira une question. Les sections vous permettront de regrouper les pages qui portent le même nom de section. 

#### Sections
Définissez la section afficher le nom dans une balise 'section' et définissez éventuellement l'attribut 'id' si vous avez besoin de créer une
référence à cette section.

```xml
<section id="intro">1. INTRODUCTION</section>
```

#### Pages
Vous pouvez créer un quiz avec différents types de pages, mais toutes les pages doivent avoir les éléments suivants en commun :
 - un attribut 'sectionId' qui attribue une page à une section. Le nom de la section apparaîtra en haut de la page.
 - un attribut `id` facultatif à utiliser comme identifiant si une référence à cette page est nécessaire. 
 - un attribut `nextPageId` : référence optionnelle à la page qui doit être affichée ensuite. Si cet attribut n'est pas défini, la page suivante décrite dans le fichier sera utilisée. 

#### Ordre des pages 
La première page décrite dans la liste sera toujours la première page affichée.
La dernière page décrite sera par défaut la dernière page affichée,
Pour forcer une page à terminer le quiz, définissez la valeur de l'attribut 'nextPageId' à 'atend'.

#### Types de page
##### `questionPage`
Ce type permet de créer une question à réponses multiples. Veuillez noter qu'une réponse doit être sélectionnée avant de passer à la page suivante.

Voici les attributs de 'questionPage':

| clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `allowMultiple` | Réglez sur 'vrai' pour permettre la sélection de réponses multiples.					       | 
| `id`            | L'id de la question.                                                                            |
| `label`         | Texte de la question à afficher. Remplace l'attribut 'visuel'.    				       |
| `sectionId`     | Définit l'id de la section à laquelle appartient la question.                                              |
| `sideVisual`    | Affiche une image en plus de vos questions. L'image doit exister dans le dossier `_meta`.              |
| `visual`        | Nom du fichier image de la question (sans extension). Le fichier doit exister dans le dossier `_meta`.    |

Le contenu de la 'questionPage' est la liste des réponses, qui peuvent être de différents types :
 - des réponses textuelles, avec la balise 'réponse' :
 ```xml
 <réponse>ma réponse</réponse>
 ```
 - des réponses visuelles, avec le tag 'imageAnswer'. Définissez l'attribut `visual` au nom de l'image cible (sans extension) dans le dossier `_meta` :
   ``xml
   <imageAnswer visual="image 2"/>
   ```
   Vous pouvez éventuellement mettre une légende :
   "xml
   <imageAnswer visual="image 2">ma légende</imageAnswer>
   ```
Il n'est pas possible de mélanger des réponses textuelles et des réponses visuelles dans une même question.

Vous pouvez définir des questions conditionnelles en fonction des réponses fournies par l'utilisateur. Pour ce faire, utilisez l'attribut `nextPageId` pour passer à une page spécifique pour une réponse donnée : 

``xml
<questionPage id="Q1" sectionId="section 2" label="À quelle question souhaitez-vous répondre ? >
	<réponse>La question suivante</réponse>
	<réponse nextPageId="Q1">Celle-ci encore</réponse>
	<réponse nextPageId="Q3">Sauter en une svp</réponse>
</questionPage>

<questionPage id="Q2" sectionId="section 3" label="La question suivante">
	...
</questionPage>	
	
<questionPage id="Q3" sectionId="section 3" label="La dernière question">
	...
</questionPage>
```
![questionPage](../../../en/img/content_quizz_questionpage.JPG)

##### `page`
Décrit une page simple à afficher avec du texte ou des images:

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `id`            | L'id de la question.                                                                            |
| `label`         | Texte de la question à afficher. Remplace l'attribut 'visuel'.	    			       |
| `sectionId`     | Définit l'id de la section à laquelle appartient la question.                                              |
| `visual`        | Nom du fichier image de la question (sans extension). Le fichier doit exister dans le dossier `_meta`.    |	 

```xml
<page sectionId="intro" étiquette="C'est un test"/>
```

##### `infoPage`
Affiche un formulaire simple dans lequel l'utilisateur peut saisir des réponses textuelles. 

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `id`            | L'id de la question.                                                                            |
| `label`         | Titre de la page d'information.  			                                               | 
| `sectionId`     | Définit l'id de la section à laquelle appartient la question.                                              |
| `valueKey`      | Relie cette valeur à une valeur partagée au niveau de votre projet. Voir page [Valeurs partagées](../advanced_setting.md#valeurs partagées).

Définissez l'attribut `étiquette` des balises `info` pour définir un nom pour la zone de texte.

``xml
<infoPage sectionId="intro" étiquette="Veuillez décliner votre identité">
	<info étiquette="Nom"/>
	<info étiquette="Prénom"/>
</infoPage>
```

![infoPage](../../../en/img/content_quizz_infopage.JPG)

##### `numericSliderPage`
Affiche une page avec un seul curseur qui permet à l'utilisateur de choisir une valeur numérique (arrondie) :

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `default`       | (Facultatif) Valeur présélectionnée.                                                                      |
| `format`        | Modifie la façon dont la valeur est affichée.                                                            |
| `id`            | L'id de la question.                                                                            |
| `label`         | Texte de la question à afficher.                                    	    			       |
| `max`           | Valeur maximale sélectionnable.                                                                          |
| `maxLabel`      | (Facultatif) Valeur d'affichage spécifique pour la valeur maximale.                                           |  
| `min`           | Valeur minimale sélectionnable.                                                                          |
| `minLabel`      | (Facultatif) Valeur d'affichage spécifique pour la valeur minimale.                                           | 
| `sectionId`     | Définit la section id à laquelle la question appartient.                                              |
| `stepSize`      | Différence entre deux pas du curseur.						       |
| `valueKey`      | Reliez cette valeur à une valeur partagée au niveau de votre projet. Voir page [Valeurs partagées](../advanced_setting.md#valeurs partagées). La seule valeur numérique qui peut être partagée est 'finance.budget'. Elle définit le prêt hypothécaire en cours. |

Quelques 'formats' possibles :
 - 'N0' : valeur arrondie
 - 'C0' : valeur monétaire arrondie selon le contexte régional actuel (c'est-à-dire en utilisant €, £, $, etc., le cas échéant)

"xml
<numericSliderPage id="fonds" sectionId="section 3" label="Vos fonds disponibles" min="0" max="5000000" stepSize="5000" format="C0" valueKey="finance.budget" />
```
![numericSliderPage](../../../en/img/content_quizz_numericslider.JPG)

##### `labelSliderPage`
Cela affiche une page avec un curseur avec des valeurs prédéfinies.

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `id`            | L'id of de la question.                                                                            |
| `label`         | Texte de la question à afficher.  			                                                       | 
| `sectionId`     | Définit l'id de la section à laquelle appartient la question.                                              |

Ajoutez des balises 'réponse' pour ajouter des valeurs prédéfinies, la première étant le minimum et la dernière le maximum.

exemple :
```xml
<labelSliderPage sectionId="section1" label="Faites vous souvent des achats en ligne ?">
	<réponse>Jamais</réponse>
	<réponse>Parfois</réponse>
	<réponse>Souvent</réponse>
	<réponse>Toujours</réponse>
</labelSliderPage>
```
![labelSliderPage](../../../en/img/content_quizz_labelslider.JPG)


##### `imageSliderPage`
Ce type offre la même fonctionnalité que le précédent 'labelSliderPage' mais en utilisant des images pour des valeurs prédéfinies.

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `id`            | L'id de la question.                                                                            |
| `label`         | Titre de la page.  			                                               | 
| `leftVisual`    | Image à gauche du curseur.                                                                 |
| `rightVisual`   | Image à droite du curseur.                                                                |
| `sectionId`     | Définit la section id à laquelle la question appartient.                                              |
| `stepQuantity`  | Le nombre d'étapes sélectionnables (valeur recommandée : 10).                                           |
| `visual`        | Nom du fichier image de la question (sans extension). Le fichier doit exister dans le dossier `_meta`.    |

```xml
<imageSliderPage sectionId="part 1" label="Qu'est ce qui vous caractérise le plus:" leftVisual="image1" rightVisual="image2" stepQuantity="10"/>
```
![imageSliderPage](../../../en/img/content_quizz_imageslider.JPG)

##### `documentPage`
Affiche un lien pour ouvrir un document dans le Compositeur Digital.

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `document`      | Nom du document à ouvrir, qui doit être disponible dans le même dossier que le quiz.              |
| `id`            | L'id de la question.                                                                            |
| `label`         | Titre de la page.  			                                             	       | 
| `sectionId`     | Définit l'id de la section à laquelle appartient la question.                                              |

```xml
<documentPage texte="simulateur de prêt" nextPageId="@end" document="Simutaeur de prêt"/>
```

##### `orderPage`
Affiche une liste de valeurs à commander par l'utilisateur.

| Clés            | Description                                                                                        |
|:----------------|:---------------------------------------------------------------------------------------------------|
| `answerNumber`  | Nombre minimum de réponses à sélectionner.           						       |
| `id`            | L'id de la question.                                                                            |
| `label`         | Texte de la question à afficher.  			                                             	       | 
| `sectionId`     | Définit la section id à laquelle la question appartient.                                              |
| `sideVisual`    | Vous permet d'afficher une image en plus de vos questions. L'image doit exister dans le dossier `_meta`. |

Ajoutez une liste de 'réponses' ou `imageAnswer` pour les choix disponibles. Les deux types ne peuvent pas être mélangés.

```xml
<orderPage sectionId="section 1" étiquette="Prioriser vos projets" answerNumber="3">
    <réponse>Rénovation</répons>
    <réponse>Acheter une maison</réponse>
    <réponse nextPageId="tousLesBiens">Acheter une voiture</réponse>
    <answer nextPageId="tousLesBiens">Préparer sa retraite</answer>
</orderPage>
```

```xml
<orderPage sectionId="section 1" étiquette="Je préfère vivre dans un" answerNumber="2">
    <visualAnswer visual="maison" visualChecked="test1">Maison</visualAnswer>
    <visualAnswer visual="appartement" visualChecked="test2">Appartement</visualAnswer>
</orderPage>
```

![Order page sample](../../../en/img/content_quizz_orderpage.JPG)


##### `scoresResultPage`
Affiche un message basé sur l'addition des scores des réponses.
Une `scoreResultPage` contient un élément "scoreResult" pour chaque résultat à afficher.

| Clés          | Description                                                                                        |
|:--------------|:---------------------------------------------------------------------------------------------------|
| `scoreMax`    | Score maximum qui indiquera ce `scoreResult`.            					     |
| `title`       | Titre du message                                                                               |
| `sideVisual`  | Affiche une image en plus de votre message. L'image doit exister dans le dossier `_meta`.                |  

Le message lui-même est un contenu écrit entre les balises d'ouverture et de fermeture `scoreResult`.
Notez que le score minimum sera le score le plus élevé parmi les autres 'scoreResult'.

```xml
<questionPage label="Hello !">
    <réponse score="1" >réponse A</réponse>
    <réponse score="2" >réponse B</réponse>
    <réponse score="3" >réponse C</réponse>
</questionPage>
	
<questionPage allowMultiple="vrai">
    <réponse score="-1" >réponse A</réponse>
    <réponse score="0" >réponse B</réponse>
    <réponse score="3" >réponse C</réponse>
</questionPage>

<scoresResultPage>
    <scoreResult title="Profil A" scoreMax="0">
        Vous semblez n'avoir répondu que A à toutes les questions...
    </scoreRésultat>
    <scoreResult title="Profil B" scoreMax="2">
        Si vous voyez ce message, il y a trois scénarios possibles :
        - vous avez répondu A puis B
        - vous avez répondu B puis A ou B
        - vous avez répondu C puis A
    </scoreRésultat>
    <scoreResult title="Profil C" scoreMax="6">
        Un cas sur deux devrait afficher ce message.
    </scoreResult>
</scoresResultPage>
```


## Créer un quiz

1. Dans votre dossier environnement, créez un dossier nommé '>Nom de votre séquence>.quiz' (par exemple "Mon quiz.quiz").
1. Dans ce dossier, ajoutez un fichier nommé `_questions.xml`.
1. (Facultatif) Si vous avez besoin de ressources graphiques pour votre quiz, créez un dossier nommé `_meta`.
1. (Facultatif) Mettez toutes les images dont vous avez besoin dans ce dossier.
1. ( Facultatif ) Si vous voulez lier des documents de votre quiz, mettez ces documents dans le dossier `.quiz`.
1. (Facultatif) Si vous voulez ajouter un aperçu à votre quiz, ajoutez un fichier nommé `_preview.jpg` ou `_preview.png` dans votre dossier. 

**Note** : Par défaut, un quiz n'a pas de prévisualisation. N'oubliez pas d'en créer un si vous en avez besoin.

! [Dossier du quiz](../../../en/img/content_quizz_folder.JPG)

## Télécharger un exemple

Un univers de démonstration contenant un échantillon pour un quiz est disponible, [essayez-le !](../Demo-Universe.zip) &#x1f604 ;

Next : [Interface de recherche (Format du Compositeur Digital UX)](search.md)

[Retour au contenu pris en charge](index.md)

