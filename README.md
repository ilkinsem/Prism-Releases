# Prism — APK (Android)

Gestionnaire documentaire **local-first** : import, lecture PDF, dossiers, scan du téléphone,
OCR on-device, opérations PDF non destructives et assistant local sourcé. Sans compte et sans
cloud IA par défaut.

## Télécharger

**[Prism v0.0.4 — APK debug](https://github.com/ilkinsem/Prism-Releases/releases/download/v0.0.4/app-debug.apk)**

- Android 8.0+ (`minSdk 26`), cible Android 15 (`targetSdk 35`).
- APK signé debug, à installer en sideload (autoriser les sources inconnues).
- Taille : ~70 Mo. SHA-256 : `373307338bde8d2e9e7c127fc6b908403aac4d9d209aec39f21d07ebe9459f5b`.

Le dépôt de code source est **privé**. Ce dépôt public ne contient que les APK et leurs notes.

## Nouveautés v0.0.4

- **Splash** : fond dégradé sombre, logo Prism, nom, tagline et indicateur de chargement.
- **Accueil** : logo, « Bonjour ! » / « Que souhaitez-vous faire ? », vignettes d'actions avec
  pictogrammes outlined et fonds tonaux.
- **Scanner** : viseur haut (≈58 % de l'écran), repères de cadrage, obturateur, galerie et modes
  Document/Carte/Photo.
- **Retour Accueil corrigé** après « Mes dossiers ».
- **Accueil documents** : swipe ou « … » pour ouvrir, favori, partager, corbeille.
- Rappel v0.0.3 : mises à jour au démarrage/manuel, champs sans contour.
- Rappel v0.0.2 : scan du téléphone, gestes Documents.

## Nouveautés v0.0.3

- **Mises à jour** : vérification au démarrage, au retour au premier plan après 6 h, et manuelle
  dans Réglages. Bandeau non modal + téléchargement de l'APK via le navigateur.
  Requête HTTPS vers GitHub Releases, sans identifiant ni contenu documentaire.
- **Champs et filtres sans contour** : fonds distincts en clair/sombre, plus aucune bordure.

## Inclus

- Accueil, Documents, Scanner, Assistant, Réglages — **FR/EN**.
- Design Prism, thèmes clair/sombre, panneaux adaptatifs sans modale applicative.
- Import SAF, dossiers/sous-dossiers, favoris, récents, corbeille, tags, recherche nom/contenu,
  doublons SHA-256.
- Lecteur PDF : zoom, miniatures, texte, recherche, rotation, extraction/suppression, division.
  Chaque transformation crée un nouveau document ; l'original reste intact.
- Scanner CameraX + PDF multipage + OCR ML Kit.
- Assistant extractif sourcé (résumé, Q/R citées, extraction dates/montants/e-mails/références),
  multi-documents, historique et purge.
- Abstraction LLM : moteur embarqué par défaut ; Ollama/LM Studio debug-only, opt-in, hôtes privés.
- Prism est déclarée comme lectrice de PDF (`ACTION_VIEW` + `application/pdf`).

## Limites assumées

DOCX→PDF (moteur de rendu non embarqué), LFM3/llama.cpp natif Android, mesure OCR CER/WER,
Google Drive, signature cryptographique, caviardisation réelle, sync et performances sur appareil
physique. L'option « tous les fichiers » est avancée et doit être évaluée vis-à-vis des règles
Google Play avant une distribution publique.

## Vérifications

- E2E Compose : 7/7 (navigation, lecteur, dossiers, assistant, recherche, purge, swipe, scan).
- Vérification réelle des mises à jour contre l'API GitHub Releases.
- Couverture : domaine 91,8 %, core common 85,1 %.
- Build, installation et lancement vérifiés sur émulateur API 35.

![Accueil v0.0.4](docs/home-v040.png)
![Scanner v0.0.4](docs/scanner-v040.png)
![Accueil](docs/home-fr.png)
![Bandeau de mise à jour](docs/update-banner.png)
![Réglages des mises à jour](docs/settings-update.png)
![Champs sans contour](docs/fields-light.png)
![Scan du téléphone](docs/scan-phone-en.png)

Nom « Prism » provisoire. Version 0.0.4.
