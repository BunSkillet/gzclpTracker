# GZCLP RPG Tracker

A phone-first GZCLP workout tracker.

## Single-file mode (primary workflow)

If you want the simplest setup, only use:

- `gzclp.html`

### Steps

1. Download/copy `gzclp.html` to your phone.
2. Open it directly from your Files app in your mobile browser.
3. (Optional) Add a browser shortcut to your home screen.

### What works in single-file mode

- Full training flow (summary, workout logging, history, settings)
- Local save via browser `localStorage`
- Export/import JSON backups from Armory
- Works even if icon CDN fails (icons may disappear, app still functions)

### Single-file limitations

- Data is tied to that browser profile/device.
- Clearing site data, reinstalling browser, or changing device can remove history.
- `file://` pages do not use service worker install/caching flow.

## Best reliability practice

- Export JSON weekly (or after big PR sessions).
- Keep at least one backup file in cloud storage.

## Multi-file hosted mode (optional)

If you host files over `http/https`, include:

- `gzclp.html`
- `manifest.webmanifest`
- `service-worker.js`

This enables proper PWA-style install/offline behavior in supporting browsers.

## Data reset behavior

"Purge Character Progress" only removes this app's keys (`gzclp_*`) instead of clearing all browser storage.
