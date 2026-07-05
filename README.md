# Inspection Camera 📷

A home-inspection photo app: take a picture, speak a note, and it's automatically
filed under **Defects** or **General Photos** based on what you say.

## How to install on your iPhone

The app must be reachable over the internet (HTTPS) for the camera to work.
Once it's hosted at a link:

1. Open the link in **Safari** on your iPhone.
2. Tap the **Share** button (square with arrow).
3. Tap **"Add to Home Screen"** → **Add**.
4. Open **Inspect** from your home screen like any other app.
5. First launch: allow **Camera** and **Microphone** when asked.

After that it works offline — no internet needed during an inspection.

## How to use

- **Take a photo** with the big shutter button. Pinch (or use −/+) to zoom.
- The app immediately **starts listening**. Say:
  - *"Defect, HVAC not cooling properly"* → filed under Defects
  - *"General picture, guest bedroom 1"* → filed under General
  - The keyword is stripped, so the note saved is just "HVAC not cooling properly".
- You can also type the note or fix the transcription, and tap the
  red/blue buttons to override the category.
- **Photos** button → gallery with Defects / General tabs. Tap any photo to
  view it full screen (pinch to zoom), edit its note, move it, share, or delete.
- **Export All** → creates one ZIP with a `Defects/` folder, a
  `General Photos/` folder (each photo named after its note), and a
  `report.txt` listing everything. It opens the iOS share sheet so you can
  save to Files, AirDrop to your computer, or email it.
- **New Inspection** wipes all photos (export first!).

All photos stay on your phone (stored in the app's local database).
Nothing is uploaded anywhere.

## Files

- `index.html` — the whole app (UI + logic)
- `manifest.webmanifest` — makes it installable as a home-screen app
- `sw.js` — service worker (offline support)
- `icon-180.png` / `icon-512.png` — app icons
