<div align="center">
  <a href="https://www.nexusmods.com/fallout4/mods/107925">
    <img src="https://staticdelivery.nexusmods.com/mods/1151/images/107925/107925-1787787810-2113693770.png" alt="NODE — Settlement Network Dashboard" width="820">
  </a>

  <h1>NODE — Settlement Network Dashboard</h1>

  <p>
    <strong>Your whole network of settlements, in one place.</strong><br>
    A fast in-game dashboard for Fallout 4 and Sim Settlements 2.
  </p>

  <p>
    <a href="https://www.nexusmods.com/fallout4/mods/107925"><img alt="Download on Nexus Mods" src="https://img.shields.io/badge/NEXUS_MODS-DOWNLOAD_NODE-E7A83A?style=for-the-badge&labelColor=030806&logo=nexusmods&logoColor=D8F5D5"></a>
    <a href="https://github.com/NOBOBYoO/NODE/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/NOBOBYoO/NODE?style=for-the-badge&label=LATEST_RELEASE&labelColor=123C30&color=78E89A"></a>
    <a href="https://github.com/NOBOBYoO/NODE/releases"><img alt="Release downloads" src="https://img.shields.io/github/downloads/NOBOBYoO/NODE/total?style=for-the-badge&label=DOWNLOADS&labelColor=123C30&color=2E8F79"></a>
  </p>

  <p>
    <a href="#overview">Overview</a> ·
    <a href="#features">Features</a> ·
    <a href="#sim-settlements-2-integration">SS2 Integration</a> ·
    <a href="#requirements">Requirements</a> ·
    <a href="#installation">Installation</a> ·
    <a href="#support-and-troubleshooting">Support</a>
  </p>
</div>

---

## Overview

NODE is an in-game dashboard for managing Fallout 4 settlements. Every settlement, settler and supply line across the Commonwealth, Far Harbor and Nuka-World comes together in one place, so the whole network can be checked and managed from anywhere instead of going workbench to workbench.

Sim Settlements 2 is a big part of it, too: city plans, plots, leaders and building classes all sit right alongside the rest. NODE updates its information automatically while playing and saves it with each save, so the dashboard is ready the moment a save loads.

> [!NOTE]
> NODE is still in early development. The network keeps growing, and community reports help shape its compatibility and stability.

## Features

### 🌐 Network overview

- Every owned settlement, in one place. The Network table columns can be sorted in either direction.
- Population, happiness, food, water, power, defense, and build budget can be compared side by side.
- City leaders and other important settlement totals are included.

### 🏘️ Settlement overview

- Workshop totals for the selected settlement.
- The active SS2 city plan, city level, leader, and leader traits.
- Pollution, cleanliness, caravan reach, shared caps, and virtual resources.
- SS2 plots by type, and the settlement's available local services.

### 🗺️ Network Map and supply lines

- The **Network Map** shows every owned settlement on the world map (Commonwealth, Far Harbor and Nuka-World) with its population, status and supply lines. Selecting a settlement opens an info box with its key stats.
- Far Harbor and Nuka-World appear as travel points with Pip-Boy-style icons once found, linked to the closest connected settlement; selecting one opens that region's map.
- The **Supply Line Manager** assigns, changes and removes supply lines. Lines left behind when a provisioner dies or leaves are cleaned up automatically. Managing lines requires rank 1 of the **Local Leader** perk, as in the base game.
- **Auto-Build Supply Lines** previews planned lines on the map, then builds them. The network grows from a hub, with one line from each settlement, and follows Logistics Station 2's settings when it is installed. By default it connects settlements that have no line; **Optimize network** plans the whole network again and only moves lines when the network gets clearly shorter. Duplicate and unlinked lines are repaired first and listed under **Line repairs**. **Link Far Harbor** and **Link Nuka-World** choose whether those regions join the network. Logistics Station 2 lines, Empire links and named settlers' lines are left alone. The preview lists settlers who would leave a job, with a **Keep job** option, and a summary lists new lines, provisioner sources and any settlement that can't be connected. A settlement's info box has **Set as hub** and **Connect**, the settler profile has **Keep off supply lines**, and **Settings > Network Map** sets the network style, which settlers may run lines, and **Auto-maintain**.
- **IDEK's Logistics Station 2** compatibility: its lines are shown read-only and left untouched, they are read shortly after a save loads, and **Ask ILS2 to rebuild** has it rebuild its own lines while the map follows along.
- A **Sim Settlements 2 Empire** layer shows Empire links and each settlement's Empire role once the save has an Empire.

