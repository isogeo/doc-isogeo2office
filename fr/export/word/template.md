# Modèles d'export au format Word

L'export au format Word fonctionne sur la base d'un modèle afin que l'utilisateur puisse personnaliser l'aspect et l'organisation du document final \(charte graphique, mise en forme...\). Un modèle Isogeo est fourni par défaut pour faciliter la prise en main par l'utilisateur.

Il est possible de créer autant de modèles que besoin.

Voici un aperçu du modèle par défaut :

![Aperçu du modèle Word à personnaliser pour les exports Word](/assets/word_template_overview.png)

## Syntaxe {#syntax}

La syntaxe est celle du moteur de _templating_ Jinja2. Elle fonctionne sur le remplacement automatique de balises par des valeurs générées ou récupérées.

Une balise est caractérisée par les doubles accolades qui l'encadrent: ```{{``` et ```}}```.

Implémentée dans isogeo2office, elle permet :

* de choisir d'afficher ou pas certains champs des métadonnées Isogeo dans les fichiers exportés ;
* de maintenir le style et la mise en forme, puisque les styles et formats appliqués aux balises le seront aussi aux valeurs remplacées. Par exemple, si la balise de titre est en **gras** dans le modèle, le titre sera bien en gras dans le fichier exporté.

## Balises et valeurs possibles {#markups}

Voici le détail des variables avec la valeur correspondante qui peut être soit la valeur d'un champ de métadonnée Isogeo, soit une valeur spécifique à isogeo2office, calculée par l'application.

Il est à noter que, en simplifiant, les balises sont de 2 types :

* "plate" (_flat_) : une balise correspond à une valeur. Exemple : titre, résumé, mots-clés...
* "tableau" (_array_) : la balise contient alors plusieurs valeurs qu'il faut parcourir. Exemple : attributs, spécifications, limitations, CGUs... Sauf à maîtriser la syntaxe, il est recommandé de se baser sur le modèle Isogeo.

