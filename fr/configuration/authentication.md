# Configuration via l'interface graphique

## Authentification {#authentication}

Au premier lancement de l'application ou si l'authentification a échoué (paramètres expirés...), le formulaire d'authentification s'affiche :

!["Formulaire d'authentification d'Isogeo to Office à l'API Isogeo"](/assets/i2o_auth_form.png)

### Authentifier l'application

1. Cliquer sur le bouton `Importer le fichier "client_secrets.json" transmis..."
2. Sélectionner le fichier téléchargé (il est possible de changer le filtre sur le type de fichier) :

    !["Sélectionner le fichier d'authentification dans Windows"](/assets/i2o_auth_credentials_picker.png)

3. Si l'authentification est bonne, cliquer sur le bouton `Appliquer`. Si elle n'est pas bonne, [demander un accès](#auth-request).
4. Après une première requête, les informations de l'application sont mises à jour dans l'onglet `Paramètres`:

!["Informations sur l\'application"](/assets/i2o_settings_authentication_info.png)

---

### Changer les clés d'authentification {#change}

Dans les paramètres, il est également possible de changer les paramètres d'authentification.

---

## Demander un accès {#auth-request}

Si l'utilisateur ne dispose pas de clés d'authentification, il peut en faire la demande en cliquant sur le bouton `Demander un accès` ou directement sur [le formulaire en ligne](https://pipedrivewebforms.com/form/427397f21f1417e5b937b673dfa12c9052944).


A tout moment, l'utilisateur peut entrer de nouvelles clés en cliquant sur le bouton `Accès`.
