# DERAILED — The Northstar Quest (Free browser version)

This is an original low-poly 3D prototype, not Nintendo's game or a realistic Ryan Gosling likeness. It is NOT published yet.

## One-time setup (free tiers)

1. Visit https://console.firebase.google.com and create a Firebase project on the Spark (free) plan.
2. Under Build > Authentication > Sign-in method, enable Anonymous.
3. Under Build > Realtime Database, create a database in locked mode (not Cloud Firestore).
4. Under Realtime Database > Rules, paste the full contents of `database.rules.json`, then Publish.
5. Under Project settings > Your apps, register a Web app. Copy its config values to `firebase-config.js`. Add the exact `databaseURL` from Realtime Database > Data. Replace every `PASTE_...` value.
6. At https://github.com, create a new public repository named `northstar-quest`.
7. Upload `index.html`, `controller.html`, `firebase-config.js`, and `database.rules.json` to the repository root and commit.
8. Go to repository Settings > Pages > Deploy from a branch > main > /(root) > Save.
9. Open the published GitHub Pages link in Chrome on the projector. The QR code will link to the phone controller for that room.

## Playing

- Open the GitHub Pages game URL on the projector. It adds a random `?room=...` identifier.
- Three volunteers scan the QR code, enter names, and receive Northstar, Weststar, and Southstar missions.
- Press Start. Their directional inputs combine, so conflicting commands can cancel.
- Press Northstar only for the reveal. Pause and Reset are available.
- To start a fresh room, open the game URL without `?room=...`. Keep the projector page open while playing.
- Reset does not remove joined players. For new volunteers, start a new room.

## Notes

- Phones can use mobile data or Wi-Fi, as long as they have internet.
- This needs internet for Firebase and the Three.js/QRCode libraries.
- Free plans have usage limits; review them before the event.
- If you see a setup error, check databaseURL, Anonymous Auth, database rules, and config.
- This is a lightweight sermon demo, not a security-hardened public game. Test with three phones beforehand.
