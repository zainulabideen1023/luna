# Luna 🌙

*Talk to the moon.* Luna is a minimal, private notebook that feels like texting yourself. Send small thoughts as they come, then look back for patterns.

**Live app:** https://zainulabideen1023.github.io/luna/

## Features

- **Thread:** write thoughts like messages. Tap a message to delete it (you can undo for a few seconds).
- **Tags:** add `#idea` or `#worry` to any thought. Tap a tag to see everything with it; Patterns counts them.
- **Search:** filter your thoughts as you type, with highlighted matches.
- **Patterns:** thought count, streak, the hours you think most, repeated words and phrases, topics that return across days, a rough tone estimate, and an occasional thought from your past.
- **Backup:** copy or download all your thoughts and restore them later, on any device.
- **Works offline** and installs to your home screen as an app (PWA).

## Privacy

- Your thoughts are stored only in your browser on your device. There are no accounts, no servers, and no tracking.
- All analysis runs on your device, using your own words. Nothing is sent anywhere.
- The only network request is the page font from Google Fonts. If it can't load, Luna falls back to your system font.
- Because data lives in the browser, clearing site data or switching phones erases it. Luna asks your browser to protect its storage, but that isn't guaranteed, so use **Backup** regularly.

## Install on Android

1. Open the live app in Chrome.
2. Tap the menu, then **Install app** (or **Add to Home screen**).

## Install on iPhone or iPad

1. Open the live app in **Safari**. (Other browsers can work on iOS 16.4 and later, but Safari is the most reliable.)
2. Tap the **Share** button (the square with an arrow pointing up).
3. Scroll down and tap **Add to Home Screen**, then **Add**.
4. Open Luna from the new home screen icon.

Notes for iOS:
- The installed app keeps its own storage, separate from Safari. If you used Luna in a Safari tab first, back up there and restore inside the installed app.
- Luna ships a 180px Apple touch icon so the moon appears on the home screen. This hasn't been tested on an iPhone yet.

## Back up and restore

- **Backup → Copy backup**, then paste it somewhere safe such as a note to yourself.
- To restore, open **Backup** and tap **Choose backup file** (a `.json` file from **Download file**), or paste a backup into the box and tap **Restore thoughts**. Thoughts already in Luna are kept and new ones are added.

## How the analysis works

Luna counts things; it doesn't understand them. Repeated words, phrases and topics work in any script, including Urdu and Roman Urdu. Tone uses a small English word list, so it misses negation ("not happy"), sarcasm and Urdu. Treat it as a rough hint.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS, JavaScript) |
| `manifest.json` | Install details: name, colors, icon |
| `sw.js` | Service worker that makes Luna work offline |
| `icon.svg` | App icon (source artwork) |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | PNG icons for Android, installs and iPhone |
| `CHANGELOG.md` | What changed in each version |
| `DECISIONS.md` | Why things are built the way they are |


## Roadmap

- Daily recap
- Optional analysis with a language model of your choice, including local models
- Native Android app

## License

Not chosen yet.
