# Configuration avancée

> **Attention : cette partie est réservée aux utilisateurs avertis.**

Il est possible d'éditer directement les options dans le fichier de configuration `settings.ini` pour certains cas :

* paramètres de proxy ;
* gestion de plusieurs fichiers de configuration \(usage massif avancé\).

## Structure du fichier _settings.ini_

```ini
[auth]
app_id =         # identifiant OAuth 2.0 - attention, normalement stocké en variable d'environnement
app_secret =     # secret OAuth 2.0 - attention, normalement stocké en variable d'environnement

[global]
def_oc = 
def_codelang = FR    # langue de l'application et des requêtes à l'API (FR ou EN)
out_folder = C:\Users\%USERNAME%\Documents\Isogeo\isogeo2office\output   # chemin du dossier pour les fichiers exportés

[proxy]
proxy_needed = 0                    # indique si un proxy est utilisé pour se connecter à l'API
proxy_type = 0                      # indique le type de proxy (basique ou NLTM)
proxy_prot = http                   # protocole utilisé par le proxy
proxy_server = proxy.server.com     # adresse du proxy
proxy_port = 80                     # port du proxy
proxy_user = proxy_user             # utilisateur du proxy

[excel]
excel_opt = 1              # indique si l'export en Excel a été choisi lors de la dernière exécution. 0 ou 1.
output_name = isogeo2xlsx    # nom du fichier de sortie

[word]
word_opt = 1                       # indique si l'export en Word a été choisi lors de la dernière exécution. 0 ou 1.
out_prefix = isogeo2docx      # préfixe du nom de fichier de sortie
tpl = template_Isogeo.docx    # chemin (relatif ou absolu) du dernier modèle choisi
opt_id = 0                    # nombre de caractères de l'identifiant unique Isogeo inclus. De 0 à 8.
opt_date = 1                  # type de date à inclure dans le nom du fichier exporté. 0, 1 ou 2.

[xml]
xml_opt = 1                    # indique si l'export en XML a été choisi lors de la dernière exécution. 0 ou 1.
out_prefix = isogeo2xml    # préfixe du nom de fichier de sortie
opt_id = 0                 # nombre de caractères de l'identifiant unique Isogeo inclus. De 0 à 8.
opt_date = 1               # type de date à inclure dans le nom du fichier exporté. 0, 1 ou 2.
```



