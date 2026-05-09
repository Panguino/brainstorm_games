# Roguelike progression

**Status:** Draft  
**Owners:** Both

## Run structure

<!-- Branching paths, stage count, biome order, bosses per run. -->

**Galactic layer (campaign)**

- **Outer rim → core:** progression is a **graph of sectors** (2D map); each visit or clear advances **inward** toward the **center** (see [core-loop-and-modes.md](./core-loop-and-modes.md)).
- **Node = mission slot:** types include **boss**, **pirate battle**, **mining**, **supernova escape**, **artifact**, **monument**, etc.—procgen and authored kits decide what **spawns** at each node. **Boss nodes** especially can use a **composer** that **stitches mechanic modules** into multi-phase fights ([combat-and-flight.md](./combat-and-flight.md)).

**Chris + team — ideas in play**

- Some **route nodes** are **time-pressure** encounters (clocked objective or escalating danger).
- Possible **artifact run**: acquire a macguffin, then **escape** with it (extraction beats normal “clear the corridor”).

## Randomization

<!-- What is seeded, what is authored, what is curated pools. -->

**Brad — direction**

- Push toward **procedural generation across the experience** (how far “everything” goes is a **scope and readability** call—rails + authored beats may still anchor the fantasy).

**Hybrid content model (Brad — Rust-inspired)**

- **Procgen “world glue”:** sectors, corridors between beats, encounter mix, loot—whatever varies run to run.
- **Fixed “monuments” (puzzles / setpieces):** **authored** chunks with **stable geometry and rules** so mastery carries across seeds (player learns the **water treatment plant**, not just *a* plant).
- **Variable placement:** each monument type may **not spawn** on a given run, and when it does it can sit at **different route positions** and **different facings / orientations** (or equivalent for 3D rails).
- **Payoff:** ties neatly to **secrets and achievements**—optional detours that reward **route knowledge** and repeat play without requiring new puzzle design every run.

## Build variety

<!-- Ship frames, loadouts, augments, synergies we want to enable. -->

**Chris — direction**

- **Customization depth** and player **choices** that support long-term “**math break**” builds (intentionally broken-feeling synergies).
- **Loot / rewards:** term **loot boxes** came up—treat as *open* until we pick a model (see Open questions).

**Brad — direction (Materia-style)**

- **Mods / items as growable kit:** FF7 **Materia**-style fantasy—slots on gear or ship, **experience or use-based leveling**, combine / evolve rules TBD.
- **Fit with Chris’s two-track power:** which materia-like things **reset each run** vs **persist** is an open design merge (could be: sockets fixed, gems found per run; or AP persists on account; etc.).

## Meta-progression

<!-- What persists after death; what we refuse to persist on principle. -->

**Two-track power (Chris)**

| Track | Dies with run? | Examples (placeholder) |
|-------|------------------|---------------------------|
| **Run pickups** | Yes | Skills, power-ups, temporary augments gathered during the run |
| **Permanent** | No | Unlocks from milestones, meta currency, account-wide options |

**Achievements → loadout cards (Chris)**

- Achievements unlock **cards** (or card-like picks).
- Those cards become options in a **pre-run loadout** (exact structure TBD: deck, slots, draft, etc.).

| Unlock type | Example | Feel (power vs variety vs story) |
|-------------|---------|-------------------------------------|
| Achievement card | e.g. “After X condition, add card Y to pool” | Variety + long-term goals |
| Permanent meta | TBD | Power curve must stay fair vs run-only spikes |
| Secret / hidden | TBD | Discovery, optional difficulty |
| Leveled mod (“Materia”) | Socketed item gains AP / tiers | Depth; must align with run vs meta rules (Brad) |

## Risk / reward optional layers

<!-- Risk cards, curses, bonus objectives, etc. -->

- **Secrets** tied to achievements or hidden conditions (Chris).
- **Achievement ladder (Brad + Chris):** some **easy** achievements for early hooks; some **extremely hard** for bragging rights / rare unlocks—avoid FOMO if they gate power (prefer cosmetics or optional cards).

## Failure and fairness

<!-- What deaths should feel fair vs dramatic; information standards. -->

## Open questions

- **Loot “boxes”:** cosmetic-only real money? gameplay drops only? no random paid—only authored / roguelike reward chests? Align before pitching or prototyping economy.
- How much **pre-run loadout** vs **pure discovery during run**? Cards might push toward more front-loaded planning—does that fight the Star Fox “on-rails flow” fantasy?
- **Artifact + escape** as its own mode, occasional node, or main campaign structure?
- **Procgen “everything” vs authored hero moments:** how much hand-authored spline / setpiece do we keep so the game still feels like Star Fox?
- **Materia persistence:** per-run gems only, account-wide leveled mods, or hybrid?
- **Monuments on rails:** how do we attach a **fixed-layout** puzzle to a **moving corridor** (branch spline, pocket volume, slow-rail “dock”) without breaking pacing?
