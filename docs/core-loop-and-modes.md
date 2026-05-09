# Core loop and modes

**Status:** Draft  
**Owners:** Both

## Macro loop — galactic map

**Campaign layer (Brad + team)**

- **Goal:** **race to the center of the galaxy** (spatial and narrative end state).
- **Map:** **2D sector graph**—**outer rim** nodes inward to **core** (Avorion-style **overworld** mental model: [Avorion](https://www.avorion.net/)).
- **Path structure (open design):**
  - **Open:** many branches; player charts their own inward spiral.
  - **Stricter:** frequent **A / B / C** forks (curated pacing, easier to balance).
  - **Hybrid:** open macro regions with **gated** chokepoints toward the core.
- **Multiplayer mix:** **solo**, **co-op**, **versus**, or **blended** rulesets—you may **encounter other players** while traversing sectors (session design TBD).

## Atomic loop (10–60 seconds)

<!-- Fly → read threats → act → reward feedback. Be specific. -->

## Run loop (full session)

<!-- Start → mid-run escalation → climax → death or win → between-run layer. -->

**Sector resolution:** picking or entering a **map node** launches a **mission** (rail corridor, pocket space, monument, etc.); clearing or failing it returns you to the **galaxy layer** (unless run ends).

**Dual flight systems ([combat-and-flight.md](./combat-and-flight.md))**

- **Free 3D flight** ([Avorion](https://www.avorion.net/)–style): strong candidate for **open space** sectors, **dogfights**, **mining fields**, or any **volume**-based node.
- **On-rails** (**Star Fox**–style tunnels / **fixed path** / **authored speed**): strong candidate for **monuments**, **setpiece bosses**, **escape** beats, and **tight readability** corridors.
- **Design work:** define which **node types** mandate which mode, whether **transitions** are seamless (one mission) or **hard cuts**, and how **PvP** behaves if players can be in different modes in the same sector (probably avoid—TBD).

**Time and objective pressure (brainstorm)**

- **Sector “rage” timer:** each sector (or level) has a **time budget**—hard fail, soft debuff, or boss spawn when time runs out (exact behavior TBD).
- **Stacking pressure:** timed **nodes** on the route can coexist with a sector timer (fun if readable; risk of “double clock” frustration—needs UX pass).

## Between-run / hub

<!-- Shop, upgrades, story, squad—whatever persists across runs. -->

## Modes

<!-- Campaign, arcade, daily, co-op lanes, etc. -->

| Mode | Purpose | In scope? |
|------|---------|-----------|
| **Galactic race (campaign)** | Rim → core progression on the **sector map** | Likely backbone |
| **Solo** | Single-player race / roguelike | Likely |
| **Co-op** | Shared map or shared missions | Discuss |
| **Versus** | Racing or fighting inward; contested nodes | Discuss |
| **Mixed** | PvE with **optional** PvP crossings or invasions | Discuss |
| **Artifact extract** | Find artifact → survive escape / delivery leg | Node type / contract |
| Standard run | Clear / survive route with roguelike build | Fits under sector missions |

**Sector node types (galaxy graph → mission theme)**

Each **node** can map to a mission template (one node might roll sub-type by seed):

| Node / mission theme | Pitch |
|----------------------|--------|
| **Boss** | Major setpiece; gate to next ring or rare loot—prefer **multi-phase** **mechanic + puzzle** flow ([World of Warcraft](https://worldofwarcraft.blizzard.com/)–style *structure*, flight-scale); **composed** from authored modules + procgen recipe ([combat-and-flight.md](./combat-and-flight.md)) |
| **Pirate battle** | Skirmish, ambush, or wave holdout |
| **Mining asteroids** | Resource / risk—time vs reward; environmental hazards |
| **Escape the supernova** | Timed escape / escalating hazard (pairs with sector timer ideas) |
| **Find the artifact** | Locate / extract macguffin (may chain with escape node) |
| **Time pressure** | Win or survive under a visible clock |
| **Artifact (mechanical)** | Pickup changes rules until delivered or run ends |
| **Monument / puzzle** | Authored **fixed** layout and solution (learnable); **spawn** and **placement** vary by seed—Rust-style optional branch (see [roguelike-progression.md](./roguelike-progression.md)) |
| (add more) | |

## Pacing targets

<!-- e.g. time to first interesting choice, run length goal. -->

- 

## Open questions

- **Sector timer + timed nodes:** if both exist, how do we keep telegraphs readable (one primary clock on HUD)?
- **Artifact extract:** standalone mode, random contract on the route, or campaign backbone?
- **Galaxy vs mission flow:** one **shared** galactic instance for all players on a server shard, or **instanced** missions with occasional **matchmaking** crossings?
- **Open map vs ABC paths:** which is default for v1 to ship faster?
