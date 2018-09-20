# Déploiement - installation {#install}

## Installation

Isogeo2office se présente sous la forme d'un exécutable autonome, livré dans une archive ZIP. Cela signifie qu'il n'y a pas de processus d'installation à proprement parler sur le système \(l'application peut donc être utilisée depuis une clé USB\).

Procédure détaillée pour lancer l'application :

1. Créer un dossier dans :
   * si administrateur sur la machine : `C:\Programmes\Isogeo\isogeo2office`
   * sinon : `C:\Users\%USERNAME%\AppData\Local\Isogeo\isogeo2office`
   * ou si l'utilisateur préfère : `C:\Users\%USERNAME%\Documents\Isogeo\isogeo2office`
2. Dézipper l'archive isogeo2office.zip fournie ;
3. Lancer `isogeo2office.exe`.

Pour plus de simplicité, comme pour n'importe quelle application Windows, il est parfaitement possible de créer un raccourci ou d'épingler l'application dans la barre des tâches.

## Mise à jour {#update}

Pour mettre à jour l'application, il suffit de remplacer tous les fichiers du dossier par ceux de la nouvelle version. Les préférences et les paramètres d'authentification sont conservés.

---

## Structure du dossier d'installation

Une seule chose à retenir ? `isogeo2office.exe` : exécutable de l'application. C'est le seul fichier à ouvrir pour utiliser le programme.

Par défaut, l'application embarque certains dossiers et fichiers qui sont de 2 types :

* les dossiers d'usage : préfixés d'un underscore \(`_`\) sont ceux amenés à contenir les éléments liés à l'utilisation \(fichiers journaux, table de correspondance des vignettes, modèles Word...\).
* les autres dossiers sont les dossiers "technique". Ils ne doivent en aucun cas être modifiés manuellement.

Quelques-uns des dossiers d'usage :

* `_auth`: dossier où placer le fichier d'authentification à l'API pour éviter à l'utilisateur d'affronter le formulaire d'authentification
* `_logs`: dossier contenant les fichiers journaux \(logs\)
* `_output`: dossier de sortie par défaut des fichiers exportés \(voir [la configuration](/configuration/configuration/configui.md)\)

* `_templates`: dossier où stocker les modèles pour l'export en format word \(voir [la section dédiée](/exporter/export-word/modele-dexport.md)\)

* `_thumbnails`: dossier où est stocké le fichier Excel _thumbnails.xlsx_ utilisé pour gérer les vignettes pour l'export en format word \(voir [la section dédiée](/exporter/export-word/modele-dexport.md)\)

![&quot;Aperçu du dossier d&apos;installation&quot;](/assets/isogeo2office_install_dir.png)

