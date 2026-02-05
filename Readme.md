[![Translation status](https://vianneypacaud.fr/img/VIANNEYPACAUDBANIERE.svg)](https://vianneypacaud.fr/)

# Extraction du texte d'une image via OCR

Ce dépôt contient le code source d'une application web interactive permettant d'éxtraire le texte d'une image'. L'application est accessible via [**ocr.gervo.fr**](https://ocr.gervo.fr).

## Structure du projet
- `index.html` : Fichier unique contenant la structure HTML5, les styles Tailwind CSS et la logique applicative.

- `Tesseract.js` : Bibliothèque de moteur OCR (chargée via CDN) utilisée pour le traitement des images dans le navigateur.

- `Lucide Icons` : Bibliothèque d'icônes utilisée pour l'interface utilisateur.

- `Tailwind CSS` : Framework utilitaire pour un rendu visuel moderne, épuré et responsive.

## Fonctionnalités principales

- **Extraction de texte locale** : Analyse des images directement dans le navigateur sans aucun envoi de données vers un serveur externe.

- **Aperçu interactif** : Une fois l'analyse terminée, l'utilisateur peut survoler et cliquer directement sur les mots dans l'image pour les copier individuellement.

- **Support multi-langues** : Possibilité de choisir entre plusieurs langues (Français, Anglais, Espagnol, Allemand) pour optimiser la précision de la détection.

- **Éditeur de texte intégré** : Le résultat de l'extraction est affiché dans une zone éditable permettant de corriger ou de mettre en forme le texte avant de le copier.

- **Interface Responsive** : Design optimisé pour une utilisation fluide sur ordinateur, tablette et smartphone.

## Installation et utilisation

1. **Prérequis** :
   - Un navigateur web moderne.
   - Un serveur web Apache (optionnel, mais recommandé pour utiliser les règles du fichier `.htaccess`).

2. **Lancement** :
   - Clonez le dépôt ou téléchargez les fichiers.
   - Ouvrez directement le fichier `index.html` dans votre navigateur ou placez le dossier sur votre serveur.

## Points techniques

- **Confidentialité et RGPD** : Le site fonctionne exclusivement côté client (dans le navigateur). Aucune donnée saisie (URL, logos) n'est transmise ou stockée sur un serveur.
- **Moteur OCR** : Utilisation de Tesseract.js, un portage JavaScript du célèbre moteur OCR de Google, permettant une reconnaissance puissante sans dépendances serveur (Node.js/Python).

- **Performance** : Le traitement utilise les Web Workers pour ne pas bloquer l'interface utilisateur pendant les calculs intensifs de reconnaissance de texte.

## Personnalisation
Le comportement du moteur (langues par défaut, logger de progression) et l'apparence visuelle peuvent être ajustés directement dans la balise `<script>` du fichier `index.html`.

## Auteur

Projet développé par **Vianney Pacaud** (Vianney Conception).

---

**Licence :** Ce projet est Open Source. La reproduction totale ou partielle est autorisée.
