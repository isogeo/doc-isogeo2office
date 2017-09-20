# Export des métadonnées en Word

## Résultat

Voici un aperçu du fichier en sortie :![](http://help.isogeo.com/fr/images/isogeo2office_word_result.png)

---

## Options

### Choix du modèle à appliquer

Liste déroulant qui permet de choisir le modèle Word à appliquer pour générer les fichiers. Correspond à la liste des fichiers Word stockés dans le dossier _templates_ de l'installation.

Voir [la section dédiée](/exporter/export-word/modele-dexport.md).

### Personnaliser le nom des fichiers

Le nom du fichier de sortie est de la forme : _\[PREFIXE\]_\__\[MD-UID\]_\_**\[MD-TITRE\]**\__\[DATE-HEURE\]_. Seul le titre de la métadonnée est obligatoirement présent dans le nom du fichier. Les autres éléments servent à garantir l'unicité des noms de fichiers en évitant les conflits entre les métadonnées de même titre \(par exemple, issues de groupes de travail différents\).

#### Préfixe

Champ libre permettant de définir le début des noms des fichiers, dans les limites des [règles inhérentes à Microsoft Windows](https://msdn.microsoft.com/fr-fr/library/windows/desktop/aa365247%28v=vs.85%29.aspx). Il est également recommandé d'éviter les caractères spéciaux.

Valeur par défaut : _isogeo2docx_.

#### UID \(_Unique Identifier_\)

Il s'agit de l'identifiant unique de la métadonnée Isogeo. Il est possible de personnaliser le nombre de caractères à inclure : de 0 à 8.

#### Date

Valeurs possibles :

* 0 : rien n'est ajouté au nom du fichier ;
* 1 : seule la date est ajoutée, sous la forme \`AAAA-MM-JJ\` ;
* 2 : la date et l'heure est ajoutée, sous la forme \`AAAA-MM-JJ-HHmmSS\`.


