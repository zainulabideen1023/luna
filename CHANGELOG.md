# Changelog

Newest first. When `index.html` changes, bump the cache version in `sw.js` and note it here.

## v3 (cache `luna-v3`) - 2026-11-19
- Storage now goes through one `Store` object (load, save, export, parse, merge), so a native app can swap it out.
- Saving no longer fails silently: a banner warns when storage is full or blocked.
- Unreadable saved data is kept (not overwritten) and can be shown from the Backup tab.
- Asks the browser for persistent storage after your first thought; Backup shows whether it's protected.
- Patterns now works with any script, including Urdu (plus basic Urdu and Roman Urdu stopwords). Tone is still English-only.
- Right-to-left text lays out correctly in bubbles, the composer, search and Patterns.
- Question share also counts the Arabic-script question mark.
- Deleting a thought can be undone for 6 seconds.
- "From your past" stays the same all day instead of changing on every tap.
- Added PNG icons (192, 512, and a 180 Apple touch icon) so the home screen shows the moon on iPhone and installs cleanly on Android. The SVG stays as a fallback.
- Backup file now includes `exportedAt`. Restore reads older backups, warns about newer ones, and reports save failures.

## v2 (cache `luna-v2`) - 2026-10-23
- Added search: filters the thread as you type, highlights matches, shows a count.
- Searching with several words requires all of them to match.
- Sending a new thought clears the search.

## v1 (cache `luna-v1`) - 2026-10-23
- First release as a PWA, named Luna.
- Thread: write thoughts like messages, tap one to delete it.
- Patterns: thought count, streak, busiest hour, repeated words and phrases, loops across days, rough tone estimate, question share, a thought from your past.
- Backup tab: copy or download all thoughts, restore by pasting (skips duplicates).
- Offline support, installable to the home screen, light and dark themes.
- Text-only files (`index.html`, `manifest.json`, `sw.js`, `icon.svg`) so everything can be pasted into GitHub from a pho
ne.
