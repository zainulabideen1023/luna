# Decisions

Why Luna is built the way it is. Add a line when you make a choice you might forget the reason for.

- **Name: Luna.** "Talking to the moon": a quiet listener that doesn't answer back.
- **Local-only storage.** Thoughts stay in the browser (localStorage). No accounts, servers, or tracking. Tradeoff: clearing site data or switching phones loses everything, so Backup exists and needs to be easy.
- **Single-file app, no framework or build step.** Easy to edit and paste from a phone, and nothing to install.
- **PWA first, native Android later.** The PWA is free to distribute and works now. A native app is for the Play Store and for connecting to local language models.
- **Hosted on GitHub Pages.** Free, gives the PWA its own address, and the repo carries forward to the native version.
- **Text-only files, SVG icon.** Uploading files from a phone failed, so every file can be pasted into GitHub's editor. PNG icons can't be pasted.
- **Backup by copy and paste, plus file download.** Downloads are blocked inside some viewers, but copy and paste works everywhere.
- **Analysis is simple counting for now.** Word frequency, repeated phrases, and a small tone word list. It works offline and stays private. AI analysis comes later through a model the user picks, ideally a local one. A hosted page can't reach local models, so that needs the native app or a computer.
- **Minimal look.** No moon decorations. The quiet interface is the point.
- **Bump the cache version on every update.** Otherwise the service worker keeps serving the old app.
- **Search clears when you send a thought**, so the new thought is always visible.

## Open questions

- License (not chosen yet).
- Sync: optional encrypted sync, or backup to Drive?
- Tags and daily recap: worth the extra complexity?
