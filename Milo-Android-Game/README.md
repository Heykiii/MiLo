# Little Delivery Robot: The Last Message

A portrait, one-thumb Android game. Milo-07, a tiny delivery robot, carries a package with no sender across the city of Aurelia over 60 levels in 6 chapters.

## How to get the APK (no Android Studio needed)

GitHub builds the APK for you every time you upload or change a file.

1. Create a new repository on GitHub (it can be private).
2. Upload **all** files from this folder, keeping the folders exactly as they are.
   - Easiest: unzip, open the repository page, click **Add file → Upload files**, and drag in everything inside the unzipped folder.
   - The folder `.github` starts with a dot, so your computer may hide it. If it does not upload, create the file by hand: **Add file → Create new file**, type the name `.github/workflows/build.yml`, and paste the contents of that file.
3. Open the **Actions** tab. A run called **Build APK** starts by itself and takes about 3–5 minutes.
4. When it shows a green tick, download the APK:
   - **Releases** (right side of the repository page): `Milo-The-Last-Message.apk`, easiest from your phone.
   - Or **Actions → the run → Artifacts** (this download is a zip with the APK inside).
5. On the phone, open the APK and allow "install from unknown sources" when Android asks.

## Controls

| Gesture | Action |
| --- | --- |
| Swipe left / right | Change lane |
| Swipe up | Jump |
| Hold | Hush: Milo freezes and dims his lights, so sensors miss him |
| Tap | Walk (first and last level), brighten Milo's light in the dark, choose in menus |
| Back button | Pause / go back |

## What is in the game

- 60 levels: 52 delivery runs (4 of them end in a puzzle) and 8 puzzle levels: window patterns, switch order, memory tiles, city-model lights, notebook questions and the Choice.
- Hazards: puddles, crates, low bars and lasers, gaps, crumbling floors, cars and drones, sensor sweeps, lightning and sparks, wind, signal forks, chases.
- Memory Fragments (3 per level), Postcards, Bolts, 12 kindness stamps that change later levels and the ending, a detective notebook, Pip's Repair Shop upgrades, chapter memories and the full ending.
- All graphics are drawn in code and all sounds are synthesized, so there are no image or sound files to manage.
- Progress saves automatically on the phone.

## Files

| File | What it is |
| --- | --- |
| `app/src/main/assets/index.html` | The whole game (HTML5 canvas + JavaScript) |
| `app/src/main/java/com/milo/lastmessage/MainActivity.java` | Opens the game full screen |
| `app/src/main/AndroidManifest.xml` | App settings (portrait, full screen) |
| `app/src/main/res/drawable/ic_launcher.xml` | App icon (Milo's face) |
| `.github/workflows/build.yml` | Tells GitHub how to build the APK |
| `build.gradle`, `settings.gradle`, `gradle.properties`, `app/build.gradle` | Android build settings |

You can also test the game on a computer: open `app/src/main/assets/index.html` in Chrome. Arrow keys move, Space taps, H holds.

## Notes

- The APK is a debug build: fine for your own phone and for sharing with testers, not for the Play Store. Publishing needs a signed release build.
- To change the app name, edit `app/src/main/res/values/strings.xml`.
