# Galla Cash Book – phone app

Your cash book is now an installable app. Same Firebase, same data, same logins and passcodes. Nothing to restore.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The app (your Firebase config is already inside) |
| `manifest.webmanifest` | App name, colour and icon, so phones can install it |
| `sw.js` | Lets the app open without internet |
| `icon-192.png`, `icon-512.png`, `maskable-512.png`, `apple-touch-icon.png` | The ₹ app icon in all sizes |

## 1. Upload to GitHub (replaces the old version)

1. Open your `galla` repository on GitHub.
2. **Add file → Upload files**. Select all 8 files from this folder together and drop them in.
3. Tap **Commit changes**. After a minute the app is live at your usual link:
   `https://mahendra41098.github.io/galla/`
4. If you previously uploaded the app as `galla.html`, open the new link above (`/galla/`), not `/galla/galla.html`.

All files sit side by side; there are no folders.

## 2. Install on each phone

**Android (Chrome):** open the link → tap **Install app** at the top (or ⋮ menu → **Install app**). The ₹ Galla icon appears on the home screen.

**iPhone (Safari only):** open the link → **Share** → **Add to Home Screen** → **Add**.

Open it once with internet on each phone. After that it opens even without internet; entries save on the phone and sync when the internet is back.

## 3. Updating the app later

When you change `index.html`, also open `sw.js` and change `galla-v1` to `galla-v2` (then v3, and so on), and upload both. Every phone picks up the new version the next time it opens the app.

## Optional: a real Android .apk file

If you want an .apk to share on WhatsApp (instead of installing from the link):

1. Go to **https://www.pwabuilder.com** and paste `https://mahendra41098.github.io/galla/`.
2. Tap **Package for stores → Android → Generate package** (free).
3. Download the zip. Inside, install the `.apk` file on each phone (allow "Install unknown apps" once).

The .apk just opens your GitHub link full screen, so updates you upload to GitHub still reach everyone automatically. Keep the `signing.keystore` file and its passwords from that zip safe: you need them to make a newer .apk later, or to put it on the Play Store (₹2,000 one-time Google developer fee).

## Good to know

- **Same data everywhere:** the old link, the installed app and the .apk all read the same Firebase books.
- **Logins stay** on each phone until someone taps **Log out**.
- **Backup:** Settings → Backup → **Download backup**, once a week.
