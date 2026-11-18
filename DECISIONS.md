# Decisions

Why Luna is built the way it is. Add a line when you make a choice you might forget the reason for.

- **Name: Luna.** "Talking to the moon": a quiet listener that doesn't answer back.
- **Local-only storage.** Thoughts stay in the browser (localStorage). No accounts, servers, or tracking. Tradeoff: clearing site data or switching phones loses everything, so Backup exists and needs to be easy.
- **Single-file app, no framework or build step.** Easy to edit and paste from a phone, and nothing to install.
- **PWA first, native Android later.** The PWA is free to distribute and works now. A native app is for the Play Store and for connecting to local language models.
- **Hosted on GitHub Pages.** Free, gives the PWA its own address, and the repo carries forward to the native version.
- **Text files, plus three PNG icons.** Everything except the icons is plain text so it can be pasted into GitHub's editor from a phone. The PNGs (`icon-192.png`, `icon-512.png`, `apple-touch-icon.png`) are generated from `icon.svg` and need a real file upload; iOS and Play Store need PNGs. They are not precached by `sw.js`, so a missing icon can never break offline install. If the artwork changes, regenerate all three. The moon sits inside the safe zone, so one 512 file serves as both normal and maskable.
- **Backup by copy and paste, plus file download.** Downloads are blocked inside some viewers, but copy and paste works everywhere.
- **Analysis is simple counting for now.** Word frequency, repeated phrases, and a small tone word list. It works offline and stays private. AI analysis comes later through a model the user picks, ideally a local one. A hosted page can't reach local models, so that needs the native app or a computer.
- **Minimal look.** No moon decorations. The quiet interface is the point.
- **Bump the cache version on every update.** Otherwise the service worker keeps serving the old app.
- **Search clears when you send a thought**, so the new thought is always visible.
- **One `Store` object owns all storage.** Nothing else touches localStorage, so the native app replaces this one object (SQLite or files) and the rest of the app stays the same.
- **Never overwrite data we can't read.** If saved data fails to parse, it is copied to `mindchat:thoughts:unreadable` before Luna starts empty, and the Backup tab can show it.
- **Backup format is a contract.** `{app:'luna', version:1, exportedAt:<ms>, thoughts:[{id:string, text:string, ts:<ms>}]}`. Readers ignore unknown fields and also accept a bare array of thoughts. Add new optional fields freely (tags can be derived from the text, so they need none); bump `version` only for a breaking change, and never change what an existing field means.
- **Ask for persistent storage after the first thought,** not on load. Some browsers show a permission prompt, and it makes more sense after you've used the app.
- **Words are letters in any script** (`\p{L}`, `\p{M}`), with a minimum length of 4 for Latin and 3 for other scripts. Anything inserted into Patterns HTML must stay letters-only or go through `esc()`.
- **"From your past" is picked by date,** so it is stable for a day and changes tomorrow.
- **Tone stays English-only for now.** Urdu tone needs its own word list, or the language-model step.

## Open questions

- License (not chosen yet).
- Sync: optional encrypted sync, or backup to Drive?
- Urdu tone word list.
- Tags and daily recap: worth the extra complexity?
