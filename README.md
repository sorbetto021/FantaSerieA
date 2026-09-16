# Fantacalcio Live – prima versione Android

Progetto Android Studio in Kotlin + Jetpack Compose.

## Funzioni incluse
- UI iniziale per lega fantacalcio
- gestione stato importazione lega
- elenco eventi: gol, assist, ammonizioni (modello estendibile a autogol, espulsioni, rigori, rigori sbagliati)
- associazione evento a squadra fantacalcio quando disponibile
- richiesta permesso notifiche Android 13+
- canale notifiche
- struttura pronta per collegare un connettore dati live

## Importante sul live
Questa build NON contiene un accesso reale a Fantaleghe.it o a un provider live di Serie A. Per implementare notifiche reali serve una fonte dati autorizzata/compatibile (API, feed o altro metodo consentito). Il progetto è volutamente compilabile anche senza tale fonte.

## Apertura
Aprire la cartella `FantacalcioLive` in Android Studio e attendere la sincronizzazione Gradle.

## APK debug
Da Android Studio: Build > Build APK(s). L'APK sarà nella cartella `app/build/outputs/apk/debug/`.

Oppure terminale: `./gradlew assembleDebug` (Windows: `gradlew.bat assembleDebug`).

## Compilazione online con GitHub Actions

1. Crea un repository GitHub vuoto.
2. Carica tutti i file di questo progetto nel repository.
3. Apri la scheda **Actions**.
4. Seleziona **Build Android APK**.
5. Premi **Run workflow**.
6. Al termine apri la build completata.
7. Nella sezione **Artifacts** scarica `FantacalcioLive-debug-apk`.
8. Estrai lo ZIP dell'artifact e troverai `app-debug.apk`.

Il workflow compila una versione **debug** dell'app. Per pubblicazione sul Play Store o distribuzione come APK firmato serve successivamente configurare una chiave di firma.
