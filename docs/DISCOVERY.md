# DISCOVERY — Project UMBRA (Batch 1)

Status: **AWAITING OWNER ANSWERS** (sent 2026-10-27)

Answer by ID, e.g. `A1: b, A4: option 1 but warmer, C2: no grabs`. Anything you skip uses the
**default** shown, recorded as PROVISIONAL in `DECISIONS.md` and revisited before it is final.
Batch 2 (detailed balance numbers, monetization specifics, boss and dungeon design) comes after
the vertical-slice character is chosen.

---

## A. Identity, IP and art direction

**A1. Release intent.** (a) private prototype for you and friends, (b) public free release,
(c) public and monetized. *Default: (b). Any public release needs the original-identity rules.*

**A2. Original identity.** Do you approve building an original world in the hunter, gate and
shadow genre, with no Solo Leveling names, characters, logos, music or art in the shipped game?
Working title options (placeholders; you choose or propose your own):
- **GATEFALL**: gates have collapsed over a modern city and hunters fight over the ruins.
- **Umbral Ascent**: the climb from weakest hunter to shadow-wielder.
- **Rankbreaker**: a ranking system exists to be broken.

*Default: yes, with internal codename "Project UMBRA" until you pick a title.*

**A3. Tone.** (a) grim and cinematic, (b) flashy, stylized anime hype, (c) a mix: dark world,
explosive combat. *Default: (c).*

**A4. Art direction.** Choose one, combine them, or reject all three.

| Option | Look | Tradeoff |
|---|---|---|
| 1. Neon Abyss | Near-black environments, cold rim light, saturated violet and blue shadow energy, crisp white "system" UI panels | Closest to the inspiration's mood. Bloom-heavy, so it needs careful tuning for mobile. |
| 2. Ashen Monochrome | Desaturated grey and black world, white highlights, one accent colour per character | Very readable combat with a distinct identity. Less colourful in thumbnails. |
| 3. Fractured City | Realistic ruined modern city at dusk, warm practical lights against cold rift light | Strongest sense of place. Highest asset and performance cost. |

**A5. The image already in this repo** (`0e630fa0…jpg`, a white feathered wing on black). Is it
a reference for this game? If so, what does it represent: a character motif, UI or logo mood,
a light-against-shadow theme, or something else? Do you have rights to use it in game?
*Default: treated as mood reference only, never shipped.*

## B. Modes and emphasis

**B1. Emphasis for the first release.** (a) PvP battlegrounds first, PvE added later,
(b) balanced, (c) PvE dungeons first plus a PvP arena.
*Default: (a). The combat framework is shared, and PvP gives the smallest complete loop.*

**B2. Modes you want eventually** (pick any): free-for-all drop-in arena, 1v1 duels, team
battles, co-op gate dungeon, raid boss, ranked. *Default for launch: FFA arena and 1v1 duels.
Gate dungeon is the first PvE mode.*

**B3. Players per server.** *Default: 12 for FFA, which keeps VFX load mobile-safe.*

## C. Combat feel

**C1. Pace.**
- (a) Fast and aggressive: short combos, frequent dashes, about 20–40 s to KO. Typical
  battlegrounds feel.
- (b) Methodical: fewer, heavier hits and big punishes, about 45–90 s to KO.
- (c) Hyper-fast aerial: long air combos, anime-fighter style. Hardest to balance, and most
  affected by latency.

*Default: (a).*

**C2. Mechanics to include.** For each, say yes, no or later: 4-hit M1 chain, block,
perfect block/parry, dash with i-frames, sprint, launcher plus air combo, ground slam,
wall bounce, ragdoll knockdown, combo breaker (burst escape), grabs or command throws,
counters, clashes (simultaneous hits cancel).
*Default: all yes except grabs (later) and clashes (later).*

**C3. Targeting.** (a) free aim in the camera direction, (b) soft lock that magnetises to the
nearest target in a cone, (c) hard lock-on toggle. *Default: (b), plus optional (c) on controller.*

**C4. Cinematic ultimates.** May an ultimate take control of the camera?
(a) attacker and victim only, at most 3 s, (b) all players nearby, (c) never, effects only.
*Default: (a). Nobody else loses control in PvP.*

**C5. Latency philosophy.** Roblox ping is often 60–200 ms.
- (a) favour the attacker (lag compensation): hits feel responsive, and defenders are sometimes
  hit "after" they dodged.
- (b) favour the defender: dodges feel fair, hits feel delayed.

*Default: (a), with rewind capped at 200 ms. Parry windows of at least 150 ms, because frame-tight
windows don't survive network jitter.*

**C6. Violence level.** *Default: no blood or gore, which keeps the Roblox maturity label low.
Impacts read through light, sound and debris instead.*

## D. Characters and kits

**D1. Structure.** (a) original named hunters with fixed kits, (b) classes (assassin, knight,
mage and so on), (c) build-your-own from weapon and skill pools. *Default: (a). Fixed kits are
easiest to balance and to give strong animation identities.*

**D2. Kit format.** *Default: 4-hit M1 chain, 4 skills, 1 ultimate charged by a meter, 1 passive,
plus universal block, dash and burst.*

**D3. Roster.** *Default: 1 character in the vertical slice, 3 at first public release.*

**D4. Concept pitches** (original; pick one for the vertical slice, and approve, edit or reject
each). After you choose, I'll send a full moveset with frame data before building anything.
- **Umbral Stalker**: twin daggers, close-range rushdown. Shadow-step teleports behind a marked
  target. Passive: hits leave shadow marks. Ultimate: a short-lived surge of summoned shadow
  soldiers that strike in sequence. *Carries the core shadow fantasy without copying it.*
