# Droid4Linux

But: afficher sur un écran externe les infos Now Playing des apps Android TV (Netflix, Prime Video, myCanal, etc.).
L'app écoute MediaSession, calcule le temps restant, expose `/now.json` et `/now.png` via un mini-serveur HTTP.

## Build sans Android Studio
- Pousse ce dossier sur GitHub.
- Le workflow `.github/workflows/build.yml` génère l'APK debug en artifact.

## Installation
1. Active Options développeur + sources inconnues.
2. Installe l'APK (sideload).
3. Ouvre l'app, accorde l'**accès aux notifications**.
4. Démarre le service HTTP. Ouvre `http://<IP_BOX>:8787/now.png` sur l'écran externe.

## Notes
- Le numéro et le nom d'épisode dépendent de ce que l'app publie.
- HTTP non chiffré sur LAN seulement.
