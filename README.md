# Prism — APK (Android)

Gestionnaire documentaire **local-first** : import, lecture PDF, dossiers, scan du téléphone,
OCR on-device, opérations PDF non destructives et assistant local sourcé. Sans compte et sans
cloud IA par défaut.

## Télécharger

**[Prism v0.0.3 — APK debug](https://github.com/ilkinsem/Prism-Releases/releases/download/v0.0.3/app-debug.apk)**

- Android 8.0+ (`minSdk 26`), cible Android 15 (`targetSdk 35`).
- APK signé debug, à installer en sideload (autoriser les sources inconnues).
- Taille : ~71 Mo. SHA-256 : `c9f408ee0e581121a46266bb803c9f3af4d4198f730e939c1d08277c8b5ad6d2`.

Le dépôt de code source est **privé**. Ce dépôt public ne contient que les APK et leurs notes.

## Nouveautés v0.0.3

- **Mises à jour** : vérification au démarrage, au retour au premier plan après 6 h, et manuelle
  dans Réglages. Bandeau non modal + téléchargement de l'APK via le navigateur.
  Requête HTTPS vers GitHub Releases, sans identifiant ni contenu documentaire.
- **Champs et filtres sans contour** : fonds distincts en clair/sombre, plus aucune bordure.
- **Scanner le téléphone** (v0.0.2) : dossier SAF ou option « tous les fichiers » consentie.
- **Gestes Documents** (v0.0.2) : swipe ou « … » pour corbeille et couper/déplacer.
- Correction du libellé « Documents » et validation du nom de dossier.
- Démarrage allégé (initialisation paresseuse PDFBox/ML Kit).

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

![Accueil](docs/home-fr.png)
![Bandeau de mise à jour](docs/update-banner.png)
![Réglages des mises à jour](docs/settings-update.png)
![Champs sans contour](docs/fields-light.png)
![Scan du téléphone](docs/scan-phone-en.png)

Nom « Prism » provisoire. Version 0.0.3.
