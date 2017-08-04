# Modèles d'export au format Word

L'export au format Word fonctionne sur la base d'un modèle afin que l'utilisateur puisse personnaliser l'aspect et l'organisation du document final \(charte graphique, mise en forme...\). Un modèle Isogeo est fourni par défaut pour faciliter la prise en main par l'utilisateur.

Il est possible de créer autant de modèles que besoin.

## Syntaxe

La syntaxe est celle du moteur de _templating_ Jinja2. 



## Valeurs possibles du template

Voici le détail des variables avec la valeur correspondante qui peut être de 2 types :

* la valeur d'un champ de métadonnée Isogeo ;
* une valeur spécifique à isogeo2office.

> Attention, toutes les varaibles ne sont pas présentes dans tous les types de métadonnées \(exemple : les attributs pour les rasters\). Consulter [la correspondance sur l'aide de la plateforme](http://help.isogeo.com/fr/features/documentation/index.html).

### Etiquettes

| Variable | Champ ou valeur correspondant | Commentaires / précisions |
| :--- | :--- | :--- |
| \{{ varOwner }}  | Groupe de travail |  |
| {{ varKeywords }\}  | Mots-clés | Liste séparée par des \`;\` |
| {{ varKeywordsCount }} | Nombre de mots-clés |  |
| {{ varInspireTheme }} | Thèmes INSPIRE |  |
| {{ varInspireConformity }} | Conformité INSPIRE | OUI ou NON |

---

### Identification

| Variable | Champ Isogeo correspondant | Commentaires |
| :--- | :--- | :--- |
| {{ varTitle }} | [Titre](http://help.isogeo.com/fr/features/documentation/md_identification.html#titre) |  |
| {{ varAbstract }} | [Résumé](http://help.isogeo.com/fr/features/documentation/md_identification.html#résumé) |  |
| {{ varPath }} | [Emplacement](http://help.isogeo.com/fr/features/documentation/md_identification.html#emplacement--nom-de-la-donnée) |  |

---

### Histoire de la donnée

| Variable | Champ Isogeo correspondant | Commentaires |
| :--- | :--- | :--- |
| {{ varDataDtCrea }} | Date de création de la donnée |  |
| {{ varDataDtUpda }} | Date de dernière modification de la donnée |  |
| {{ varDataDtPubl }} | Date de publication de la donnée |  |
| {{ varValidityStart }} | Date de début de validité |  |
| {{ varValidityEnd }} | Date de fin de validité |  |
| {{ validityComment }} | Commentaire sur la période de validité |  |

---

### dentification

| Variable | Champ Isogeo correspondant | Commentaires |
| :--- | :--- | :--- |
| {{ varTitle }} | Titre |  |
| {{ varAbstract }} | Résumé |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |



