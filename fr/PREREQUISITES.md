# Fonctionnement

## Déroulé

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

[![&quot;isogeo2office - Tour guidé en GIF animé&quot;](https://bytebucket.org/isogeo/isogeo-2-office/raw/94895562fd0c1d9f8d9ef2f543175cf6da7a21ff/img/demo_fr.gif)](https://bytebucket.org/isogeo/isogeo-2-office/raw/94895562fd0c1d9f8d9ef2f543175cf6da7a21ff/img/demo_fr.gif "Voir un GIF de démonstration complète")

## Schéma technico-fonctionnel

A titre indicatif, voici un schéma du déroulé technique de l'application :

![&quot;Schéma technico-fonctionnel&quot;](/assets/isogeo2office_SchemaTechnicoFonctionnel.png)

---

# Prérequis

## Isogeo

* au moins un groupe de travail Isogeo ;
* au moins un catalogue contenant au moins une métadonnée, partagé à l'application ;
* le module standard OpenCatalog ;
* des clés d'authentification auprès de l'API Isogeo ;

## Environnement technique

* ordinateur Windows  7+ ;
* droits d’administration le temps de l’installation des dépendances ;
* droits d’écriture sur le dossier d’installation et sur celui de sortie \(“output”\) ;
* une connexion autorisée et configurée \(proxy, pare-feu...\) vers [https://v1.api.isogeo.com/\*](https://v1.api.isogeo.com/) et [https://id.api.isogeo.com/\*](https://v1.api.isogeo.com/)



