# Export des métadonnées au format XML ISO 19139

L’export consiste en la récupération de la version XML de chaque métadonnée, fournie par Isogeo. Il est possible de générer automatiquement un fichier compressé au format ZIP contenant toutes les fiches du partage. Idéal pour l’échange massif standardisé ou une démarche de sauvegarde.

> Le format XML ISO 19139 est celui recommandé dans la directive INSPIRE et le plus répandu dans les échanges de catalogues de métadonnées.

## Résultat

Voici un aperçu des fichiers en sortie, contenus dans leur archive ZIP :![](/assets/isogeo2office_xml_result.png)

## Options

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

### Consolider dans une archive zippée

Option permettant de regrouper tous les fichiers dans un seul fichier ZIP.