### 🔔 Notifications

- Alerts on the status pill, an **Alerts** drawer with the last 100 events grouped by day, and an on-screen ticker while the dashboard is closed.
- Covers new settlements, city level-ups and leaders, plot construction and improvements, supply lines, scans, attacks and lost settlements, and settlers. Each type can be switched off under **Settings > Notifications**.

### 🧱 Plots and Plot Profile

- The **Plots** tab lists every SS2 plot in a settlement, with its type, name (building plan), owner, occupants (current and max), level, and size.
- Selecting a plot opens its **Plot Profile**: a preview of the plot's stage model, its occupants and their status, building plan progress, power, operating costs, and benefits and penalties with readable resource names.
- When the current stage's model can't be shown, another stage's model is used instead, or **Model Not Available**.
- While another settler action is still running, the plot's last known details show right away with a notice.
- Occupant names open their settler profile, and closing it returns to the plot.
- **Assign / Reassign** a settler from the same settlement. The picker highlights the SPECIAL stats SS2 uses for that building class and lists the best fit first. On full plots it offers to replace an occupant.
- **Refresh plot**, set its **Upgrade mode** (settlement default, automatic, or manual), or open SS2's **plot menu** or **building plan selector**. Demolish and scrap stay in SS2's own menu.

### 👥 Population and resident management

- Residents who count toward the settlement population, including humans, robots, dogs, and compatible modded actors.
- Livestock, defenses, and workshop equipment stay out of the population list.
- SPECIAL stats, resident type, sickness, Home, Job, and Hobby for each resident.
- Exact SS2 building-plan names when a resident is assigned to a plot.
- Vanilla beds, crops, shops, provisioner work, and other supported assignments when no SS2 plot applies.
- Filters for residents with no home, unemployed residents, and provisioners.
- Selecting a resident opens the centered **settler profile**:
  - **Info**: type, settlement, role, and bed, with a warning for a settler with no bed or no home.
  - **S.P.E.C.I.A.L.** with Skilled, Gifted, and Savant ranks.
  - **Home**, **Job**, and **Hobby** rows. A plot assignment opens its Plot Profile, and **Assign** opens a plot picker grouped by the assignments SS2 allows on each plot. Full plots can be picked, with a choice of who to replace. The list shows each plot's Building Class and Level, and the stat a hobby plot trains. Settlers Sim Settlements 2 won't allow on a plot are greyed out, with the stat they're missing.
  - **Flags**: Commandable, Allow Move, and Allow Caravan.
  - **Actions**: Unassign bed, Unassign job, Unassign hobby, Move to Player, and Transfer to another settlement. Transfer uses a settlement list and a confirm step. While a transfer is in progress the profile stays locked, with transferring and verifying status, until the transfer has been confirmed. Settlers with **Allow Move** turned off can't be transferred; **Move to Player** still works.
  - A **Status** section (health, vigor rating, rads, and ailments), shown once SS2's advanced settler functions are unlocked.
- Settler changes wait in a short queue and report a failure if they can't run, instead of being dropped.

### ⚙️ Settings and quality of life

- Press **Home** to open NODE and **Esc** to close it.
- Holding **N** for 3 seconds opens NODE even if the open key is taken by another mod, and a notice appears when that seems to be the case.
- The open key can be rebound from the in-game Settings page.
- The NODE theme or an alternate color theme can be chosen in Settings.
- The whole dashboard can be scaled from Settings to fit the screen.
- The **Settlers Re-Naming System** gives generic settlers first names and surnames. Unique named people are left alone, unnamed **Worker** settlers are included, and settlers named by other mods through quests keep their names. Each save keeps its own record of renamed settlers.
- With Nobody's Leaders 3 installed, the **Nobody's Leaders 3 compatibility** setting (on by default) leaves the names it gives settlers alone.
- The **Status Indicator** is a compact pill at the top of the menu for following background work. Selecting it shows details on settlement updates, Sim Settlements updates, recent activity, and any wait on a settler change. It only redraws when something changes, and the **Status Indicator** setting hides it while background updates keep running.
- Background refresh timing can be adjusted under **Settings → Systems → Scans System → Advanced**: native settlement audits every **120 seconds** and SS2 details every **180 seconds** by default, on separate schedules. Settings still on the old 30-second audit default move to 120 seconds once.
- Interface animation can be reduced for smoother use on large settlement networks.
- NODE appears in the Prisma Dock on the ESC menu.
- Settings are grouped into collapsible cards with jump buttons.
- The compass, crosshair and other on-screen elements are hidden while the dashboard is open.
- The optional **Console** page (turned on in Settings) shows versions, scan health and a filterable, searchable log.

