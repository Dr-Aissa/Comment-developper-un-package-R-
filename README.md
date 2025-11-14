# Guide rapide pour créer un package R

Créer un package R permet d’organiser, réutiliser et partager ton code et tes données de manière professionnelle.

## 1. Créer la structure de base

Créer un dossier pour le package : nom_du_package/.

Utiliser :

usethis::create_package("nom_du_package")

## 2. Organiser les fichiers

R/ : scripts avec les fonctions.

man/ : documentation des fonctions (auto-générée).

DESCRIPTION : informations sur le package (nom, version, auteur, dépendances).

NAMESPACE : définit les fonctions exportées.

data/ (optionnel) : datasets intégrés.

## 3. Écrire et documenter les fonctions

Chaque fonction dans un fichier .R.

Documenter avec roxygen2 :

#' Titre
#'
#' Description
#' @param x Description de l’argument
#' @return Description de la sortie
#' @export
ma_fonction <- function(x) { x + 1 }

## 4. Générer la documentation

devtools::document() → crée automatiquement les fichiers .Rd dans man/.

## 5. Tester et développer

Charger le package en dev : devtools::load_all().

Tester toutes les fonctions.

## 6. Vérifier et construire

Vérification : devtools::check().

Construction : devtools::build().

7. Versionner et partager

Initialiser un dépôt Git et .gitignore.

Publier sur GitHub pour partage et suivi des versions.
