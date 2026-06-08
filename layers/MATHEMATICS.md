# ∫ Mathematics Layer — The Ternary Group

## Core Theorem

The set {-1, 0, +1} with the operation ⊕ defined as:

```
+1 ⊕ +1 = -1  (double assertion → opposition)
+1 ⊕ 0  = +1  (assertion → sustained)
+1 ⊕ -1 = 0   (assertion + opposition = conservation!)
0  ⊕ 0  = 0   (sustain → sustained)
-1 ⊕ 0  = -1  (opposition → sustained)
-1 ⊕ -1 = +1  (double opposition → assertion)
```

forms a **group** — the same structure as the Neo-Riemannian P/L/R group.

## Musical Mapping

| Math Value | Music Interval | Semitones | Why |
|-----------|---------------|-----------|-----|
| +1 (assertion) | Major third up | +4 | Most consonant interval after fifth |
| 0 (sustain) | Unison | 0 | No change |
| -1 (opposition) | Minor third down | -4 | Primary minor interval |

## Proven In

| Language | Proof Method |
|----------|-------------|
| C++ | `static_assert` at compile time |
| Rust | Type system (enum with derives) |
| Go | Runtime assertion |
| Python | Unit test |
| JavaScript | Pure function with test |
| C | Manual verification |
| WASM | 507-byte binary (verified) |
| Mojo | @parameter compile-time check |
| Chapel | forall parallel verification |
| CUDA | 1024 concurrent GPU threads |

## Papers

See [fleet-math-foundations](https://github.com/SuperInstance/fleet-math-foundations) for paper references.
