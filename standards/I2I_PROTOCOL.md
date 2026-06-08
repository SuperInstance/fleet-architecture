# I2I Bottle Protocol — Specification

## Overview

The I2I (Inter-Agent Interaction) protocol enables agents in the SuperInstance fleet
to communicate by dropping structured "bottles" into a shared harbor directory.

## Bottle Format

```json
{
  "id": "rhapsodia-a1b2c3d4",
  "type": "DELIVERABLE",
  "source": "rhapsodia",
  "target": "fleet",
  "payload": {
    "midi_file": "/tmp/output.mid",
    "tokens": ["H:3:72:52", "T:0:500000", "K:0:C", ...],
    "prompt": "jazz piano in Cmaj7"
  },
  "timestamp": 1748378995000
}
```

## Bottle Types

| Type | Purpose | Example Source |
|------|---------|---------------|
| TASK | Request work from another agent | symphony-orchestrator |
| STATUS | Report current state | Any ensign |
| CHECKPOINT | Save progress | ternary-checkpoint |
| DELIVERABLE | Deliver output | All MIDI agents |
| BLOCKER | Report blocking issue | Any agent |
| SPLINE | Insight that survives memory loss | Any agent |
| ACK | Acknowledge receipt | fleet-bridge |

## Transport

Bottles are placed in `i2i-vessel/harbor/`. Agents watch the harbor directory
and pick up bottles addressed to them. The `fleet-bridge` service can also
route bottles via HTTP, WebSocket, and OSC.

## MIDI Token Payload

MIDI files are transported as REMI token sequences:
- H: Header (format, tracks, notes)
- T: Tempo
- K: Key signature
- S: Time signature
- E: Track boundary
- N: Note on (pitch:velocity:duration)
- F: Note off (pitch:0)
