# Changelog

All notable changes to this project are documented here.
Format loosely follows [Keep a Changelog](https://keepachangelog.com/).

## [0.2.0] — 2026-06-21

### Added
- **Minor-key analysis** — set a minor key (`key: Am`, `F#m`, …) and Roman numerals /
  harmonic functions are analyzed against the natural + harmonic minor (i, ii°, III, iv,
  v/V, VI, VII/vii°); substitutions and transposition respect the minor key.
- **Autosave** — the document is saved to local storage on every edit and restored on
  reload; a save indicator shows in the editor header.
- **New / Open / Save** — start a blank song, open a `.txt` / `.md` / ChordPro file, or
  download the source as `.txt` (re-openable).
- **Invalid-chord linting** — unrecognized chords are underlined in red with a count in
  the preview header; non-chord tokens (e.g. `N.C.`) render as plain labels.
- **Tempo (BPM)** — `bpm:` / `tempo:` directive and a ♩ tempo pill.
- **Theme menu** — Dark, Light, Terminal, Sepia, and Pastel themes (remembered between
  sessions).

### Fixed
- Substitution popover no longer gets clipped at the bottom of the window — it flips above
  the chord and clamps to the viewport.

## [0.1.0] — 2026-06-21

Initial version.

### Added
- Text-first editor with live preview pane.
- Music-theory engine: chord parsing, key-aware transposition, Roman-numeral and
  harmonic-function analysis, substitution generation, and enharmonic note spelling.
- Chord substitution menu (tritone, relatives, same-function, secondary dominants,
  borrowed chords, extensions).
- Key transposition by semitone or to any target key.
- Color coding by harmonic function with Roman-numeral labels.
- Chord notes and 2-octave piano diagrams on hover and in the substitution menu;
  toggle to show notes under every chord.
- Export to Markdown; print to PDF with colors preserved.
- Dark / light themes, command palette, chord autocomplete, resizable editor/preview split.
