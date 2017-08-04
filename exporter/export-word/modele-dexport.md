# Modèles d'export au format Word

L'export au format Word fonctionne sur la base d'un modèle afin que l'utilisateur puisse personnaliser l'aspect et l'organisation du document final \(charte graphique, mise en forme...\). Un modèle Isogeo est fourni par défaut pour faciliter la prise en main par l'utilisateur.

Il est possible de créer autant de modèles que besoin.

Voici un aperçu du modèle par défaut :
![](http://help.isogeo.com/fr/images/isogeo2office_word_template.png)

## Syntaxe

La syntaxe est celle du moteur de _templating_ Jinja2.

## Valeurs possibles du template

Voici le détail des variables avec la valeur correspondante qui peut être de 2 types :

* la valeur d'un champ de métadonnée Isogeo ;
* une valeur spécifique à isogeo2office.

> Attention, toutes les varaibles ne sont pas présentes dans tous les types de métadonnées \(exemple : les attributs pour les rasters\). Consulter [la correspondance sur l'aide de la plateforme](http://help.isogeo.com/fr/features/documentation/index.html).

### Etiquettes

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varOwner }} {% endraw %} | Groupe de travail |  |
| {% raw %} {{ varKeywords }} {% endraw %} | Mots-clés | Liste séparée par des \`;\` |
| {% raw %} {{ varKeywordsCount }} {% endraw %} | Nombre de mots-clés |  |
| {% raw %} {{ varInspireTheme }} {% endraw %} | Thèmes INSPIRE |  |
| {% raw %} {{ varInspireConformity }} {% endraw %} | Conformité INSPIRE | OUI ou NON |

---

### Identification

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %} | [Titre](http://help.isogeo.com/fr/features/documentation/md_identification.html#titre) |  |
| {% raw %} {{ varAbstract }} {% endraw %} | [Résumé](http://help.isogeo.com/fr/features/documentation/md_identification.html#résumé) |  |
| {% raw %} {{ varPath }} {% endraw %} | [Emplacement](http://help.isogeo.com/fr/features/documentation/md_identification.html#emplacement--nom-de-la-donnée) |  |

---

### Historique de la donnée

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varDataDtCrea }} {% endraw %} | Date de création de la donnée |  |
| {% raw %} {{ varDataDtUpda }} {% endraw %} | Date de dernière modification de la donnée |  |
| {% raw %} {{ varDataDtPubl }} {% endraw %} | Date de publication de la donnée |  |
| {% raw %} {{ varValidityStart }} {% endraw %} | Date de début de validité |  |
| {% raw %} {{ varValidityEnd }} {% endraw %} | Date de fin de validité |  |
| {% raw %} {{ validityComment }} {% endraw %} | Commentaire sur la période de validité |  |

---

### Evénements sur la donnée

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %} | Titre |  |
| {% raw %} {{ varAbstract }} {% endraw %} | Résumé |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

---

### Géographie et informations techniques

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %} | Titre |  |
| {% raw %} {{ varAbstract }} {% endraw %} | Résumé |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

---

### Conditions de diffusion et d'utilisation

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %} | Titre |  |
| {% raw %} {{ varAbstract }} {% endraw %} | Résumé |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |


---

### Contacts

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %} | Titre |  |
| {% raw %} {{ varAbstract }} {% endraw %} | Résumé |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

---

### Attributs

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :------: | :---------------------------- | :------------------------ |
| {% raw %} {{ varTitle }} {% endraw %} | Titre |  |
| {% raw %} {{ varAbstract }} {% endraw %} | Résumé |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |











