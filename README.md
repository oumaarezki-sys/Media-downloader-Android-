# Media Downloader Android

Port Android de [mhogomchungu/media-downloader](https://github.com/mhogomchungu/media-downloader) : interface native (Kotlin, Jetpack Compose, Material 3) pour yt-dlp, FFmpeg et aria2c via [youtubedl-android](https://github.com/yausername/youtubedl-android) 0.18.1.

## Fonctions

- File de téléchargements : collage de liens, import depuis un fichier texte, partage depuis un navigateur ou une app, téléchargements simultanés
- Playlist : chargement de la liste, sélection par cases ou par plage, ajout à la file
- Abonnements : suivi de playlists/chaînes, détection et téléchargement des nouveautés
- Choix du format (liste yt-dlp vidéo/audio) et préréglages : Meilleure, 2160p à 360p, MP3, M4A, Opus, FLAC, WAV, AAC, plus préréglages personnalisés (options yt-dlp)
- Réglages : Wi-Fi seulement, aria2c, fragments, limite de débit, proxy, cookies.txt, sous-titres, miniature, métadonnées, SponsorBlock, modèle de nom, options yt-dlp libres
- Service au premier plan, notifications, historique (Room), journal par téléchargement
- Destination : dossier choisi (SAF) ou Téléchargements/MediaDownloader
- Mise à jour de yt-dlp (stable, nightly, master), automatique une fois par jour
- FR / EN / AR, thème clair, sombre ou dynamique

## Compiler

JDK 17. Android Studio : ouvrir le dossier puis Run. En ligne de commande :

    ./gradlew assembleDebug

APK dans `app/build/outputs/apk/debug/` (un APK par ABI + universel). Le workflow `.github/workflows/build.yml` produit aussi les APK sur GitHub Actions.

## Limites

- Seul yt-dlp est embarqué (pas gallery-dl, youtube-dl, lux, you-get, svtplay-dl, wget, safari books).
- Dépend du fonctionnement de youtubedl-android et des sites ciblés : mettre yt-dlp à jour en cas d'échec d'extraction.

## Licence

Dépend de youtubedl-android (GPL-3.0) : toute distribution de l'APK impose de publier le code source sous GPL-3.0 compatible. Code écrit de zéro, sans reprise du code Qt/C++ de l'original (GPL-2.0+). À utiliser dans le respect du droit d'auteur et des conditions des sites utilisés.
