# TEST REPORT — Project UMBRA

Only checks that actually ran are recorded here. "Generated", "installed", "tested" and
"verified in game" are kept separate.

## Test environments
| Environment | What it can verify | Available? |
|---|---|---|
| Cloud dev container (Claude) | Formatting, linting, pure-Luau unit tests (Lune), definition linting, `rojo build` producing a place file | See toolchain check below |
| Owner's Roblox Studio | Engine behaviour, physics, animations, VFX, multi-client local server, MicroProfiler | Unknown (DISCOVERY I1) |
| Live private server / devices | Real latency, mobile performance, DataStores in production | Later (M9) |

## Toolchain check (2026-10-27, cloud container)
Installed from crates.io with `cargo install --locked`:

| Tool | Version | Result |
|---|---|---|
| StyLua | 2.6.0 | Installed and runs |
| Selene | 0.31.0 | Installed and runs |
| Lune | 0.11.1 | Installed. A smoke script ran successfully, including `@lune/roblox` `Vector3` math. |
| Rojo | 7.7.1 | Installed. A smoke project built to `.rbxl`, and Lune read the place back and found the ModuleScript at `ReplicatedStorage.Shared.Probe`. |

Note: the container is ephemeral, so these tools must be reinstalled in a new container
(about 10 minutes of compile time) until the SessionStart hook (T-030) exists.

## Test runs
None yet. No game code exists.

## Bug log
| ID | Found | Severity | Description | Status |
|---|---|---|---|---|
| — | — | — | — | — |
