# Changelog

Versions mises en ligne de rachatourets.com, de la plus récente à la plus ancienne. Chaque version correspond à un tag git du même nom (voir le [README](README.md)).

## v2026.10.31 — 31/10/2026

### Corrigé
- Affichage mobile : balise viewport réparée, carte de l'Europe adaptée à la largeur de l'écran
- Formulaire : redirection en HTTPS après envoi, remplissage automatique (nom, e-mail, téléphone), contrôle du format du téléphone
- Coquilles (« vous rediriger », phrase sans sujet, encadré « À noter » reformulé)
- Blocs « Comment ça se passe ? » et « Pourquoi… » de nouveau centrés sur grands écrans

### Ajouté
- Bouton d'appel dans l'en-tête et numéro cliquable dans l'encadré d'information
- Référencement : nouveau titre et description, balises Open Graph, données structurées (LocalBusiness)
- Accessibilité : balise `main`, icônes décoratives ignorées par les lecteurs d'écran
- Outillage : aperçu local avec browser-sync (`npm run dev`, `npm run preview`)

### Modifié
- Titre principal : « Rachat et revalorisation de tourets bois, contreplaqué et PVC »
- Espagne ajoutée dans l'accroche ; adresse de contact unique `contact@rachatourets.com`
- Titres de section unifiés ; titres, pastilles et encadrés alignés à gauche sur mobile et tablette
- Tailles de texte : accroche réduite sur mobile, boutons réduits, texte d'aide du formulaire agrandi
- Séparateur entre la carte et la zone de contact
- Carte en fichier SVG externe

## v2026.04 — 30/04/2026
- Ajustement du numéro de téléphone

## v2024.08 — 26/08/2024
- Nouveaux numéros de téléphone sur tout le site
- Espagne ajoutée à la liste des zones d'intervention

## v2023.11 — 05/11/2023
- Évolutions 2023 du contenu et du formulaire
- Mises à jour de dépendances (Dependabot)

## v2022.02 — 22/02/2022
- Refonte : bouton « Contactez-nous » et ajustements de mise en page

## v2021.06 — 13/06/2021
- Version 2 du site ; feuille de style appelée avec un paramètre de version (contournement du cache)

## v2020.03 — 11/03/2020
- Première version du site (design V1)
- Formulaire de contact testé ; images en JPG (WebP non pris en charge par Safari à l'époque)
