# Musiicode

A music-writing IDE — write chord charts and lead sheets like code, with live harmonic
analysis, chord substitutions, key transposition, piano-shape diagrams, and color coding
by harmonic function.

It's a single self-contained `index.html` (no build step, no dependencies). Open it in a
browser, or wrap it with [Tauri](https://tauri.app/) for a native desktop app.

## Features

- **Text-first editor** with live preview — directives (`key:`, `time:`, `title:`),
  `# Section` headers, barred chords `| Cmaj7 Am7 | Dm7 G7 |`, and inline chord-over-lyric
  lines `[C]Twinkle [G]twinkle`.
- **Chord substitutions** — click any chord for tritone subs, relatives, same-function
  diatonic swaps, secondary dominants, borrowed chords, and extensions.
- **Key transposition** — semitone steps or jump to any key, with key-aware sharp/flat spelling.
- **Roman-numeral analysis** and **color coding** by function (tonic / subdominant / dominant / chromatic).
- **Chord notes + piano diagrams** on hover.
- **Export** to Markdown or print to PDF.
- Dark / light themes and a resizable editor / preview split.

## Usage

Open `index.html` in any modern browser. Press <kbd>⌘K</kbd> / <kbd>Ctrl+K</kbd> for the
command palette, or click **syntax help** in the editor header.

## License

MIT
