# TASK BOARD — Project UMBRA

Updated 2026-10-27. Priority: P0 (blocking), P1, P2.

## Active
| ID | Task | WS | Priority | Notes |
|---|---|---|---|---|
| T-001 | Discovery Batch 1 answered by owner | — | P0 | `docs/DISCOVERY.md` |

## Blocked (waiting on owner)
| ID | Task | WS | Blocked by |
|---|---|---|---|
| T-010 | Full moveset spec, with frame data, for the vertical-slice character | WS2 | D4, C1, C2 |
| T-011 | Art direction mood board and palette sheet | WS3/WS6 | A3, A4 |
| T-012 | Map concept options (top-down sketches) | WS6 | H1–H5 |
| T-013 | Rojo project scaffold and bootstrap loaders | WS7 | I2 (toolchain) |

## Backlog: unblocked once the toolchain is chosen (no creative decisions inside)
| ID | Task | WS | Priority |
|---|---|---|---|
| T-020 | Net layer: remote registry, schema validators, rate limiter, with Lune tests | WS1 | P0 |
| T-021 | Character state machine (server) plus attribute mirroring | WS1 | P0 |
| T-022 | Move-definition schema and definition linter | WS1/WS2 | P0 |
| T-023 | Pure combat math: FrameData, DamageFormula, ComboScaling, with tests | WS1 | P0 |
| T-024 | Hitbox service with position history and lag compensation | WS1 | P1 |
| T-025 | InputController action map (keyboard/mouse, touch, gamepad) | WS4 | P1 |
| T-026 | DataService skeleton with versioned schema and migrations | WS5 | P1 |
| T-027 | VFX/audio cue API, pooling and quality tiers (placeholder visuals) | WS3 | P1 |
| T-028 | Greybox test-arena builder (PLACEHOLDER geometry) and training dummy | WS6 | P1 |
| T-029 | CI workflow (format, lint, tests, definition linter) | WS7 | P1 |
| T-030 | SessionStart hook to install the toolchain in cloud sessions | WS7 | P2 |

## Completed
| ID | Task | Date | Evidence |
|---|---|---|---|
| T-000 | Repo inspection, project documents scaffolded, discovery sent | 2026-10-27 | This commit |