### 🐞 Bug reports and data export

- **Report a bug** (Console page and Settings) builds a report with versions, loaded F4SE plugins, key mods, settlement and supply line status, recent scans, settings, recent Console lines and the end of `NODE.log`. **Copy** puts it on the clipboard and **Save to file** writes it to `Documents/My Games/Fallout4/NODE/reports`.
- **Export Data**: **Export now** and optional **Auto-export on save** write settlements, settlers, plots and supply lines to JSON and CSV under `Documents/My Games/Fallout4/NODE/export`.

## Sim Settlements 2 integration

NODE builds on what Sim Settlements 2 already offers. It reads SS2's data, like plots, building classes, leaders and city plans, through the functions SS2 provides, and never changes or replaces any of SS2's own code or features. The goal isn't to stand in for SS2, just to give it a clearer, more informative view.

NODE isn't affiliated with or endorsed by the Sim Settlements 2 team. The building-class icons come from SS2's own assets, and all credit for them goes to the SS2 Team members who made them.

When the information is available, NODE shows:

- Applied city plans and city levels.
- City leaders and their major, minor, and weakness traits.
- Residential, agricultural, industrial, martial, municipal, commercial, and recreational plot totals.
- Exact building-plan names for resident Home, Job, and Hobby assignments.
- Every plot's building plan, owner, occupants, level, and size, plus the Plot Profile details and actions listed above.
- The settler profile's Status section, shown once SS2's advanced settler functions are unlocked.
- Pollution and cleanliness.
- Clinic, hospital, sanitation, cemetery, communications, and caravan service coverage.
- Caravan reach, shared caps, virtual storage, and material categories.

## Requirements

Install the dependency intended for the Fallout 4 runtime in use. Use the Old-Gen, Next-Gen, or Anniversary-compatible file offered by each dependency author where it applies.

### 🎮 Fallout 4

