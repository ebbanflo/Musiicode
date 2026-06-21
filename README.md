# Musiicode

[![Live demo](https://img.shields.io/badge/▶_Live_demo-Musiicode-89b4fa?style=for-the-badge)](https://ebbanflo.github.io/Musiicode/)
[![License: MIT](https://img.shields.io/badge/License-MIT-a6e3a1?style=for-the-badge)](./LICENSE)

A music-writing IDE — write chord charts and lead sheets like code, with live harmonic
analysis, chord substitutions, key transposition, piano-shape diagrams, and color coding
by harmonic function.

**▶ Try it live:** <https://ebbanflo.github.io/Musiicode/>

It's a single self-contained `index.html` — no build step, no dependencies, no network
calls. Open it in a browser, or wrap it with [Tauri](https://tauri.app/) for a native
desktop app.

> Status: personal project / work in progress. Used as a reference and writing tool.

## Features

- **Text-first editor** with a live preview pane.
- **Chord substitutions** — click any chord for tritone subs, relative major/minor,
  same-function diatonic swaps, secondary dominants, borrowed chords, and extensions.
  Picking one rewrites the source.
- **Major & minor key analysis** — Roman numerals and harmonic function for both major
  and minor keys (set `key: Am`, `F#m`, …).
- **Key transposition** — semitone steps or jump to any key, with key-aware sharp/flat
  spelling (slash-chord basses included).
- **Color coding** by function — tonic, subdominant, dominant, and chromatic/borrowed.
- **Chord notes + piano diagrams** on hover (and in the substitution menu); a toggle to
  show notes under every chord.
- **Invalid-chord linting** — unrecognized chords are underlined with a count in the header.
- **Tempo (BPM)** and time-signature display.
- **Autosave** to local storage, plus **New / Open / Save** (`.txt` / `.md` / ChordPro).
- **Export** to Markdown or source `.txt`, or print to PDF (preserves the colored sheet).
- **Five themes** (dark, light, terminal, sepia, pastel), a **command palette**, chord
  **autocomplete**, and a **resizable** editor / preview split.

## Quick start

Open `index.html` in any modern browser. That's it. Press <kbd>⌘K</kbd> / <kbd>Ctrl+K</kbd>
for the command palette, or click **syntax help** in the editor header.

## Syntax

```
title: My Song          ← document directives (optional)
key: C
time: 4/4

# Verse                 ← section header

| Cmaj7 Am7 | Dm7 G7 |  ← barred chords, | is a bar line

[C]Twinkle [G]twinkle [Am]little [F]star   ← chords inline above lyrics
```

| You write | It means |
|-----------|----------|
| `key: C` `time: 4/4` `title: …` | document settings |
| `# Name` | a section header |
| `\| Cmaj7 Am7 \| Dm7 G7 \|` | chords grouped into bars |
| `[C]word` | a chord positioned above a lyric |

Chord symbols follow normal lead-sheet notation: `C`, `Am7`, `Gmaj7`, `F#m7b5`, `Bdim7`,
`Csus4`, `D7/F#`, `Eb13`, etc.

## Keyboard / interactions

| Action | How |
|--------|-----|
| Command palette | <kbd>⌘K</kbd> / <kbd>Ctrl+K</kbd> |
| Chord autocomplete | start typing a chord, <kbd>Tab</kbd> to accept |
| See a chord's notes + piano shape | hover the chord in the preview |
| Substitute a chord | click the chord in the preview |
| Transpose | <kbd>▲</kbd>/<kbd>▼</kbd> buttons, or the Key pill |
| Show notes under every chord | **♪ Notes** |
| Export Markdown / PDF | **⤓ Export** |
| Resize panes | drag the divider; double-click to reset |

## Tech

Plain HTML, CSS, and vanilla JavaScript in one file. The music-theory engine (chord
parsing, transposition, Roman-numeral analysis, substitutions, and note spelling) is
self-contained and has no runtime dependencies.

## Roadmap

- Beat-accurate chord placement within bars
- Nashville-number view
- Altered-dominant (`alt`) chord parsing
- ChordPro import/export round-tripping

## License

[MIT](./LICENSE) © 2026 Ebban
