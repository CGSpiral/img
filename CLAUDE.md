# CLAUDE.md — standing rules for every session on this project

This repository holds a Roblox anime battlegrounds game, internal codename **Project UMBRA**
(provisional, internal only; the public title has not been chosen). The project owner is the
creative director and makes all final design decisions.

## Start of every session
1. `git pull` the working branch (`claude/solo-leveling-roblox-game-1uhjzm` unless told otherwise).
2. Read `RESUME_HERE.md`, then `docs/DECISIONS.md` and `docs/TASK_BOARD.md`.
3. Continue from the recorded checkpoint. Do not restart completed work. Do not re-ask questions
   already answered in `docs/DECISIONS.md` or `docs/DISCOVERY.md`.

## Creative control (mandatory)
- Major creative decisions (art direction, characters, movesets, animation, VFX, audio, UI, map,
  bosses, progression, monetization, modes, balance philosophy) need explicit owner approval.
- Present options with tradeoffs, then ask. Log every approval, rejection and revision in
  `docs/DECISIONS.md`.
- Prototypes are allowed only when labelled `-- PLACEHOLDER (unapproved)` in code and marked
  PLACEHOLDER in docs. A prototype is never an approval.
- Movesets use the template in `docs/TEMPLATES.md` (name, input, function, range, startup,
  active, recovery, cooldown, damage, hitstun, knockback, counterplay, VFX, animation needs).

## Honesty rules
- Never invent Roblox asset IDs. Only record IDs the owner has verified (`docs/ASSET_REGISTER.md`).
- Never claim an animation, sound, model or map exists in the owner's experience unless verified.
- Keep generated, installed, tested and verified-in-game separate in all reports.
- Never fabricate test results. `docs/TEST_REPORT.md` records only checks that actually ran.

## IP rule
- The shipped game uses an original identity. No Solo Leveling names, characters, logos, music,
  artwork or designs in game content unless the owner documents permission in
  `docs/ASSET_REGISTER.md`. Genre tropes (hunters, gates, ranks, shadow magic) are fine;
  specific protected expression is not.

## Engineering rules
- One authoritative architecture: `docs/SYSTEM_ARCHITECTURE.md`. Update it when interfaces change.
- Server-authoritative combat: clients send intents, never hits, damage, currency or unlocks.
- Data-driven definitions (characters, moves, enemies) in `src/shared/Definitions`.
- No monolithic scripts. Explicit dependencies. Match existing naming and comment density.
- When a shared module changes, find and update every dependent file.

## End of every meaningful work session
Update `RESUME_HERE.md`, `docs/TASK_BOARD.md`, `docs/DECISIONS.md`, `docs/TEST_REPORT.md`
(and other docs touched), then commit and push.