[![Supported Fallout 4 versions](https://img.shields.io/badge/FALLOUT_4-1.10.163_%7C_1.10.984_%7C_1.11.191%2B-78E89A?style=for-the-badge&labelColor=123C30&logo=steam&logoColor=D8F5D5)](https://store.steampowered.com/app/377160/Fallout_4/)

Supported runtimes: **1.10.163** (Old-Gen), **1.10.984** (Next-Gen), and **1.11.191 or newer** (Anniversary Edition).

### 🧩 Fallout 4 Script Extender

[![F4SE requirement](https://img.shields.io/badge/F4SE-MATCH_YOUR_GAME_VERSION-78E89A?style=for-the-badge&labelColor=123C30)](https://f4se.silverlock.org/)

Install the F4SE build made for the exact Fallout 4 runtime in use, and always launch the game through F4SE.

### 📚 Address Library for F4SE Plugins

[![Address Library requirement](https://img.shields.io/badge/ADDRESS_LIBRARY-MATCH_YOUR_GAME_VERSION-78E89A?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/47327)

Choose the Address Library package that matches the Old-Gen, Next-Gen, or Anniversary runtime.

### 🖥️ PrismaUI F4

[![PrismaUI F4 version](https://img.shields.io/badge/PRISMAUI_F4-2.1.1-E7A83A?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/105454)

NODE currently targets **PrismaUI F4 2.1.1**.

### 🛠️ Workshop Framework

[![Workshop Framework version](https://img.shields.io/badge/WORKSHOP_FRAMEWORK-2.5.0%2B-2E8F79?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/35004)

Use **Workshop Framework 2.5.0 or newer**, including the author-provided Old-Gen replacer when the runtime needs it.

### 🏙️ Sim Settlements 2

[![Sim Settlements 2 version](https://img.shields.io/badge/SIM_SETTLEMENTS_2-3.6.0%2B-2E8F79?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/47976)

Use **Sim Settlements 2 3.6.0 or newer**. The base SS2 installation or the corresponding All Chapters Pack is supported.

> [!IMPORTANT]
> **NODE requires PrismaUI F4 2.1.1.**
>
> **`NODE.esp` is required and must be enabled.** It provides the companion quest used for SS2 settlement details and supported resident-management controls.

Optional: **IDEK's Logistics Station 2** and **Nobody's Leaders 3** are detected automatically when installed.

## Installation

### Mod Organizer 2 or Vortex — recommended

1. Install the required dependencies listed above for the game version in use.
2. Download NODE from [Nexus Mods](https://www.nexusmods.com/fallout4/mods/107925) or the [GitHub Releases page](https://github.com/NOBOBYoO/NODE/releases).
3. Install the archive with Mod Organizer 2 or Vortex.
4. Confirm that **`NODE.esp`** is enabled in the load order.
5. Launch Fallout 4 through **F4SE**.
6. Load a save and press **Home** to open NODE.

### Manual installation

1. Install all requirements first.
2. Open the NODE archive and copy its **`Data`** folder into the Fallout 4 installation folder.
3. Allow the NODE files to merge into the game's existing **`Data`** folder. Do not create a second `Data\Data` folder.
4. Enable **`NODE.esp`** with a plugin manager.
5. Launch Fallout 4 through F4SE and press **Home** in-game.

### Updating NODE

Install the new version over the existing NODE installation and allow your mod manager to replace the older packaged files.

**NODE requires PrismaUI F4 2.1.1.**

`NODE.ini` is created automatically on first launch and is **not shipped in release archives**. Updating NODE therefore does not replace existing preferences; newly introduced settings are added only when missing.

## Using NODE

1. Press **Home** while in-game to open the dashboard.
2. Use **Network Overview** to compare all owned settlements.
3. Use **Settlement Overview** to inspect one settlement in detail.
4. Open the **Population** tab to review residents, and select one to open their settler profile.
5. Open the **Plots** tab to review SS2 plots, and select one to open its Plot Profile.
6. Open the **Network Map** to see settlements and supply lines, manage lines, or run **Auto-Build Supply Lines**.
7. Use **Settings** to change the open key, theme, Interface scale, settler renaming, notifications, data export, refresh timing, motion, Status Indicator, and Console.
8. Press **Esc** to close NODE.

NODE begins building its settlement information after the game is ready. Large or heavily modded saves can take longer to complete their first network-wide update, but already prepared settlement information remains available as newer results arrive.

## Support and troubleshooting

- **Missing SS2 details:** Check that `NODE.esp`, Workshop Framework, and Sim Settlements 2 are enabled, and that their versions match the game runtime.
- **NODE does not open:** Check that Fallout 4 was launched through F4SE and that PrismaUI F4 **2.1.1** is installed.
- **Interface hitching:** On a large save, enable **Reduce Animations**, or raise **Native settlement audit** and **SS2 detail refresh** under **Settings → Systems → Scans System → Advanced**.
- **Log location:** `Documents\My Games\Fallout4\F4SE\NODE.log`.

When reporting a problem, use **Report a bug** (Console page or Settings) and save the report. It includes the game, F4SE and NODE versions, loaded plugins and the end of `NODE.log`. Please attach it together with:

- `f4se.log` and `PrismaUI_F4.log`.
- The affected settlement and clear reproduction steps, when applicable.

Please report issues through the [NODE Nexus Mods page](https://www.nexusmods.com/fallout4/mods/107925).

## AI usage disclosure

AI tools are used during NODE's development for automation, debugging, image generation, and implementation support. Design decisions, feature direction, review, testing, and release responsibility remain under the author's supervision.

## Support

Support for continued development is welcome on Ko-fi.

<a href='https://ko-fi.com/Z7Z028MXCC' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi3.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

## Credits

- **Workshop Framework** — [kinggath](https://www.nexusmods.com/fallout4/mods/35004)
- **Sim Settlements 2** — [kinggath and the Sim Settlements 2 Team](https://www.nexusmods.com/fallout4/mods/47976)
- **PrismaUI F4** — [StarkMP; Fallout 4 port by NomadsReach / Fallen World](https://www.nexusmods.com/fallout4/mods/105454)
- **Fallout 4 Script Extender (F4SE)** — [Ian Patterson, Stephen Abel, and Brendan Borthwick](https://f4se.silverlock.org/)
- **Address Library for F4SE Plugins** — [meh321](https://www.nexusmods.com/fallout4/mods/47327)

## Repository notice

This public repository holds NODE's release information and the approved downloadable packages. The source code is kept privately and isn't distributed from here.

See [LICENSE](LICENSE) for the terms that apply to NODE's public release files.

---

<div align="center">
  <strong>NODE</strong><br>
  <sub>Your whole network of settlements, in one place.</sub><br><br>
  <a href="https://www.nexusmods.com/fallout4/mods/107925">Nexus Mods</a> ·
  <a href="https://github.com/NOBOBYoO/NODE/releases">Releases</a>
</div>
