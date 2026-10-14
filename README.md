<p align="center">
  <img src="view/node-logo.png" alt="NODE" width="760">
</p>

<p align="center">
  <strong>Your whole network of settlements, in one place.</strong><br>
  A fast in-game dashboard for Fallout 4 and Sim Settlements 2.
</p>

# NODE — Settlement Network Dashboard

NODE gives you a live, network-wide view of every settlement you own. It keeps complete per-settlement snapshots ready in memory and in each save, so opening the dashboard or changing settlements paints cached information immediately instead of starting a new scan.

The visual identity follows the NODE palette:

| Role | Color | Hex |
| --- | --- | --- |
| Foundation | Black | `#030806` |
| Panels | Dark Green | `#123C30` |
| Structure | Teal | `#2E8F79` |
| Primary signal | Phosphor Green | `#78E89A` |
| Text | Pale Mint | `#D8F5D5` |
| Activity and warnings | Amber | `#E7A83A` |

## What NODE shows

### Network Overview

- Every owned settlement in one table.
- Total population, average happiness, and network-wide food, water, and power.
- City leaders, defense, build budget, and other key settlement totals.

### Settlement Overview

- Population, happiness, food, water, power, defense, beds, and build budget.
- Applied SS2 city plan and level, city leader, and leader traits.
- Pollution and cleanliness.
- SS2 plots by type and local service coverage.
- Caravan reach, caps, virtual storage, and material categories.

### Population

- Residents that contribute to the workshop Population counter, including humans, robots, dogs, and compatible modded actors. Non-population creatures and workshop objects are excluded.
- SPECIAL, type, sickness state, Home, Job, and Hobby for each resident.
- Exact SS2 building-plan names for plot assignments.
- Vanilla bed, farming, vendor, provisioner, and other assignment fallbacks.
- Filters for No Home, Unemployed, and Provisioners.

### Settler profile

Selecting a resident opens a centered settler profile:

- **Info**: type, settlement, role (Leader, Provisioner, or Settler), and bed, with a warning for a settler with no bed or no home.
- **S.P.E.C.I.A.L.**: each stat with its Skilled (5+), Gifted (8+), or Savant (10) rank.
- **Assignments**: Home, Job, and Hobby rows. A plot assignment opens its Plot Profile; **Assign** opens a picker of the settlement's plots, grouped by the assignments SS2 allows on them. Full plots are listed but can't be picked.
- **Flags**: Commandable, Allow Move, and Allow Caravan.
- **Actions**: Unassign bed, Unassign job, Unassign hobby, Move to Player, and Transfer to another settlement.
- A **Status** section (health, vigor rating, rads, and up to three ailments), shown once SS2's advanced settler functions are unlocked.

Settler changes wait in a short queue, so opening another settler or making another change before one starts doesn't drop it. A change that can't run reports a failure.

### Plots

- A **Plots** tab for each settlement lists every SS2 plot with its type, name (building plan), owner, occupants (current and max), level, and size, with filters for each plot type.
- Selecting a plot opens the **Plot Profile**:
  - a preview of the plot's stage model. When the current stage's model can't be shown, another stage's model is used instead, or **Model Not Available**;
  - occupants with their role and status. Names open their settler profile, and closing it returns to the plot;
  - building plan info: plan, size, level, build stage, occupancy, condition, power, and operating costs;
  - benefits and penalties with readable resource names.
- While another settler action is still running, the plot's last known details show right away with a notice.
- Plot actions: **Assign / Reassign** a settler from the same settlement (best SPECIAL fit first, with replace options on full plots), **Refresh plot**, **Upgrade mode** (settlement default, automatic, or manual), **Open SS2 plot menu**, and **Change building plan**. Demolish and scrap stay in SS2's own menu.

### Console and Settings

- A compact in-game event log for useful status and troubleshooting information. The Console page is off by default and can be turned on in Debug settings.
- Rebindable open key, NODE and alternate color themes, Interface scale, watermark and scan-line controls, and reduced motion.
- The **Status Indicator**: a compact pill at the top of the menu. Selecting it opens details on settlement updates and Sim Settlements updates, recent activity, and any wait on a settler change. It can be hidden with the **Status Indicator** setting without stopping background updates.
- Settlers Renaming System for generic settlers, with an option to name faction and group NPCs as well. Unnamed settlers called **Worker** are renamed too, and settlers named by other mods through quests keep those names. The record of renamed settlers is kept in each save, so turning renaming off restores the right names for that save.
- **Nobody's Leaders 3 compatibility**: shown only when Nobody's Leaders 3 is installed, on by default. Settlers that Nobody's Leaders 3 names keep those names.
- NODE appears in the Prisma Dock on the ESC menu.
- Adjustable background refresh timing for different system and save sizes.
- **Export network data** (Debug) writes the Network Overview rows to `Data\F4SE\Plugins\NODE\network-debug.json`.

