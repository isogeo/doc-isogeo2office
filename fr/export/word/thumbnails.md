# Gestion des vignettes

Depuis la version 2.0.0 de l'application, il est possible d'intégrer des vignettes dans les exports Word en établissant une correspondance entre une image et une métadonnée.

## Fonctionnement global {#description}

Un fichier Excel sert de table de correspondance entre des images stockées localement (sur l'ordinateur de l'utilisateur donc) et les métadonnées, sur la base de leurs identifiants uniques.

Lors de l'export en Word :

1. la table de correspondance est parcourue
2. en cas de correspondance, le chemin vers l'image est testé
3. si l'image est atteignable en lecture par l'application, elle est ajoutée dans le fichier Word en lieu et place de la variable `varThumbnail`
4. sinon, c'est le logo Isogeo qui est inséré.

## Marche à suivre

### Générer la table de correspondance {#update}

Avant toute chose, s'assurer d'avoir fermé le fichier Excel.

1. Dans l'onglet `Paramètres`, ouvrir la partie `Word` et cliquer sur le bouton `Générer/mettre à jour`.
2. Les métadonnées sont récupérées auprès d'Isogeo
3. Les métadonnées sont stockées dans le fichier Excel dédié dans le dossier de l'application (`thumbnails\thumbnails.xlsx`)

### Compléter la table de correspondance {#complete}

1. Dans l'onglet `Paramètres`, ouvrir la partie `Word` et cliquer sur le bouton `Editer la table de correspondance`.
2. Compléter la colonne 3 avec les chemins absolus vers les images

![Fichier Excel de correspondance des vignettes](/assets/i2o_word_thumbnails_table.png)

#### Précautions

Attention à ne pas :

- changer le nom de l'onglet (_i2o_thumbnails_)
- changer le nom des colonnes

----

## Questions fréquentes {#faq}

### Je ne veux pas d'image dans mes exports {#no-image}

Il suffit de [retirer la balise _varThumbnail_ dans le modèle d'export](/export/word/template.md).
