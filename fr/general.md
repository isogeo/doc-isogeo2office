# Fonctionnement

## Déroulé {#scenario}

Voici le scénario d'utilisation :

1. Au lancement de l'application : test de la connexion internet, création du fichier de log ;
2. Authentification à Isogeo et vérification de la configuration ;
3. Chargement de l'interface graphique ;
4. L'utilisateur fait ses choix :
   * format\(s\) d'export souhaité\(s\) ;
   * options liées à chaque format ;
   * dossier de sortie ;
5. Une fois le processus lancé, l'application récupère l'ensemble des métadonnées auprès de l'API Isogeo ;
6. Les métadonnées sont pré-traitées et nettoyées pour garantir l'export ;
7. L'export est effectué dans l'ordre suivant : Excel, Word puis XML. Chaque étape est indiquée dans la barre d'état en bas.
8. Une fois le traitement terminé, l'utilisateur peut fermer l'interface.

## Schéma technico-fonctionnel {#schema}

A titre indicatif, voici un schéma du déroulé technique de l'application :

![Schéma technico-fonctionnel](/assets/isogeo2office_SchemaTechnicoFonctionnel.png)
