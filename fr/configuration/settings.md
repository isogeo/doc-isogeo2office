# Préférences

## Onglet des paramètres {#tab}

La majorité des paramètres peuvent être réglés directement depuis l'interface graphique.

![Onglet des paramètres](/assets/i2o_settings_global.png)

### Options d'export {#export}

### Dossier de sortie {#output_folder}

Par défaut, les fichiers générés sont stockés dans le sous-dossier `_output`. Dans ce menu, il est possible de :

- choisir un autre dossier de sortie
- ouvrir le dossier de sortie

### Personnaliser le nom des fichiers {#filenames}

Le nom du fichier de sortie est de la forme : _\[PREFIXE\]_\__\[MD-UID\]_\_**\[MD-TITRE\]**\__\[DATE-HEURE\]_. Seul le titre de la métadonnée est obligatoirement présent dans le nom du fichier. Les autres éléments servent à garantir l'unicité des noms de fichiers en évitant les conflits entre les métadonnées de même titre \(par exemple, issues de groupes de travail différents\).

#### Préfixe

Champ libre permettant de définir le début des noms des fichiers, dans les limites des [règles inhérentes à Microsoft Windows](https://msdn.microsoft.com/fr-fr/library/windows/desktop/aa365247%28v=vs.85%29.aspx). Il est également recommandé d'éviter les caractères spéciaux.

Valeur par défaut : _isogeo2office_.

#### Date

Valeurs possibles :

- rien n'est ajouté au nom du fichier ;
- seule la date est ajoutée, sous la forme \`AAAA-MM-JJ\` ;
- la date et l'heure est ajoutée, sous la forme \`AAAA-MM-JJ-HHmmSS\`.

Valeur par défaut : _rien_.

#### UUID \(_Universal Unique Identifier_\)

Il s'agit de l'identifiant unique de la métadonnée Isogeo.
Il est possible de personnaliser le nombre de caractères à inclure : de 0 à 8.

Valeur par défaut : _5_.

----

### Autres {#other}

#### Minimiser l'application pendant l'export

Cette option permet de réduire la fenêtre de l'application dans la barre des tâches pendant l'export. Elle est restaurée (affichée) à la fin du traitement ou en cas de problème.

![Application minimisée dans la barre des tâches](/assets/systray_icon.png)

----

## Paramètres additionnels {#advanced}

D'autres paramètres peuvent être réglés

### Fichier de configuration de l'environnement {#environment_file}

Dans certaines configurations avancées, il est possible d'utiliser un fichier de configuration d'environnement `.env`.

Structure type du fichier :

```conf
# GLOBAL
ISOGEO_PLATFORM=prod
OAUTHLIB_INSECURE_TRANSPORT=0

# URLS
ISOGEO_API_URL=https://api.isogeo.com/
ISOGEO_ID_URL=https://id.api.isogeo.com/

# PROXY
HTTP_PROXY=
HTTPS_PROXY=

# API - GROUP (Client Credentials)
ISOGEO_API_CLIENT_ID=
ISOGEO_API_CLIENT_SECRET=
```

### Stockage des paramètres {#location}

Les paramètres sont stockés dans la base de registre Windows : `Ordinateur\HKEY_CURRENT_USER\Software\Isogeo\IsogeoToOffice\`

![Paramètres sauvegardés dans la base de registre de Windows](/assets/settings_location_registry.png)
