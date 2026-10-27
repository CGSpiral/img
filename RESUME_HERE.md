# RESUME HERE — Project UMBRA

**Last updated:** 2026-10-27
**Repo / branch:** `cgspiral/img` · `claude/solo-leveling-roblox-game-1uhjzm`

## Current state
- **Phase:** M0 Discovery. Waiting for the owner's answers to `docs/DISCOVERY.md` (Batch 1).
- **Game code:** none yet. Nothing has been built in Roblox Studio. No assets uploaded.
- **Documents:** draft versions created in `docs/` (bible, roadmap, architecture, asset
  register, references, task board, decisions, test report, templates, discovery).
- **Repo contents before this project:** one image, `0e630fa0…jpg` (white wing on black).
  Logged as REF-000 / AST-000, purpose unknown.

## Last completed action
Scaffolded the project documents and sent the discovery questions (task T-000).

## Next actions (in order)
1. Record the owner's discovery answers in `docs/DECISIONS.md` and update `PROJECT_BIBLE.md`.
2. If the toolchain is approved: scaffold the Rojo project (T-013), then the unblocked
   foundation tasks T-020…T-023 with tests.
3. Write the full moveset spec sheet for the chosen vertical-slice character (T-010) and send
   it for approval.
4. Send the art-direction mood and palette sheet (T-011) and map concept options (T-012).

## Approvals needed from owner
All of `docs/DISCOVERY.md` Batch 1. The most blocking items: A2 (identity), A4 (art
direction), C1 (pace), D4 (first character), E1 (rig), I2 (integration method).

## Blockers and environment notes
- **Push blocked (2026-10-27):** `git push` and the GitHub connector both return 403. Claude
  has read access to `cgspiral/img` but no write access. The commit exists only in the cloud
  container, and a copy of the docs was sent to the owner as a zip. Fix: reconnect GitHub at
  https://claude.ai/connect-github and install the Claude GitHub App on the repo. Then push
  the branch.
- This cloud environment's network policy blocks `create.roblox.com` (Roblox docs). The owner
  can allow it under Network access in the environment settings.
- The crates.io registry is reachable. StyLua, Selene, Lune and Rojo all install and work
  (details in `docs/TEST_REPORT.md`).
- The cloud container is ephemeral. Only committed and pushed work survives. Tools must be
  reinstalled in a new container until a SessionStart hook is added (T-030).
- Claude cannot open Roblox Studio, upload assets, playtest or see the rendered game. The
  owner does those steps.

## Copy-paste resume prompt
```
Resume Project UMBRA (my Roblox battlegrounds game) in repo cgspiral/img, branch
claude/solo-leveling-roblox-game-1uhjzm. First pull the branch and read CLAUDE.md,
RESUME_HERE.md, docs/DECISIONS.md and docs/TASK_BOARD.md. Don't restart finished work and
don't re-ask answered questions. Give me a status summary in under 10 lines and list the
approvals you still need from me, then continue with "Next actions". Commit and push after
each meaningful step.
```
