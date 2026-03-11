# GZCLP RPG Tracker

A single-file mobile-friendly GZCLP tracker (`gzclp.html`) with local persistence, streaks, XP, and backup import/export.

## Quick start (phone, single-file mode)

If you want to **just download one HTML file and use it on your phone**:

1. Copy `gzclp.html` to your phone.
2. Open it in a mobile browser (Chrome/Safari/Edge).
3. Use the app normally.

### Important notes for single-file mode

- Data is saved in browser storage (`localStorage`) on that device/browser profile.
- If you clear browser site data, uninstall the browser, or switch browsers/devices, data may be lost.
- In `file://` mode, service workers/PWA install flow are not used (this is expected).
- The app now safely handles missing icon CDN loads so core tracking still works even if icon assets fail.

## Recommended mode (best phone app-like behavior)

For better install/offline behavior, host the files with a web server and open via `http://` or `https://`:

- `gzclp.html`
- `manifest.webmanifest`
- `service-worker.js`

Then use your browser's **Add to Home Screen** option.

## Backup and restore

In **Armory → Backups**:

- **Export JSON** creates a backup file with config + sessions.
- **Import JSON** restores from that backup format.

Tip: export weekly or after important PR sessions.

## Data reset behavior

"Purge Character Progress" only removes this app's keys (`gzclp_*`) from localStorage.
