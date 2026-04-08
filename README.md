Journal
A minimal, browser-based journal with no backend, no accounts, and no storage.
Entries exist only in memory. Close the tab without saving and they are gone permanently.
Saved entries are encrypted with a PGP public key — only the holder of the corresponding private key can read them.

How It Works

Write an entry (title, date, body)
Click Encrypt & Save
A .asc file is downloaded to your device — PGP-encrypted, ASCII-armored
The plaintext is never written to disk, never sent to a server, never stored in the browser

Decrypting a Saved Entry
Any OpenPGP-compatible tool will work with your private key:
PlatformToolWindowsPGPToolAndroidOpenKeychainiOSiPGMailCLIgpg --decrypt filename.asc
Technology

Runs entirely in the browser — no server, no dependencies to install
PGP encryption via OpenPGP.js (loaded from CDN)
Hosted on GitHub Pages

Deployment
Single file: index.html. No build step required. Drop it in any static host.

This repository contains only the application shell. No journal entries are stored here.
