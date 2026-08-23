# CLANKER — Little Torment

A browser toy. A small white robot in a facility, and a pink partner who chose to stay.
Equip a weapon, click either of them. Everything is a single self-contained `index.html`
(vanilla JS + canvas + Web Audio, no build step, no dependencies).

## Run locally
Just open `index.html`, or serve it:
```
python3 -m http.server 8000
# then visit http://localhost:8000
```

## How it works
- **Verlet ragdoll physics** for both characters, grab-and-fling on either body.
- **Procedural dialogue** — Clanker starts in corporate-assistant voice and degrades to
  screaming; lines never repeat (persisted used-line registry).
- **Emotional state model** (pain / grief / attachment / hope / dissociation) persisted to
  localStorage, drives voice and behaviour.
- **Partner system** with shared-pain scars, a personalized death sequence, and endless
  post-death interaction.
- **Pain-driven environment** — the room bruises as cumulative damage rises.

All state lives in `localStorage`; there is no backend.
