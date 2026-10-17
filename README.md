# fintaro-updates

Public download place for updates of the Fintaro desktop app. No code lives here.

Each release `vX.Y.Z` holds only:

- the updater bundles of that version,
- their `.sig` files (minisign signatures),
- `latest.json` (the update manifest).

The app reads `https://github.com/fintaro-ai/fintaro-updates/releases/latest/download/latest.json`.
It installs a bundle only if its signature verifies against the update key built into the app
(minisign key ID `C3943901C782EABB`) and the signed version equals the offered one.

Bundles are signed offline. The secret key is never in this repository, in GitHub, or in any
automation. The process is documented in `docs/RELEASE.md` of the Fintaro product repository.
