# DinoServer 1.2.19 FRIEND TEST

Give this same ZIP to both testers. Each tester extracts their own copy on their
own Windows PC. No account credentials, saved parks or developer device links
are included. This is a friend-testing build, not a production update ZIP.

## Quick setup

1. Extract the entire ZIP into a NEW folder, for example
   `C:\Games\DinoServer-1.2.19-Friend-Test`. Keep the old server and saves intact.
   Stop any other DinoServer before running `DinoServer/DinoServer.exe` here.
   This package includes its Python runtime; no Python or Termux install is needed.
2. Open Cache Delivery. Download & Install Android Cache for Android/LDPlayer,
   or Download & Install iOS Cache for iPad/iPhone. Wait for verification to finish.
   You may instead copy only the matching cache folder from your existing server
   into this package's `DinoServer/server/cache_android` or `cache_ios`.
3. Android testers: the corrected GAME APK is in `Game`. Install it over your
   compatible SDK26-signed JPB game to test immediate card-pack debit. It is not
   the mobile server/controller app. Keep game data. If Android reports a signing
   conflict, keep the old app and resolve the installation separately; do not
   uninstall or erase an existing park just to force installation. This is a
   32-bit ARM game and requires ARM compatibility (LDPlayer supports translation).
   iOS testers keep their existing JPB installation; an APK does not install on iOS.
4. On Overview, select iOS or Android / Emulator to match the device. Configure
   the device's JPB routing to THIS tester's PC LAN IP displayed by DinoServer.
   The ZIP has no fixed IP. Device and PC must be able to reach each other.
   If Windows blocks incoming traffic, close JPB and use the supplied
   `DinoServer/server/OPEN_LAN_FIREWALL.bat` as administrator for the server rules;
   detailed troubleshooting is in `DinoServer/docs/WINDOWS-INSTRUCTIONS.md`.
5. Start the server and open JPB using Play as guest. Complete the date-of-birth
   screen yourself if shown. Let the native game create and save its actual park.
   **Do not import the old demo preload or a real guest save into this test.**
6. Once the park is visible and saved, fully close JPB and reopen it as a guest.
   This next login applies **100,000 Bucks and 1,000,000 XP (displayed level 30)**
   once. The stored level field is 29 because the game displays it as level 30.
   If still waiting for the initial park save, let it finish and reconnect again.
   Future logins keep your earned/spent balance and progress; they do not refill.

## Cross-save test (optional)

Use one tester's server folder for both of that tester's devices. Try guest login
once on the second device, then close both games and stop the server. In Guest
Saves > Cross-save / linked devices, select the waiting device and the existing
test park. Confirm Link device. Install both caches and select the appropriate
platform on Overview before starting the server for that device. One device can
play the park at a time. The shared park gets one allowance total, not another
100,000 Bucks per device. Full instructions: `DinoServer/docs/CROSS-SAVE.md`.

## Notes

- Automatic updates are disabled and the launcher is labelled FRIEND TEST.
- Test credit is restricted to parks newly created by this test server. Importing
  an existing park does not qualify it for an allowance.
- Caches are separate downloads to keep this ZIP small. Cache download/install
  does not start the server. No personal saves, bindings, locks or signing keys ship.
- Existing mobile controller mail/portrait issues remain pending. This ZIP does
  not contain a new mobile controller APK or a patched iOS game.
- Keep this folder separate from your production installation and back up the
  test park before save/import tests. Never upload the test ZIP to the updater.
