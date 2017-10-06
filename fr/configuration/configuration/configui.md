# Configuration via l'interface graphique

## Authentification

Au premier lancement de l'application, l'utilisateur doit entrer les clés oAuth2 \(un identifiant et un secret\) qui lui ont été transmises par l'équipe Isogeo :

!["Formulaire d'authentification d'Isogeo to Office à l'API Isogeo"](/assets/isogeo2office_auth_form_FR.png)

Si l'utilisateur ne dispose pas de clés d'authentification, il peut en faire la demande en envoyant un mail à [projets@isogeo.fr](mailto:projets@isogeo.fr) ou cliquer sur le bouton `Demande d'accès`\(s'il dispose d'un client mail par défaut configuré sur son ordinateur.

Une fois l'authentification établie, l'application indique :

* le total de métadonnées partagées ;
* le nombre de partages qui l'alimentent ;
* le nombre de groupes de travail lui partageant des catalogues ;
* si la configuration est correcte. Dans le cas contraire, le message d'erreur apparaît dans la barre d'état en bas de la fenêtre.

A tout moment, l'utilisateur peut entrer de nouvelles clés en cliquant sur le bouton `Accès`.

## Raccourcis divers

En regard des informations de configuration, 4 boutons sont proposés :

* `Administrer` : ouvre la page d'administration de chaque partage pointant sur l'application dans le navigateur web par défaut.
* `Contacter`: ouvre le client email par défaut configuré sur la machine de l'utilisateur pour envoyer un courriel préformaté à l'équipe Isogeo.
* `Accès`: permet de changer les clés d'authentification à l'API \(voir ci-dessus\).
* `Signaler`: ouvre la page de signalement des anomalies de l'application.

## Choix d'export et lancement

Dans le volet du bas, l'utilisateur peut :

* choisir une ou plusieurs options d'export ;
* choisir le dossier de stockage des fichiers de sortie \(valeur par défaut : dossier _output_ de l'installation\). Son nom est rappelé dans l'interface ;
* ouvrir le dossier de stockage dans son explorateur.

C'est aussi dans ce volet qu'il peut lancer le processus d'export.

