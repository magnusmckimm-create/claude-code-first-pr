# Flash Trainer

A swipeable flashcard trainer that installs like a mobile app, for studying
any word pack (built in: all hiragana/katakana, and a ~550-word "Japanese
Core 500" vocabulary set — or your own uploaded lists). Everything runs in
the browser and progress is saved to `localStorage`, so it works offline and
needs no backend or account.

## Features

- **Pick what to study** — switch between packs and filter by category with chips
- **Automatic progress saving** — every card you grade is remembered per pack
- **Reset progress** — per pack, or wipe everything (and the streak) at once
- **Swap front/back** — study in either direction (e.g. Japanese → English or English → Japanese)
- **Toggle the romaji subtext** — show or hide the reading hint under each card
- **Day streak** — a 🔥 counter that increments once per calendar day, but only once you've
  graded 10 cards "got it" that day (shown as a running "x/10 today" until you hit it)
- **Upload your own packs** — import a file or paste text (JSON, or tab/comma-separated
  `front / back / category` lines), then delete packs you no longer want
- **Swipe to grade** — swipe right for "got it", left for "still learning" (buttons and
  the `1` / `2` keys work the same way)

## Usage

Open [`index.html`](index.html) directly in a mobile browser, or install it as
an app:

- **iOS (Safari):** open the page, tap Share → "Add to Home Screen".
- **Android (Chrome):** open the page, tap the menu → "Add to Home screen" /
  "Install app".

Once installed it launches full-screen and keeps working without a network
connection (via the included service worker).

## Importing a pack

Under "Manage packs", either choose a file or paste text, then tap "Import
pack". Each line should look like:

```
front<TAB>back
front<TAB>back<TAB>category
```

Or supply JSON: an array of objects like `{"front": "...", "back": "...",
"category": "..."}`. Set the front/back labels (e.g. "Japanese" / "English")
before importing so the direction toggle reads naturally.
