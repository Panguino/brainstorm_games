# Technical and scope

**Status:** Draft  
**Owners:** Both

## Target platforms

<!-- PC first? Console? handheld? -->

## Engine / stack

<!-- Unity, Unreal, Godot, custom—undecided is fine. -->

## Art direction (Brad)

- **Meshes:** favor **lower-poly**, readable shapes (performance headroom + strong silhouette).
- **Juice:** spend budget on **particles, beams, impacts, and lighting** (post stack, volumetrics, stylized bloom—exact tech depends on engine).

## Multiplayer

**Design intent (Brad + team — draft)**

- Support **solo**, **co-op**, **versus**, and **mixed** formats under one **galactic race** premise: players **work inward** on a **sector map** and may **run into each other** along the way.
- **Open questions for engineering:** session model (dedicated servers vs peer), **shard** size, **instancing** per sector mission vs **persistent** galaxy, anti-cheat for PvP, and how **crossings** are scheduled (random overlap, opt-in invasion, shared hubs).

**Likely complexity order for prototypes**

1. Solo **rim → core** with procgen nodes (no netcode).
2. Co-op **fixed party** in shared sector instances.
3. Versus or **mixed** crossings (highest design + tech risk).

## Content pipeline

<!-- How we ship levels: splines, chunks, Houdini, hand-authored, etc. -->

**Brad — procedural content**

- Goal: **procedurally generated** as much as is practical: **routes**, **encounters**, **loot**, possibly **environment chunks** along splines, etc.
- Likely still need **authored kits** (tile sets, enemy modules, boss patterns) so procgen assembles **legible** encounters rather than noise.
- **Monuments (Rust-style):** ship **discrete authored prefabs** (puzzles, derelicts, “plants”) as **stable content**; the **generator** only decides **if** they appear, **where** on the route graph they plug in, and **orientation**—same brain-teach each time, fresh **hunt** each run.
- **Boss composer:** same philosophy as encounters—**authored mechanic modules** (phases, attacks, puzzles) assembled by a **composer** into **multi-stage** bosses ([combat-and-flight.md](./combat-and-flight.md)); validate combos so **rails readability** holds.
- **Dual flight stack:** ship **two player controllers**—**six-DOF (or arcade 3D) free flight** and **spline / tunnel on-rails**—plus **content** that declares which mode a mission uses ([combat-and-flight.md](./combat-and-flight.md)). Plan **shared** combat data (weapons, HP) where possible to avoid double-balancing everything.

## Prototype plan

<!-- Smallest vertical slice to validate fun: -->

1. 
2. 
3. 

## Risks

| Risk | Mitigation |
|------|------------|
| Procgen + rail shooter readability | Curated piece library, playtest seeds, caps on simultaneous threats |
| Procgen boss combos | Module tags, ban-lists, **composer** tests; fewer concurrent mechanics than MMO raids |
| Two flight systems | Shared **ship stats** + mode-specific **controllers**; **prototype each** separately before blending |
| Materia-style systems + run reset rules | Paper-design the two-track model before implementation |
| Visual polish vs solo/small team scope | Lock art rules early (low poly + one great lighting pass) |
| Multiplayer + procgen galaxy scope | Ship **solo** first; gate PvP on **fun** crossings not griefing; strict MVP netcode |

## Cut line (if we are behind)

<!-- Ordered list: what dies first. -->

1. 

## Open questions

- Which **engine** best supports spline rails + heavy VFX + your target platforms?
- **Full procgen narrative:** Chris wants drip lore—does procgen only structure *delivery* while text stays authored, or true gen narrative (usually high risk)?
- **Netcode:** which **session** shape matches “meet people on the way” without exploding budget?
