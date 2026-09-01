---
type: meta
---

## Preface

This document is written during the **Pre-production phase**. We are not committed to a tech stack yet — these are initial thoughts intended to inform our decision when we transition into the **Prototyping phase**. At that point, we will revisit this document and make a final call based on what we need to prove out in a prototype.

---

## Bevy vs Godot 4

Both engines are under active consideration for Terrible Knights. Below is a comparison grounded in the specific demands of this game.

### Bevy (Rust)

**Pros**
- ECS architecture is a natural fit for mass entity processing — the endless horde mechanic and village outcome simulation are well-suited to Bevy's parallel processing model.
- Rust's performance gives headroom for complex simulation (predicting nightly village damage, managing supply chain state across multiple villages) at essentially no runtime cost.
- Low-poly art style keeps rendering demands modest, playing to Bevy's strengths rather than exposing its weaker areas (e.g. no advanced VFX pipeline needed).
- If the team is Rust-comfortable, the codebase will be fast, safe, and highly performant by default.

**Cons / Risks**
- **No visual editor.** Level and settlement map design would be done in code or via external tools. This slows iteration significantly, especially in early production.
- **Multiplayer networking is not first-party.** Co-op (1–6 players) would rely on community crates (`lightyear`, `bevy_replicon`). These are capable but less battle-tested than Godot's built-in multiplayer.
- **Ecosystem maturity.** More game-specific systems (FPS controllers, navmesh, UI) require community crates or custom implementation. More things get built from scratch.
- **Steeper learning curve** for a new studio, particularly for team members not already fluent in Rust.

---

### Godot 4

**Pros**
- **Visual editor.** Scene-based workflow makes level design, UI, and iteration much faster — important for a new studio building confidence.
- **Built-in multiplayer.** Godot 4's high-level multiplayer API is mature and well-documented. Co-op networking is a solved problem out of the box.
- **Larger ecosystem of tutorials and game-specific patterns.** Easier to find answers to common game dev problems (FPS controllers, navigation agents, physics).
- **Faster prototyping.** GDScript in particular allows rapid iteration without compile times.
- Low-poly 3D is well supported and straightforward to implement.

**Cons / Risks**
- **Performance ceiling.** GDScript is slower than Rust. For hundreds of horde entities plus simulation logic, GDScript may require C# or GDExtension (Rust/C++) to hit performance targets. This adds complexity.
- **ECS is not native.** Mass entity processing is less elegant in Godot's node/scene model. Workarounds exist but require discipline.
- **Less architectural guidance** for the simulation layer (supply chains, village state, outcome prediction) — these systems will need careful design to avoid performance pitfalls in GDScript.

---

## Summary

| Concern | Bevy | Godot 4 |
|---|---|---|
| Horde performance | Strong | Manageable (may need C#/GDExtension) |
| Village simulation | Strong | Manageable |
| Multiplayer co-op | Risky (community crates) | Strong (first-party) |
| Level design iteration | Slow (no editor) | Fast (visual editor) |
| FPS gameplay | Buildable (community crates) | Well-supported |
| Learning curve (new studio) | Steeper | Gentler |
| Low-poly rendering | Fine | Fine |

Both engines can ship this game. The decision will likely come down to **team Rust fluency** and **how painful the lack of a visual editor feels during prototyping**. These are the two questions to answer when we enter the Prototyping phase.

From Lead Designer: Ideally, I'd like this to be one of the game projects we attempt to build out with Bevy, I'd love to see what we as a group could accomplish with that Game Engine.
