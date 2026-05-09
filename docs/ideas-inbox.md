# Ideas inbox

**Status:** Draft  
**Owners:** Both

Dump raw ideas here first. When something survives discussion, move it into the relevant doc and mark this line **Moved** with a link path.

**Triage tags:** `[combat]` `[flight]` `[roguelike]` `[meta]` `[narrative]` `[tech]` `[audio]` `[ux]`

---

## Brad

- `[tech]` `[roguelike]` **Heavy procedural generation:** bias toward **procedurally generated everything** (scope TBD: stages, encounters, loot tables, visuals—see [technical-and-scope.md](./technical-and-scope.md)).
- `[roguelike]` `[meta]` **Materia-style growth:** socket or attach **mods / items** that **level up** over use or investment (FF7 **Materia** vibe—slots, AP, fusion rules all TBD).
- `[tech]` **Art direction:** **lower-poly** geometry paired with **strong particles and lighting** (readable silhouette + flashy read on combat).
- `[meta]` **Achievements and secrets:** mix of **easy** collectibles for momentum and **very hard** goals for prestige / long-tail (overlaps Chris—merge in [roguelike-progression.md](./roguelike-progression.md)).
- `[roguelike]` `[meta]` **Rust-style monuments / puzzles:** **procgen map** (or route) but **hand-authored “monuments”**—same **layout and solution** each time so players **learn** them across runs; **placement**, **orientation**, and **whether a given monument appears at all** vary by seed (like Rust: water treatment **exists as a design**, but **where** it lands on the island changes). See [roguelike-progression.md](./roguelike-progression.md).
- `[combat]` `[roguelike]` **WoW-style bosses:** **multi-stage** fights with **mechanic + puzzle** beats per phase (telegraphs, soak windows, intermissions); bosses **partly procgen** by **composing** hand-made **mechanic modules** into a boss “recipe” per run. See [combat-and-flight.md](./combat-and-flight.md).
- `[flight]` `[tech]` **Two flight systems:** (1) **full 3D flying**, [Avorion](https://www.avorion.net/)–style in open space; (2) **on-rails** **Star Fox**–style through **tunnels** or along a **fixed path** at **authored speed**. Both wanted; context per mission / layer TBD. See [combat-and-flight.md](./combat-and-flight.md), [core-loop-and-modes.md](./core-loop-and-modes.md).

## Chris

- `[narrative]` **Drip lore:** slowly unlock story and world lore across playthroughs (not front-loaded).
- `[narrative]` **Character depth:** cast that grows over time; relationships / arcs worth returning for.
- `[roguelike]` `[meta]` **Build depth + “math break” fantasy:** customization and choices that support deep synergies and overpowered-feeling combos (Chris framed this with **loot boxes**—needs a design call: real-money / gacha-style vs purely in-run reward containers vs no “boxes,” just drops).
- `[roguelike]` **Two-layer power:** abilities / skills / power-ups gathered during a run and **lost on run end**, plus separate **permanent** unlocks from play.
- `[roguelike]` `[meta]` **Achievements → cards:** achievements unlock **cards** (or card-like options) that can be placed into a **pre-run loadout** (deck-building or slot-based—TBD).
- `[meta]` **Achievements and secrets:** long-tail goals, optional content, discoverability without spoiling surprises.

## Together / unclear owner

- `[roguelike]` `[ux]` **Sector rage timer:** hard or soft time limit per sector / level (pressure + pacing).
- `[roguelike]` **Artifact run:** objective is to **find an artifact**, then **escape with it** (defend / route / extraction twist).
- `[roguelike]` **Time-pressure nodes:** some route nodes are explicitly clocked (different from always-on sector timer—could stack or replace).
- `[narrative]` `[meta]` **Theme — race to galactic center:** **2D sector map** (rim → core), [Avorion](https://www.avorion.net/)–style overworld feel; **solo / co-op / vs / mix**; may **encounter other players** on the way; pathing **fully open** vs **ABC forks** or hybrid.
- `[narrative]` **Why the center:** **being chased** inward; or **finding the source** of the enemy (or both).
- `[narrative]` `[meta]` **Replay fiction:** **time loops** (learn from last run); or **simulation / training** runs with a **“real”** attempt after reset; or simulation **hidden** from the player until reveal (trust / payoff TBD).

---

## Synced into structured docs

| Topic | Where it lives |
|-------|----------------|
| Chris progression + achievements/cards | [roguelike-progression.md](./roguelike-progression.md), [world-and-narrative.md](./world-and-narrative.md) |
| Sector timer, artifact escape, timed nodes | [core-loop-and-modes.md](./core-loop-and-modes.md) |
| Brad: procgen scope, art stack, materia-style systems | [technical-and-scope.md](./technical-and-scope.md), [roguelike-progression.md](./roguelike-progression.md) |
| Brad: authored monuments in procgen space (Rust-like) | [roguelike-progression.md](./roguelike-progression.md), [core-loop-and-modes.md](./core-loop-and-modes.md), [technical-and-scope.md](./technical-and-scope.md) |
| Galactic race theme, map, multiplayer mix, replay frames | [vision-and-pillars.md](./vision-and-pillars.md), [core-loop-and-modes.md](./core-loop-and-modes.md), [world-and-narrative.md](./world-and-narrative.md), [technical-and-scope.md](./technical-and-scope.md), [roguelike-progression.md](./roguelike-progression.md) |
| WoW-style multi-phase bosses + procgen mechanic mix | [combat-and-flight.md](./combat-and-flight.md), [technical-and-scope.md](./technical-and-scope.md) |
| Dual flight: free 3D (Avorion) + on-rails (Star Fox) | [combat-and-flight.md](./combat-and-flight.md), [core-loop-and-modes.md](./core-loop-and-modes.md), [technical-and-scope.md](./technical-and-scope.md), [vision-and-pillars.md](./vision-and-pillars.md) |
