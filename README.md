# RiyaazKit — Your Daily Music Practice Companion

Every great song starts with fifteen honest minutes. RiyaazKit keeps your guitar,
keyboard or voice in shape — a practice timer that counts only real minutes, a
metronome that keeps you honest, a setlist of songs you're learning, a chord deck
with finger diagrams, an ear trainer, and a listening journal.

**Live:** https://abhiramunni.github.io/riyaazkit/

## What it does

- **Practice console** — pick an instrument (Guitar, Keyboard, Vocals, Violin,
  Ukulele), start a session timer, stop & save. Quick +15 / +30 minute logging
  for practice away from the screen. Daily goal (10 / 20 / 30 / 45 min) with a
  progress bar and plain-words verdict.
- **Metronome** — 40–208 BPM slider, tap tempo, −4 / +4 nudges, 4-beat bar with
  a strong first beat, built on Web Audio (no files, works offline).
- **Setlist** — songs you're learning with progress bars, sorted closest-to-done
  first. Add your own, nudge +10%, or mark "I can play it through". Seeded with
  five Malayalam classics, all removable.
- **Chord deck** — 12 essential guitar chords (C, G, D, Am, Em, F, Dm, E, A, Bm,
  Cadd9, G7) with SVG fretboard diagrams, finger tips, and a "known" tracker with
  a progress ring.
- **This week, honestly** — a 7-day minutes bar chart with a dashed daily-goal
  line, plus a streak counter (consecutive days with any practice).
- **Ear trainer** — two notes play (Web Audio, A4 = 440 Hz); name the interval
  from 7 options. 8 rounds per game, best score saved on-device.
- **Listening journal** — log what you listened to and how it felt; listening
  closely is practice too.
- **Warm-ups & guides** — 6 short routines (finger stretches, chromatic warm-up,
  scale ladder, strumming, vocal breathing, slow run) with done-today toggles,
  and 6 plain-language guides.
- **Your data stays yours** — everything in localStorage only, no account, no
  uploads. Copy a practice summary, remove samples, or erase everything (two-tap).

## Design

Warm editorial palette (ivory paper, espresso ink, bronze / amber / gold /
terracotta) with Fraunces + Inter. Full-screen cinematic intro with a spinning
vinyl record, staggered title and progress bar (tap-to-skip; quick version on
return visits), a 3-step onboarding tour, Ken Burns drift on the two embedded
AI-generated warm-editorial photos, and a "rehearsal studio" layout — hero photo
band with an overlapping practice console, a dark vinyl setlist rail, a chord
deck with a sticky diagram panel, and a dark stage panel for the ear trainer.

## Tech

Single self-contained `index.html` (~1.4 MB, photos embedded as data URIs). No
backend, no build step, no external API. Works offline once loaded (Google Fonts
gracefully falls back to system fonts).

## QA

`node qa-test.js` — 75/75 headless jsdom assertions, `node --check` clean, zero
uncaught JS errors, zero pictographic emoji. Covers seed data, week/streak
maths (seeded week 110 min, streak 3 days), session timer ticking and saving,
metronome BPM clamping and beat advance, song add/bump, chord toggle and SVG
diagrams, ear-trainer scoring, journal and routine toggles, goal switching,
sample removal, and summary text.
