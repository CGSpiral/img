# ASSET REGISTER — Project UMBRA

Rules:
- **Never invent asset IDs.** The `Roblox ID` column is filled only with IDs the owner has
  uploaded or verified. Until then the registry key resolves to a labelled placeholder.
- Animations only play in an experience when they are owned by the experience owner (the
  owner's account, or the group that owns the experience). Audio has similar permission rules.
  Upload under the same owner as the experience.
- Status values:
  - `needed`: required, not yet made
  - `placeholder`: temporary stand-in, labelled
  - `in-progress`
  - `uploaded`: has an ID, not yet verified in game
  - `verified`: tested working in the experience
  - `rejected`

## Assets on record

| ID | Asset | Type | Purpose | Source | Ownership / permission | Status | Roblox ID | Notes |
|---|---|---|---|---|---|---|---|---|
| AST-000 | `0e630fa032b44fe269c3c5a26c39afed.jpg` (white wing on black) | Image | Unknown, see REF-000 | Uploaded to repo by owner 2026-04-08 | **Unknown** | reference only | — | Never ship until the owner confirms rights |

## Open-source code (pending DISCOVERY I5)

| ID | Library | Use | Licence | Status |
|---|---|---|---|---|
| LIB-001 | ProfileStore (loleris) | Session-locked saving | To verify | proposed |

## Required asset categories (filled in as designs are approved)
- **Animations:** locomotion set, M1 chains, skills, ultimates, hit reactions, knockdown and
  get-up, block, parry, dash, NPC and boss sets.
- **VFX textures and meshes:** slash arcs, impact flipbooks, shockwave rings, shadow smoke,
  portals, ground cracks.
- **Audio:** per-move swing and impact sounds, footsteps, UI, ambience, music tracks.
- **UI art:** icons for skills and ultimates, HUD frames, menu backgrounds, logo (original).
- **Models:** modular city kit, gate and portal set pieces, dungeon kit, enemies, bosses.
