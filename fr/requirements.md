# Prérequis {#requirements}

## Isogeo

* au moins un groupe de travail Isogeo ;
* au moins un catalogue contenant au moins une métadonnée, partagé à l'application ;
* le module standard OpenCatalog ;
* des clés d'authentification à l'API Isogeo sous forme d'un fichier _client_secrets.json_ ;

## Environnement technique

* ordinateur Windows 7+ mais support uniquement sur Windows 10+ ;
* droits d’écriture sur le dossier d’installation et sur celui de sortie ;
* une connexion autorisée et configurée \(proxy, pare-feu...\) vers [https://*.api.isogeo.com](https://api.isogeo.com/about)

## Proxy {#proxy}

Si la connexion doit se faire via un proxy, quelques réglages supplémentaires sont à réaliser.

### Indiquer les paramètres du proxy à l'application {#proxy_app}

Ajouter les paramètres de proxy au [fichier de configuration de l'environnement](configuration/settings.md#environment_file) :

1. Créer/éditer le fichier `.env` à la racine du dossier d'installation
2. Ajouter les lignes `HTTP_PROXY`et `HTTPS_PROXY` en renseignant l'URL du proxy comme dans les exemples ci-dessous :

```ini
# proxy sans authentification
HTTP_PROXY=http://url:port/
HTTPS_PROXY=https://url:port/
# proxy avec authentification
HTTP_PROXY=http://identifiant:mot_de_passe@url:port/
HTTPS_PROXY=https://identifiant:mot_de_passe@url:port/
```

### Configuration Windows {#proxy_windows}

Configurer directement le proxy depuis les paramètres Windows. Exemple sous Windows 10 :

![Configuration du proxy sous Windows 10 pour autoriser les connexions vers l&apos;API Isogeo](/assets/settings_proxy_win10_api.png)
