# 🎵 Application Layer — 20 MIDI Fleet Repos

## Data Flow

```
Text Prompt → text2midi → MIDI File → tokenizer → REMI Tokens
                                                     │
Ternary Vector → tidalcycles → TidalCycles Patterns  │
State Vector  → musiclang    → Chord Progressions    ├→ I2I Bottle → Fleet
State Sequence → generator   → MIDI Completion      │
Note Training  → markov      → Statistical Stream   │
                                                    │
MIDI File → theorist    → Theory Analysis            │
MIDI File → visualizer  → SVG Piano Roll             │
MIDI File → sheet-music → LilyPond Sheet Music       │
MIDI File → player      → WAV Audio                  │
Text Prompt → jam-engine → 3-Track Band MIDI         │
                                                    ▼
                                           Fleet Harbor (I2I)
```

## Repo Roles

| Layer Role | Repos | What they transform |
|-----------|-------|-------------------|
| **Generators** (input→MIDI) | text2midi, generator, jam-engine, markov | Text/states/vectors → MIDI |
| **Analyzers** (MIDI→data) | theorist, symmetry-analyzer | MIDI → structured analysis |
| **Renderers** (MIDI→output) | visualizer, sheet-music, player | MIDI → SVG/PDF/WAV |
| **Rhythm** (vectors→patterns) | tidalcycles, voice-leader, fugue-engine | Ternary vectors → rhythm/scores |
| **Harmony** (states→chords) | musiclang | State vectors → chord progressions |
| **Transport** (MIDI→tokens) | tokenizer, osc-server | MIDI ↔ tokens ↔ OSC |
| **Mathematics** (core theory) | ternary-music, math-foundations | Group theory ↔ interval theory |

## Cross-Language Implementations

Each key mathematical operation is implemented in 10 languages.
See [fleet-math-foundations](https://github.com/SuperInstance/fleet-math-foundations).
