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
| Swipe down | Pulse: breaks glitch bots and cracked crates in your lane |
| Hold | Hush: Milo freezes and dims his lights, so sensors miss him |
| Tap | Walk (first and last level), brighten Milo's light in the dark, choose in menus |
| Back button | Pause / go back |

## What is in the game

- **Juno Vale:** the main character, Pip's fastest courier (short natural coily hair, denim vest over a black crop top, frayed denim shorts, olive backpack, chunky sneakers). She rides an electric scooter through the runs with Milo in the crate on the back; Settings → Runner switches back to Milo on foot. In the Heart (chapter 6) Milo goes on alone.
- **Poster art:** painted sunset posters for the title, level cards, chapter cards and results.

- **Glitch bots:** broken scrap robots roll toward Milo from level 5 on. Swipe down to fire a pulse and break them, jump over them, or dodge. Armoured ones (orange frame) need two pulses. Crates with a cyan crack break too. Break several within 3 seconds for a combo (more bolts each time).
- **Power-ups:** shield (blocks one hit), bolt magnet (pulls in bolts from every lane for 8 seconds), rocket skates (3 seconds of speed: smash through everything, fly over holes).
- **Night Shift:** an endless mode on the city map (unlocks after level 5). The city changes every day, speed keeps rising, every checkpoint adds 10 seconds, and three hits end the shift. Score = distance + bolts + breaks; your best and today's best are saved, and the bolts you earn go to the Repair Shop.

- **Look:** sunset-and-neon city style: pink-to-orange skies, a striped retro sun, palm trees, pastel art-deco buildings with neon trims, bold slanted mission titles.
- **Countdown:** every delivery run and puzzle has a time limit (shown at the top). Pink clock pickups add 4 seconds, reboots cost time, and time left turns into bonus bolts. If the clock hits 0:00 the delivery fails and you try again. Levels 1, 56, 58 and 60 have no clock.

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
