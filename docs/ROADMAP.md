# ROADMAP — Project UMBRA

Status: **DRAFT, awaiting owner approval** (2026-10-27). Milestone scope adjusts to the
answers in `DISCOVERY.md`.

## Principles
- Freeze shared interfaces first (move definitions, combat remote protocol, character state
  machine, VFX/audio cue API, animation registry, data schema). Workstreams build against them.
- Every gameplay feature ships as a full vertical cut: input → client prediction → remote →
  server validation → authoritative effect → replication → animation/VFX/audio → UI → tests.
- Placeholders are labelled. A milestone is "done" only on its acceptance criteria, with test
  evidence in `TEST_REPORT.md`, verified in Studio by the owner where it needs the engine.

## Milestones

| # | Milestone | Main outputs | Acceptance criteria |
|---|---|---|---|
| M0 | Discovery and pre-production | Discovery answers, project bible, approved pillars, vertical-slice character concept, toolchain choice | Batch-1 answers logged. Bible sections A–D approved. Toolchain chosen. |
| M1 | Technical foundation | Rojo project, service/controller loader, config system, Net layer (schema-validated, rate-limited remotes), character state machine, DataService skeleton, Lune unit tests, definition linter, CI, greybox test-arena builder, debug overlay | `rojo build` produces a place file. Two-player Studio test: spawn, state replicates, malformed or spammed remotes rejected and logged. All automated checks pass. |
| M2 | Combat vertical slice | 1 approved character with placeholder animations: M1 chain, block, dash, 2 skills. Server hit detection with lag compensation. Hitstun, knockback, cooldown HUD, training dummy, placeholder hit VFX and SFX. PC, touch and controller input. | Two players can fight a full round in a Studio local server. Exploit cases fail safely (invalid move, out-of-range, cooldown bypass, remote spam). Owner signs off on feel. |
| M3 | Combat depth and roster | Parry, air combos, launchers, ultimates and meter, combo scaling and anti-infinite rules, burst. Characters 2 and 3. Character select. | Every approved move matches its spec sheet. No infinite combo found in a scripted combo search. Owner approves balance pass 1. |
| M4 | Animation, VFX and audio production | Owned animations replace placeholders. VFX library with quality tiers and pooling. Cinematic ultimates. Sound and music mix. | Asset register shows every shipped asset owned or licensed, with verified IDs. Effects stay within the performance budget on a low-end mobile test. |
| M5 | Custom map | Pre-build package (8 items below), then greybox, art pass, lighting, streaming and performance tuning | Owner approves each phase. Spawn fairness and sightline checks pass. Map meets memory and FPS budget. |
| M6 | PvE | Enemy AI framework, telegraphs, gate dungeon instance, first boss with phases, summons if approved | Co-op dungeon is clearable by 1–4 players. AI is server-authoritative and stays within its CPU budget. |
| M7 | Progression and persistence | Data schema with migrations, XP, currency, unlocks, quests if approved. Save, retry and failure handling. | Join/leave/rejoin, server-shutdown and failed-save tests pass. No client-awarded value is possible. |
| M8 | UI/UX completion | Main menu, settings (graphics, audio, accessibility, binds), match results, kill feed, progression UI, mobile layout, controller navigation | Every screen is usable with mouse, touch and gamepad alone. Owner approves visuals. |
| M9 | Hardening and QA | Security audit, performance profiling, multiplayer stress test (Studio multi-client plus private live server), bug-fix pass | Bug log has no open blockers. Performance budgets are met. Security checklist passes. |
| M10 | Release | IP clean pass, maturity questionnaire guidance, monetization if approved, publishing guide, final report | Final report separates generated, installed, tested and verified-in-game work. Owner approves publish. |

## Dependencies
```
M0 ─► M1 ─► M2 ─► M3 ─► M4 ─────────────► M9 ─► M10
      │     │     └────► M6 (needs combat core)  ▲
      │     └──────────► M8 (HUD grows with each milestone)
      ├────────────────► M7 (schema early, features after M3)
      └─ M5 pre-build package runs in parallel from M1; greybox needs M2 movement metrics
```

## Parallel workstreams

| Workstream | Owns (files) | Starts | Depends on |
|---|---|---|---|
| WS1 Combat and networking | `src/shared/Combat`, `src/shared/Net`, `src/server/Services/Combat*`, `Hitbox*`, `Damage*` | M1 | Interfaces only |
| WS2 Characters and animation | `src/shared/Definitions/Characters`, `.../Moves`, `src/shared/Registry/AnimationRegistry` | M1 (schemas), M2 (content) | WS1 move schema |
| WS3 VFX and audio | `src/client/Controllers/VFX*`, `Audio*`, `src/shared/Registry/VFX*`, `Sound*` | M2 | Cue API (frozen in M1) |
| WS4 UI and controls | `src/client/Controllers/Input*`, `UI*`, `src/client/UI` | M1 | Action map, state attributes |
| WS5 AI and progression | `src/server/Services/AI*`, `Data*`, `Progression*` | M1 (data), M6 (AI) | Combat core for AI |
| WS6 Map and environment | `tools/map`, `references/`, map specs | M1 (pre-build docs) | Movement metrics from M2 |
| WS7 QA and optimization | `tests/`, `tools/lint`, CI, `TEST_REPORT.md` | M1 | Everything |

Ownership rule: one workstream owns each file. Cross-workstream changes go through the
interface in `SYSTEM_ARCHITECTURE.md` and are recorded there.

## M5 map pre-build package (required before final construction)
1. Top-down layout (SVG, to scale in studs)
2. Landmark and zone list
3. Traversal and spawn plan
4. Arena and combat-space dimensions
5. Lighting and atmosphere spec (Lighting, Atmosphere, Sky, post-processing values)
6. Modular building and environment asset list
7. Performance and streaming strategy (StreamingEnabled settings, part and triangle budgets)
8. Construction and validation checklist
