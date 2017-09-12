# Déploiement et utilisation

Isogeo2office se présente sous la forme d'un exécutable autonome dans une archive ZIP. Cela signifie qu'il n'y a pas de processus d'installation à proprement parler sur le système et que le programme est utilisable sur une clé USB.

Procédure détaillée pour lancer l'application :

1. Créer un dossier dans :
   * si administrateur sur la machine : `C:\Programmes\Isogeo\isogeo2office`
   * sinon : `C:\Users\%USERNAME%\AppData\Local\Isogeo\isogeo2office`
   * ou si l'utilisateur préfère : `C:\Users\%USERNAME%\Documents\Isogeo\isogeo2office`
2. Dézipper l'archive isogeo2office.zip fournie ;
3. Lancer `isogeo2office.exe`.

Pour plus de simplicité, il est parfaitement possible de créer un raccourci, comme pour n'importe quelle application Windows.

## Structure du dossier d'installation

Malgré la profusion de dossiers et fichiers contenus dans l'archive, seuls certains sont importants à retenir :

* `output`: dossier de sortie par défaut des fichiers exportés \(voir [la configuration](/configuration/configuration/configui.md)\) ;
* `templates`: dossier où stocker les modèles pour l'export en format word \(voir [la section dédiée](/exporter/export-word/modele-dexport.md)\) ;
* `isogeo2office.exe` : exécutable de l'application. C'est le seul fichier à ouvrir pour utiliser le programme.
* `settings.ini` : fichier de configuration du programme. Ne doit être édité manuellement qu'en cas de besoin de configuration avancée \(voir [section dédiée](/configuration/configuration/configadvanced.md)\).

!["Aperçu du dossier d'installation"](/assets/isogeo2office_install_dir.png)

