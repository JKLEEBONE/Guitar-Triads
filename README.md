# Guitar Triad Flashcards, Diagrams & Test

A single-page app for learning and memorizing triad shapes across the guitar neck. No frameworks, no dependencies — just one HTML file.

## Deploy

**Vercel (recommended):**
1. Push this repo to GitHub
2. Import the repo in [vercel.com](https://vercel.com)
3. Deploy — it will automatically serve the `public/` folder

**Or run locally:**
```bash
npx serve public
```

## What's In It

### 4 Tabs:

**1. Flashcards**
- Interactive flip cards (click or spacebar to flip, arrow keys to navigate)
- 3 modes:
  - **Chord Name → Notes**: Shows "G major" → you recall "G - B - D"
  - **Notes → Chord Name**: Shows "G - B - D" → you name the chord
  - **Diagram → Chord & Notes**: Shows a fretboard position → you identify it
- Filter by Major only, Minor only, or both
- Shuffle and reset buttons

**2. Fretboard Diagrams**
- Full horizontal neck diagrams (frets 1-15) showing ALL inversions of each triad across the neck
- 3 string sets with clickable tabs (defaults to G-B-E):
  - **G-B-E** (strings 3-2-1) — default view
  - **D-G-B** (strings 4-3-2)
  - **A-D-G** (strings 5-4-3)
- Each diagram shows 4 strings: the 3 triad strings + 1 adjacent string showing where the triad shape extends
- Color-coded notes:
  - **Orange** = Root
  - **Black** = 3rd
  - **Blue** = 5th
- Connecting lines between notes in the same voicing
- Filter by specific chord and/or major/minor
- Fret markers at 3, 5, 7, 9, 12

**3. Test Dashboard**
- 20-question multiple choice quiz
- 4 question types (or mixed):
  - Chord Name → Notes
  - Notes → Chord Name
  - Diagram → Chord Name
  - Mixed (random from all types)
- Smart wrong answers: all options share the same root note so you can't eliminate by spotting the root
- Live scoring: correct count, total, accuracy %, and streak

**4. Print Cards**
- Printable flashcard layout (Ctrl+P)
- Front/back side by side for cutting and folding
- Filter by major/minor

## Music Theory Covered

- All 12 notes with enharmonic spellings (C#/Db, etc.)
- **Major triads**: Root + Major 3rd + Perfect 5th
- **Minor triads**: Root + Minor 3rd + Perfect 5th
- **3 inversions**: Root position (R-3-5), 1st inversion (3-5-R), 2nd inversion (5-R-3)
- Voicings constrained to max 4-fret spread (playable shapes)
- Standard tuning (E-A-D-G-B-E)

## Tech

- Single HTML file (`public/index.html`), zero dependencies
- Music theory calculated in JavaScript at runtime
- Fretboard diagrams drawn on HTML5 Canvas
- Works fully offline
