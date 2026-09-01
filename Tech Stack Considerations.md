---
type: meta
---

## Preface

This document is written during the **Pre-production phase**. We are not committed to a tech stack yet — these are initial thoughts intended to inform our decision when we transition into the **Prototyping phase**. At that point, we will revisit this document and make a final call based on what we need to prove out in a prototype.

---

## Bevy vs Godot 4 (C# + Chickensoft)

Both engines are under active consideration for Terrible Knights. The Godot side of this comparison assumes **C# with the Chickensoft framework** — our preferred Godot stack across projects. Below is a comparison grounded in the specific demands of this game.

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

### Godot 4 (C# + Chickensoft)

[Chickensoft](https://chickensoft.games) is an open-source framework built on top of Godot 4 + C# that provides structured architecture patterns: dependency injection (`AutoInject`), hierarchical state machines (`LogicBlocks`), testing infrastructure, and project scaffolding. It's our preferred Godot stack.

**Pros**
- **Visual editor.** Scene-based workflow makes level design, UI, and iteration much faster — important for a new studio building confidence.
- **Built-in multiplayer.** Godot 4's high-level multiplayer API is mature and well-documented. Co-op networking is a solved problem out of the box.
- **C# performance.** Far faster than GDScript. The horde and simulation performance concerns that apply to vanilla Godot are largely eliminated here.
- **Chickensoft's `LogicBlocks`** are a strong fit for this game's stateful systems — village states, the day/night cycle, supply chain state management, and World Event handling all map naturally to hierarchical state machines.
- **Structured architecture.** Chickensoft's patterns (`AutoInject`, node lifecycle management) impose discipline on complex systems, reducing the risk of the codebase becoming unwieldy as scope grows.
- Low-poly 3D is well supported and straightforward to implement.

**Cons / Risks**
- **ECS is not native.** Mass entity processing is less elegant in Godot's node/scene model. C# + disciplined patterns help, but it's not the same as a true ECS. The horde mechanic may require careful design to avoid node overhead at scale.
- **Smaller community within a community.** Godot tutorials are plentiful; Chickensoft-specific resources are fewer. The team will be charting more of their own path.
- **More upfront setup.** Chickensoft's tooling adds initial complexity compared to dropping into GDScript. Pays off at scale, but has a learning curve.
- **Compile times.** C# loses GDScript's instant iteration. Not severe, but notable vs. scripted workflows.

---

## Summary

| Concern | Bevy | Godot 4 (C# + Chickensoft) |
|---|---|---|
| Horde performance | Strong (ECS) | Good (C# eliminates GDScript ceiling; node overhead at scale still a watch item) |
| Village simulation | Strong | Good (LogicBlocks a natural fit) |
| Multiplayer co-op | Risky (community crates) | Strong (first-party) |
| Level design iteration | Slow (no editor) | Fast (visual editor) |
| FPS gameplay | Buildable (community crates) | Well-supported |
| Stateful systems architecture | ECS native | Strong (Chickensoft LogicBlocks) |
| Learning curve (new studio) | Steeper | Moderate (Godot + C# + Chickensoft layer) |
| Low-poly rendering | Fine | Fine |

Both engines can ship this game. With C# + Chickensoft, Godot closes the performance gap significantly and gains architectural structure that suits this game's complexity. The decision will likely come down to **team Rust fluency** and **how painful the lack of a visual editor feels during prototyping**. These are the two questions to answer when we enter the Prototyping phase.

From Lead Designer: Ideally, I'd like this to be one of the game projects we attempt to build out with Bevy, I'd love to see what we as a group could accomplish with that Game Engine. But I understand the maturity of it isn't quite there. The only two things that really hit me are
1. It still needs a visual builder for non-generated scenes (e.g. building out the Main City for example). 
	1. This is being worked on, and if Sovereign Pirate is our first studio production, this may be a thing by the time we are prototyping this project
2. Multiplayer support
	1. This isn't a total no go, again, there are solutions out there, but we would need to test and vet them to determine what we can use and what we may need to build around that choice to make it all work.


I think Bevy DOES potentially give us more room to scale the chaos for Horde mode in night scenes, but admittedly, depending on the networking solution for multiplayer, that could pose as a bottleneck. Again things we'd have to discover during a prototype phase.
