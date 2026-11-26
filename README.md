# LifeMaxing v1.0

A mobile-first, installable personal life archive. The archive starts on **26 November 2026**.

## Included
- Passcode gate and AES-GCM encrypted local archive (PBKDF2 key derivation)
- Automatic local saving after actions and manual save buttons
- Daily mood, energy, sleep, one-line summary, good/hard moments, gratitude and free journal
- Searchable memory timeline and standalone memory capture
- Custom habits with categories and frequency targets
- Fitness sessions (running, strength, walking, mobility, etc.)
- Study sessions with active-recall notes
- Mood/habit insights, weekly reflections and monthly letters
- Encrypted export/import backup
- PWA manifest and offline shell caching

## Publish on GitHub Pages
Upload `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, and `icon-512.png` to the repository root. In Settings → Pages choose Deploy from a branch → `main` → `/(root)` → Save. Open the Pages URL, then use the browser menu → Add to Home Screen / Install.

## Storage and recovery
The app stores one encrypted data envelope in this browser's localStorage. The passcode is not stored. Export an encrypted JSON backup regularly and keep it somewhere separate (Google Drive is suitable). To restore, import the backup and enter the same passcode. Clearing browser data or losing the device without a backup can permanently remove the local archive. If the passcode is forgotten, the encrypted archive cannot be unlocked.

## Google sign-in / cloud sync
Not active in this build. A real Google sign-in and automatic cloud backup requires a Firebase project, enabled Google provider, Firestore rules, and project configuration. Do not treat local storage as cloud backup. This is deliberately disclosed rather than showing a fake connected status.

## Privacy
The archive is encrypted before it is written to localStorage. The browser's cached app shell is not encrypted, but it contains no journal entries. Use a strong passcode and protect access to the device. This is a personal-use app, not a security-audited vault.