> Attention, toutes les variables ne sont pas présentes dans tous les types de métadonnées \(exemple : les attributs pour les rasters). Consulter [la correspondance sur l'aide de la plateforme](https://help.isogeo.com/fr/features/documentation/index.html).

### Étiquettes {#keywords}

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varOwner }} {% endraw %} | Groupe de travail |  |
| {% raw %} {{ varKeywords }} {% endraw %} | Mots-clés | Liste séparée par des \`;\` |
| {% raw %} {{ varKeywordsCount }} {% endraw %} | Nombre de mots-clés |  |
| {% raw %} {{ varInspireTheme }} {% endraw %} | Thèmes INSPIRE |  |
| {% raw %} {{ varInspireConformity }} {% endraw %} | Conformité INSPIRE | OUI ou NON |

---

### Identification {#general}

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :--------------------------------------: | :--------------------------------------------------------------------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %}    | [Titre](https://help.isogeo.com/fr/features/documentation/md_identification.html#titre) |  |
| {% raw %} {{ varAbstract }} {% endraw %} | [Résumé](https://help.isogeo.com/fr/features/documentation/md_identification.html#résumé) |  |
| {% raw %} {{ varPath }} {% endraw %}     | [Emplacement](https://help.isogeo.com/fr/features/documentation/md_identification.html#emplacement--nom-de-la-donnée) | . |

---

### Historique de la donnée {#historic}

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varCollectContext }} {% endraw %} | Contexte de collecte |  |
| {% raw %} {{ varCollectMethod }} {% endraw %} | Méthode de collecte |  |
| {% raw %} {{ varDataDtCrea }} {% endraw %} | Date de création de la donnée |  |
| {% raw %} {{ varDataDtUpda }} {% endraw %} | Date de dernière modification de la donnée |  |
| {% raw %} {{ varDataDtPubl }} {% endraw %} | Date de publication de la donnée |  |
| {% raw %} {{ varValidityStart }} {% endraw %} | Date de début de validité |  |
| {% raw %} {{ varValidityEnd }} {% endraw %} | Date de fin de validité |  |
| {% raw %} {{ validityComment }} {% endraw %} | Commentaire sur la période de validité | . |

---

### Événements de modification sur la donnée {#events}

_Type : "tableau"_

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varEventsCount }} {% endraw %} | Nombre d'événements | Valeur "plate" |
| {% raw %} {{ varEvents }} {% endraw %} | Tableau des événements | |
| {% raw %} {% for event in varEvents %} [...] {% endfor %} {% endraw %} | Boucle sur chaque événement (exemple) | |
| {% raw %} {{ event.date }} {% endraw %} | Date | |
| {% raw %} {{ event.kind}} {% endraw %} | Type | |
| {% raw %} {{ event.description }} {% endraw %} | Description | . |


Exemple dans le modèle Isogeo :

![](/assets/word_syntax_events.png)


---

### Géographie et informations techniques {#technical}

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varNameTech }} {% endraw %} | Nom du fichier ou de la table |  |
| {% raw %} {{ varType }} {% endraw %} | Type de donnée |  |
| {% raw %} {{ varFormat }} {% endraw %} | Format et version |  |
| {% raw %} {{ varGeometry }} {% endraw %} | Type de géométrie |  |
| {% raw %} {{ varObjectsCount }} {% endraw %} | Nombre d'objets |  |
| {% raw %} {{ varSRS }} {% endraw %} | Système de coordonnées |  |
| {% raw %} {{ varScale }} {% endraw %} | Echelle |  |
| {% raw %} {{ varResolution }} {% endraw %} | Résolution |  |
| {% raw %} {{ varTopologyInfo }} {% endraw %} | Topologie | . |

---

### Spécifications {#specifications}

_Type : "tableau"_

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varSpecifications }} {% endraw %} | Tableau des spécifications | |
| {% raw %} {% for spec in varFields %} [...] {% endfor %} {% endraw %} | Boucle sur les spécifications (exemple) | |
| {% raw %} {{ spec.name }} {% endraw %} | Nom | |
| {% raw %} {{ spec.date }} {% endraw %} | Date | |
| {% raw %} {{ spec.conformity }} {% endraw %} | Conformité | |
| {% raw %} {{ spec.link }} {% endraw %} | URL | . |


Exemple dans le modèle Isogeo :
![](/assets/word_syntax_feature-attributes.png)

---

### Conditions de diffusion et d'utilisation {#cgus}

_Type : "tableau"_

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varCGUS }} {% endraw %} | Tableau des conditions | |
| {% raw %} {% for cgu in varCGUS %} [...] {% endfor %} {% endraw %} | Boucle sur les conditions (exemple) | |
| {% raw %} {{ cgu.name }} {% endraw %} | Nom | |
| {% raw %} {{ cgu.content }} {% endraw %} | Contenu | |
| {% raw %} {{ cgu.link }} {% endraw %} | URL | |
| {% raw %} {{ cgu.description }} {% endraw %} | Description | |
| {% raw %} {{ varLimitations }} {% endraw %} | Tableau des limitations | |
| {% raw %} {% for limitation in varLimitations %} [...] {% endfor %} {% endraw %} | Boucle sur les limitations (exemple) | |
| {% raw %} {{ limitation.type }} {% endraw %} | Type | |
| {% raw %} {{ limitation.restriction }} {% endraw %} | Restriction | |
| {% raw %} {{ limitation.inspire }} {% endraw %} | Article INSPIRE | |
| {% raw %} {{ limitation.description }} {% endraw %} | Description | |
| {% raw %} {{ limitation.content }} {% endraw %} | Contenu | . |

---

### Contacts {#contacts}

_Type : "tableau"_

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varContactsCount }} {% endraw %} | Nombre de contacts | Valeur "plate" |
| {% raw %} {{ varContactsDetails }} {% endraw %} | Tableau des contacts |  |
| {% raw %} {% for contact in varContactsDetails %} [...] {% endfor %} {% endraw %} | Boucle sur les contacts (exemple) |  |
| {% raw %} {{ contact.name }} {% endraw %} | Nom du contact |  |
| {% raw %} {{ contact.organization }} {% endraw %} | Organisme |  |
| {% raw %} {{ contact.role }} {% endraw %} | Type |  |
| {% raw %} {{ contact.email }} {% endraw %} | Adresse email |  |
| {% raw %} {{ contact.phone }} {% endraw %} | Numéro de téléphone |  |
| {% raw %} {{ contact.fax }} {% endraw %} | Numéro de fax |  |
| {% raw %} {{ contact.adressLine1 }} {% endraw %} | Adresse postale 1 |  |
| {% raw %} {{ contact.adressLine2 }} {% endraw %} | Adresse postale 2 |  |
| {% raw %} {{ contact.zipCode }} {% endraw %} | Code postal |  |
| {% raw %} {{ contact.city }} {% endraw %} | Ville |  |
| {% raw %} {{ contact.countryCode }} {% endraw %} | Code du pays | . |

---

### Attributs {#feature-attributes}

_Type : "tableau"_

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varFieldsCount }} {% endraw %} | Nombre de champs attributaires | Valeur "plate" |
| {% raw %} {{ varFields }} {% endraw %} | Tableau des attributs | |
| {% raw %} {% for field in varFields %} [...] {% endfor %} {% endraw %} | Boucle sur les attributs (exemple) | |
| {% raw %} {{ field.name }} {% endraw %} | Nom de l'attribut | |
| {% raw %} {{ field.alias }} {% endraw %} | Alias | |
| {% raw %} {{ field.dataType }} {% endraw %} | Type | |
| {% raw %} {{ field.description }} {% endraw %} | Description | . |


Exemple dans le modèle Isogeo :
![](/assets/word_syntax_feature-attributes.png)

---

### Propriétés de la métadonnée {#properties}

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varMdDtCrea }} {% endraw %} | Date de création | |
| {% raw %} {{ varMdDtUpda }} {% endraw %} | Date de dernière mise à jour | |
| {% raw %} {{ varMdDtExpt }} {% endraw %} | Date d'export | |
| {% raw %} {{ varEditAPP }} {% endraw %} | Lien d'édition sur APP | |
| {% raw %} {{ varViewOC }} {% endraw %} | Lien de consultation sur l'OpenCatalog | . |