- **Rift Knight**: greatsword and armour. Slow, with super-armour on heavy swings, a launcher
  and a guard-break. Ultimate: tears a rift and cleaves through it. *An anchor for new players.*
- **Gatecaller**: ranged zoner. Opens small portals that fire projectiles from angles, and
  repositions through portals. Ultimate: a gate collapse that pulls enemies together.
  *Adds range and tests the projectile systems.*

*Default vertical-slice pick: Umbral Stalker.*

**D5. Shadow summons.** (a) signature mechanic of one character, (b) universal system that
every player unlocks, (c) PvE only. *Default: (a). AI allies in PvP are costly for performance
and balance.*

**D6. Transformations / awakening modes.** yes, no or later. *Default: later. Each one doubles
that character's animation and VFX work.*

## E. Animation, VFX and audio

**E1. Rig.**
- (a) R6: the battlegrounds standard, about twice as fast to animate, readable silhouettes.
- (b) R15: more expressive, more work.
- (c) custom rigged characters: highest quality, needs a modeller.

*Default: (a) R6.*

**E2. Who animates?** (a) you or a team member in Roblox Animation Editor or Moon Animator,
(b) commissioned animator, (c) Creator Store animations (check licence), (d) I write keyframe
data and procedural placeholders, and you publish them in Studio.
*Note: Roblox animations only play in an experience if the experience owner (you, or your
group) owns them.*

**E3. VFX fidelity.** (a) Roblox-native particles, beams and trails only, which I can author
fully in code, (b) plus custom flipbook textures and mesh effects, which need images and meshes
you create or license and upload. *Default: (a) for prototypes, (b) as the target for ultimates.*

**E4. Accessibility.** *Default: settings to reduce flashing, reduce camera shake, and an effects
quality slider are mandatory.*

**E5. Music direction.** (a) dark orchestral and electronic hybrid, (b) aggressive synth or
phonk, (c) rock or metal, (d) other. Source: Roblox Creator Store licensed library, commission,
or your own. *Default: (a), using Creator Store licensed tracks as placeholders.*

## F. Progression and monetization

**F1. Progression depth.** (a) none: pure skill, cosmetic unlocks only, (b) light: levels unlock
characters and cosmetics, (c) deep: hunter rank, stats, gear, dungeon loot.
*Default: (b) at launch, extendable to (c). Stats in PvP threaten fairness, so if you choose (c)
I'd propose PvE-only stats.*

**F2. Monetization.** (a) none for now, (b) cosmetics only, (c) cosmetics plus character
unlock shortcuts, (d) game passes with gameplay benefits. *Default: (a) now, (b) later.
I'll argue against pay-to-win in PvP.*

## G. Platforms and controls

**G1. Priority order** of PC, mobile and controller. *Default: PC for tuning, but mobile and
controller supported from the first combat slice, not bolted on later.*

**G2. Default PC binds** (to confirm): LMB = M1, 1–4 = skills, G = ultimate, F = block (hold),
Q = dash, R = burst, Shift = sprint, Space = jump, Ctrl = shift-lock toggle.

## H. Map

**H1. References.** Upload images into `references/<category>/` in this repo (architecture,
terrain, lighting, arena, dungeon, destruction, palette), or describe them. No references yet?
I'll offer original concepts for approval.

**H2. Setting.** (a) ruined modern city with a collapsed gate at its centre, (b) underground
dungeon temple, (c) hybrid: city arena hub plus dungeon instances behind gates.
*Default: (c), with the city arena built first.*

**H3. Scale.**
- (a) compact arena, about 300×300 studs: fights find each other, the most readable option.
- (b) medium, about 600×600 studs, with 3–4 sub-arenas.
- (c) large explorable hub.

*Default: (b).*

**H4. Destruction.** (a) none, (b) cosmetic debris and craters that heal, (c) destructible
props. *Default: (b). Full destruction is expensive on mobile and over the network.*

**H5. Time of day and weather.** *Default: night under a violet gate glow, light fog.*

## I. Production logistics

**I1. Studio and ownership.** Do you have Roblox Studio and an account? Should the experience be
owned by your account or by a Roblox group? *Recommendation: a group, so collaborators' assets
work in the game.*

**I2. Integration method.**
- (a) Rojo: this repo syncs live into Studio through the Rojo plugin, and I can also build a
  ready-to-open `.rbxl` place file.
- (b) a `.rbxl` or `.rbxm` file only, which you open or insert. No sync tooling needed.
- (c) copy-paste scripts by hand: not recommended at this scale.

*Default: (a), with (b) as the fallback.*

**I3. Existing assets or people.** Do you have animations, models, sounds, UI art, an animator,
a modeller or testers?

**I4. Repository.** Keep the project in `cgspiral/img` on this branch, or move it to a dedicated
repo? *Default: stay here for now.*

**I5. Open-source libraries.** May I use well-known MIT-style Roblox libraries, for example
ProfileStore for session-locked saving, after licence checks? *Default: yes, logged in
ASSET_REGISTER.*

**I6. Team, time and cadence.** Solo or team? A rough target date? How often do you want
check-ins?

**I7. Minor decisions.** May I decide minor details (exact UI spacing, internal names, file
layout) myself and log them as PROVISIONAL? *Default: yes.*
