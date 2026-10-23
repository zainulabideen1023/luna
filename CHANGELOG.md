# Changelog

Newest first. When `index.html` changes, bump the cache version in `sw.js` and note it here.

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