## Fast, cache-first scanning

NODE handles workshop discovery, roster construction, classification, aggregation, caching, persistence, and UI serialization in native code. Papyrus is used only for SS2 or Workshop Framework properties and mutations that do not have a safe native equivalent. The script bridge submits raw forms, locations, and numeric values; native code performs the processing.

Default refresh timing:

- Settlement totals: every **15 seconds**.
- Changed settlement detail: **0.5 seconds** after a change. A changed settlement refreshes on its own, without restarting a totals refresh already in progress.
- Native settlement audit: every **120 seconds**.
- SS2 detail refresh: every **180 seconds**, on its own schedule. Full SS2 detail passes wait while a settler action is running.
- Settlements updated at once: **1**.

These values, plus **Pause Scans**, are under **Settings → Systems → Scans System → Advanced**. Settings still on the old **30-second** audit default move to 120 seconds once; custom values are kept. The Status Indicator can be hidden without disabling background refreshes.

Dashboard data is stored in each save's F4SE co-save and written only when the game saves. After loading a save, the dashboard opens with that save's last known settlements, settlers, and plots, then refreshes them in the background. Old per-character files in `Data\F4SE\Plugins\NODE\cache` are removed on launch.

## Requirements

- [Fallout 4 Script Extender (F4SE)](https://f4se.silverlock.org/)
- [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327)
- [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) **2.1.1**
- [Workshop Framework](https://www.nexusmods.com/fallout4/mods/35004)
- [Sim Settlements 2](https://www.nexusmods.com/fallout4/mods/47976)
- Fallout 4 **1.10.163** (Old-Gen), **1.10.984** (Next-Gen), or **1.11.191+** (Anniversary Edition)

> [!IMPORTANT]
> **NODE requires PrismaUI F4 2.1.1.**
>
> `NODE.esp` is required and must be enabled. It contains the small companion quest used for SS2-only metadata and supported settler actions. When it is disabled, the native plugin reports the missing requirement and does not repeatedly attempt partial scans.

## Installation

1. Install F4SE, Address Library, and PrismaUI F4 **2.1.1** for your game version.
2. Install Workshop Framework and Sim Settlements 2.
3. Install NODE with Vortex or Mod Organizer 2.
4. Enable `NODE.esp` in your load order.
5. Launch the game through F4SE. Press **Home** to open NODE and **Esc** to close it. The open key can be changed in Settings.

`NODE.ini` is created automatically on first launch and is not included in update archives. Existing values remain in place, while settings introduced by newer versions are appended when missing.

## Troubleshooting

- If SS2 information remains unavailable, first confirm that `NODE.esp`, Workshop Framework, and Sim Settlements 2 are enabled.
- If NODE does not open, confirm that Fallout 4 was launched through F4SE and that PrismaUI F4 **2.1.1** is installed.
- If the interface feels busy on a large save, enable **Reduce Animations**, or raise **Native settlement audit** and **SS2 detail refresh** under **Settings → Systems → Scans System → Advanced**.
- The in-game Console groups repeated warnings. The native log is written to the standard F4SE log location as `NODE.log`.
- When reporting a problem, include the game version, NODE log, load order, affected settlement, and reliable reproduction steps.

## Development

NODE is still evolving, but its runtime scanner, native cache, co-save persistence, UI, and bounded script bridge are structured for real saves and immediate menu rendering. See the [scan architecture](docs/native-scan-architecture.md) for the data boundary and consistency guarantees.

## AI usage disclosure

AI tools are used during development for automation, debugging, image generation, and implementation support. Design decisions, feature direction, review, testing, and release responsibility remain under the author's supervision.

## Sim Settlements 2 disclosure

NODE is not meant to replace Sim Settlements 2 systems or menus. It offers a cleaner, broader and faster way to use the features SS2 already provides.

NODE never changes or rewrites any SS2 scripts. Those stay untouched. It only calls what SS2 already exposes through its API and Papyrus.

No credit is claimed for SS2's features or functionality. Credit goes to Kinggath and the SS2 Team.

## Support

Support for continued development is welcome on Ko-fi.

<a href='https://ko-fi.com/Z7Z028MXCC' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi3.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

## Credits

- [Workshop Framework](https://www.nexusmods.com/fallout4/mods/35004) — kinggath
- [Sim Settlements 2](https://www.nexusmods.com/fallout4/mods/47976) — kinggath and the Sim Settlements 2 Team
- [PrismaUI F4](https://www.nexusmods.com/fallout4/mods/105454) — StarkMP; Fallout 4 port by NomadsReach / Fallen World
- [Fallout 4 Script Extender (F4SE)](https://f4se.silverlock.org/) — Ian Patterson, Stephen Abel, and Brendan Borthwick
- [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327) — meh321
