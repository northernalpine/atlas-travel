ATLAS TRAVEL — iPHONE WORKOUT LOGGER (Track B prototype)

WHAT IS INCLUDED
- index.html: self-contained, full Track A v4 program embedded; no live network requests.
- sw.js, manifest.webmanifest, icon.svg: offline-capable install assets.
- track_a_v4.json: authoritative unmodified program source.

RECOMMENDED IPHONE SETUP
1. Upload the contents of this folder to an HTTPS static host (such as GitHub Pages or Netlify). Do not host sensitive training logs; the site itself contains only the program prescription.
2. Open the hosted URL in iPhone Safari while online. Use Share > Add to Home Screen. Open ATLAS from the Home Screen at least once while online so the page and offline cache initialize.
3. Choose the workout date, tap BEGIN WORKOUT, enter actual load/reps/seconds/RIR, then tap MARK SET COMPLETE. Changes save immediately to storage on that iPhone.
4. For outdoor riding, tap OUTDOOR RIDE: this creates a saved transition checkpoint. Leave the phone, then return and choose RESUME / REVIEW. Enter ride data, tap SAVE CARDIO ENTRY, tap REVIEW & FINISH, then CONFIRM FINISH & SAVE.
5. On completion review the workout summary. Use DATA / BACKUP to Export all workouts JSON daily. Save to Files/iCloud Drive or share with yourself. CSV is a companion per-set export.
6. After traveling, import/export these data to the Pi using a separate DB-specific mapping tool. These files DO NOT directly overwrite the Raspberry Pi SQLite DB.

IMPORTANT
- This build is browser-local, not synced across devices. Back up data after every workout. Safari Private Browsing and storage clearing can lose records.
- This is a working prototype and has not been tested on a physical iPhone or your Pi. Test one dummy session, reload, export, restore before traveling.
- To avoid a stale app version on a hosting service, update the service worker cache name when deploying a revised build.
- Starting and finishing store real timestamps; elapsed timer uses those timestamps even after app suspend.
- The cardio entry is manual; Suunto automatic matching is deferred to the home Track B build.
