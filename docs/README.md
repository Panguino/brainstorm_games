# Planning docs (working title: Star Fox–style roguelike)

Use this folder as the single place for design intent, open questions, and agreed decisions. Prefer short bullets; move settled calls into **Decisions** sections or into `decisions.md`.

**Working spine:** **race to the center of the galaxy** on a **2D sector map** (rim → core), with sector nodes becoming missions—see [core-loop-and-modes.md](./core-loop-and-modes.md) and [world-and-narrative.md](./world-and-narrative.md).

## Doc map

| File | Purpose |
|------|---------|
| [vision-and-pillars.md](./vision-and-pillars.md) | Pitch, audience, pillars, explicit non-goals |
| [core-loop-and-modes.md](./core-loop-and-modes.md) | Run structure, session flow, game modes |
| [combat-and-flight.md](./combat-and-flight.md) | Movement, camera, weapons, enemies, bosses |
| [roguelike-progression.md](./roguelike-progression.md) | RNG, routes, unlocks, meta, difficulty |
| [world-and-narrative.md](./world-and-narrative.md) | Setting, tone, characters, chapter themes |
| [technical-and-scope.md](./technical-and-scope.md) | Engine, team capacity, cut lines, prototypes |
| [decisions.md](./decisions.md) | Decision log (what we chose and why) |
| [ideas-inbox.md](./ideas-inbox.md) | Raw ideas before triage |

## Conventions

- **Owner** fields: `Brad`, `Chris`, or `Both`.
- **Status**: `Draft`, `Discussing`, `Agreed`, `Cut`, `Later`.
- When something graduates from inbox to design, copy it into the right doc and link back to the inbox line if useful.
