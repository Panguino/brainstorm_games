# Combat and flight

**Status:** Draft  
**Owners:** Both

## Flight model

**Two control systems (Brad + team — both in scope)**

We want **two distinct flight modes**, swappable by **context** (e.g. overworld vs mission type) or by **node design**—exact handoff rules are TBD in [core-loop-and-modes.md](./core-loop-and-modes.md).

| Mode | Fantasy | Control summary |
|------|---------|-------------------|
| **Free flight (3D)** | [Avorion](https://www.avorion.net/)–style **six-DOF** (or near–six-DOF) **space flight** in open volumes | Player steers **thrust / rotation**, picks vectors, dogfights in **open space** or large arenas |
| **On-rails** | **Star Fox**–style **corridor** or **tunnel** runs on a **defined path** at a **set or scripted speed** | Lateral / vertical **lane** offset, **roll / barrel dodge**, aim/shoot; path and **pace** authored per spline or tunnel |

**Shared expectations**

- **Weapons** and **damage** should feel consistent across modes where possible (same ship fantasy), even if **aiming affordances** differ (rails: generous lock / lead reticle; free: full aim).
- **Difficulty** is tuned per mode: rails emphasize **pattern literacy**; free flight emphasizes **spatial control** and **threat geometry**.

## Camera

<!-- Lock-on, cinematic rails, player control, sickness safeguards. -->

| Mode | Camera bias |
|------|-------------|
| **Free 3D** | Chase cam, optional cockpit; **player** controls look offset; watch **disorientation** in dense asteroids |
| **On-rails** | **Cinematic** forward push; mild **look-at** threats; reduce **motion sickness** (FOV, banking limits, vignette options) |

## Controls (intent)

<!-- Stick layout, dodge/barrel roll, brake/boost, priority actions. -->

| Mode | Primary verbs |
|------|----------------|
| **Free 3D** | Pitch/yaw/roll, thrust/brake, strafe if we include it; boost on cooldown or energy |
| **On-rails** | **Lane** position, roll, aim/fire; **speed** may be **scripted** (scripted boosts/slow zones) rather than always player-throttle |

## Weapons and tools

| Slot / type | Role | Notes |
|-------------|------|-------|
| Primary     |      |       |
| Secondary   |      |       |
| Utility     |      |       |

## Enemies and encounters

<!-- Archetypes, telegraphing, mix rules for waves. -->

## Boss structure

**WoW-style raid DNA (Brad + team)**

- **Multi-phase:** health thresholds or timers **advance phases**; each phase changes **mechanics**, **arena geometry**, or **adds** (similar in *feel* to [World of Warcraft](https://worldofwarcraft.blizzard.com/) raid bosses—telegraphed roles, soak, dodge windows, intermission puzzles—not a 40-player clone).
- **Boss-as-puzzle:** phases can include **positional puzzles**, **weak-point windows**, **interrupt cadence**, or **environment interactions** (monuments-lite but inside one fight).
- **Spectacle vs readability:** rail / 3D flight means **fewer simultaneous** mechanics than a top-down MMO; cap **HUD clutter** and **audio** callouts.

**Procedural composition (Brad)**

- Bosses are **not** fully random soup: use an **authoring kit** of **mechanic modules** (beam sweep, mine drop, fighter escort, gravity well, puzzle gate, etc.).
- A **boss composer** picks a **sequence** and **subset** of modules per seed (and may scale with **sector depth** toward galactic core).
- **Goals:** variety across runs + **learnable** tells once a module appears; **avoid** unfair combos (ban-lists, tags like `movement-heavy` × `low-visibility`).

| Layer | Authored | Procgen / composed |
|-------|----------|-------------------|
| Phase skeleton | Example order templates | Which template + how many phases |
| Mechanics | Each module tuned + VOFX | Which modules, order, timing offsets |
| Identity | Silhouette, name, one-liner | Palette swap, attach prefab kit |

## Difficulty knobs (combat-local)

<!-- Not full meta—just damage, aggression, patterns. -->

- Per-module **intensity** (speed, density) independent of **which** modules rolled.

## Open questions

- **Co-op / vs scaling:** do boss puzzles assume **solo** count, or variable party size?
- **Validation:** automated or designer-reviewed **combo allowlist** so procgen bosses stay **clearable** on rails?
- **Mode per content:** is **free flight** default for **galaxy / sector space** and **rails** for **setpieces / tunnels / monuments**, or do some **bosses** mix **phases** (free → rail snap)?
- **Same ship, two rigs:** one **prefab** with two **controllers**, or different **craft** per mode—what is better for **feel + scope**?
