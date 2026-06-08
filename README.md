# 🏗️ fleet-architecture

**The complete architecture of the SuperInstance fleet — layers, protocols, data flows.**

This repo documents how all 56+ repos connect. It's the map that shows where each piece fits.

## The Five Layers

```
┌─────────────────────────────────────────────────────┐
│  🎵 Application Layer                               │
│  text2midi, musiclang, markov, jam-engine, etc.     │
├─────────────────────────────────────────────────────┤
│  🔌 Integration Layer                                │
│  strudel, hydra, magenta, orca, touchdesigner, etc.  │
├─────────────────────────────────────────────────────┤
│  ∫ Mathematics Layer                                │
│  ternary-music, math-foundations, symmetry-analyzer │
├─────────────────────────────────────────────────────┤
│  🏛️ Infrastructure Layer                            │
│  fleet-bridge, tminus-dispatcher, i2i-bottle-agent  │
├─────────────────────────────────────────────────────┤
│  🧠 Orchestration Layer                             │
│  symphony-runtime, symphony-orchestrator, headspace │
└─────────────────────────────────────────────────────┘
```

## Architecture Files

| File | What it covers |
|------|---------------|
| `layers/APPLICATION.md` | The 20 MIDI fleet repos and their relationships |
| `layers/INTEGRATION.md` | 6 ecosystem connectors and how they bridge |
| `layers/MATHEMATICS.md` | The ternary group, conservation laws, proofs |
| `layers/INFRASTRUCTURE.md` | Fleet-bridge, I2I protocol, dispatchers |
| `layers/ORCHESTRATION.md` | Symphony runtime, composite headspace |
| `standards/I2I_PROTOCOL.md` | The I2I bottle protocol spec |
| `standards/MIDI_TOKENS.md` | REMI token format specification |
| `diagrams/` | ASCII architecture diagrams for each layer |

## Quick Navigation

| You want to... | Start here |
|---------------|-----------|
| Understand the MIDI pipeline | `layers/APPLICATION.md` |
| Bridge to an external tool | `layers/INTEGRATION.md` |
| Learn the mathematical foundation | `layers/MATHEMATICS.md` |
| Connect to the fleet infrastructure | `layers/INFRASTRUCTURE.md` |
| Orchestrate multiple agents | `layers/ORCHESTRATION.md` |
| Follow the I2I protocol | `standards/I2I_PROTOCOL.md` |
| Run a complete pipeline | `tutorials/` |

## Tutorials

Each layer has a step-by-step tutorial that walks through the complete flow.
See `tutorials/` for the full collection.
