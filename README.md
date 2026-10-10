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

NODE brings your entire settlement network into one clear in-game dashboard. Open it from anywhere to compare settlements, review local needs, inspect residents, and manage supported assignments without travelling from workshop to workshop.

Settlement information stays ready while you play. Each save keeps its own last known settlements, settlers, and plots, so the dashboard opens right away after loading and keeps refreshing quietly in the background. There is no manual scan to run before it becomes useful.

> [!NOTE]
> NODE is in early development. Features will continue to grow, and community reports are an important part of improving compatibility and stability.

## Features

### 🌐 Network overview

- View every owned settlement in one place.
- Compare population, happiness, food, water, power, defense, and build budget.
- See city leaders and other important settlement totals at a glance.
- Quickly identify communities that need attention.

### 🏘️ Settlement overview

- Review essential workshop totals for the selected settlement.
- See the active SS2 city plan, city level, leader, and leader traits.
- Check pollution, cleanliness, caravan reach, shared caps, and virtual resources.
- Review SS2 plots by type and see the settlement's available local services.

### 🧱 Plots and Plot Profile

- Open the **Plots** tab to list every SS2 plot in a settlement with its type, name (building plan), owner, occupants (current and max), level, and size.
- Select a plot to open its **Plot Profile**: a preview of the plot's stage model, its occupants and their status, building plan progress, power, operating costs, and benefits and penalties with readable resource names.
- When the current stage's model can't be shown, another stage's model is used instead, or **Model Not Available**.
- While another settler action is still running, the plot's last known details show right away with a notice.
- Occupant names open their settler profile, and closing it returns to the plot.
- **Assign / Reassign** a settler from the same settlement. The picker highlights the SPECIAL stats SS2 uses for that building class and lists the best fit first. On full plots it offers to replace an occupant.
- **Refresh plot**, set its **Upgrade mode** (settlement default, automatic, or manual), or open SS2's **plot menu** or **building plan selector**. Demolish and scrap stay in SS2's own menu.

### 👥 Population and resident management

- Browse residents who count toward the settlement population, including humans, robots, dogs, and compatible modded actors.
- Keep livestock, defenses, and workshop equipment out of the population list.
- Review SPECIAL stats, resident type, sickness, Home, Job, and Hobby.
- See exact SS2 building-plan names when a resident is assigned to a plot.
- See vanilla beds, crops, shops, provisioner work, and other supported assignments when no SS2 plot applies.
- Filter for residents with no home, unemployed residents, and provisioners.
- Select a resident to open the centered **settler profile**:
  - **Info**: type, settlement, role, and bed, with a warning for a settler with no bed or no home.
  - **S.P.E.C.I.A.L.** with Skilled, Gifted, and Savant ranks.
  - **Home**, **Job**, and **Hobby** rows. A plot assignment opens its Plot Profile, and **Assign** opens a plot picker grouped by the assignments SS2 allows on each plot.
  - **Flags**: Commandable, Allow Move, and Allow Caravan.
  - **Actions**: Unassign bed, Unassign job, Unassign hobby, Move to Player, and Transfer to another settlement.
  - A **Status** section (health, vigor rating, rads, and ailments), shown once SS2's advanced settler functions are unlocked.
- Settler changes wait in a short queue and report a failure if they can't run, instead of being dropped.

### ⚙️ Settings and quality of life

- Press **Home** to open NODE and **Esc** to close it.
- Rebind the open key from the in-game Settings page.
- Choose the NODE theme or an alternate color theme.
- Scale the whole dashboard from Settings to fit your screen.
- Give generic settlers first names and surnames with the Settlers Renaming System. Unique named people are left alone, unnamed **Worker** settlers are included, and settlers named by other mods through quests keep their names. Each save keeps its own record of renamed settlers.
- With Nobody's Leaders 3 installed, the **Nobody's Leaders 3 compatibility** setting (on by default) leaves the names it gives settlers alone.
- Follow background work with the **Status Indicator**, a compact pill at the top of the menu. Select it for details on settlement updates, Sim Settlements updates, recent activity, and any wait on a settler change. It only redraws when something changes, and the **Status Indicator** setting hides it while background updates keep running.
- Adjust background refresh timing under **Settings → Systems → Scans System → Advanced**: native settlement audits every **120 seconds** and SS2 details every **180 seconds** by default, on separate schedules. Settings still on the old 30-second audit default move to 120 seconds once.
- Reduce interface animation for smoother use on large settlement networks.
- NODE appears in the Prisma Dock on the ESC menu.
- Optionally enable the Console page in Debug settings for status and troubleshooting.

## Sim Settlements 2 integration

NODE is not meant to replace Sim Settlements 2 systems or menus. It offers a cleaner, broader and faster way to use the features SS2 already provides.

NODE never changes or rewrites any SS2 scripts. Those stay untouched. It only calls what SS2 already exposes through its API and Papyrus.

No credit is claimed for SS2's features or functionality. Credit goes to Kinggath and the SS2 Team.

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

Install the dependency intended for your Fallout 4 runtime. Use the Old-Gen, Next-Gen, or Anniversary-compatible file offered by each dependency author where applicable.

### 🎮 Fallout 4

[![Supported Fallout 4 versions](https://img.shields.io/badge/FALLOUT_4-1.10.163_%7C_1.10.984_%7C_1.11.191%2B-78E89A?style=for-the-badge&labelColor=123C30&logo=steam&logoColor=D8F5D5)](https://store.steampowered.com/app/377160/Fallout_4/)

Supported runtimes: **1.10.163** (Old-Gen), **1.10.984** (Next-Gen), and **1.11.191 or newer** (Anniversary Edition).

### 🧩 Fallout 4 Script Extender

[![F4SE requirement](https://img.shields.io/badge/F4SE-MATCH_YOUR_GAME_VERSION-78E89A?style=for-the-badge&labelColor=123C30)](https://f4se.silverlock.org/)

Install the F4SE build made for your exact Fallout 4 runtime and always launch the game through F4SE.

### 📚 Address Library for F4SE Plugins

[![Address Library requirement](https://img.shields.io/badge/ADDRESS_LIBRARY-MATCH_YOUR_GAME_VERSION-78E89A?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/47327)

Choose the Address Library package that matches your Old-Gen, Next-Gen, or Anniversary runtime.

### 🖥️ PrismaUI F4

[![PrismaUI F4 version](https://img.shields.io/badge/PRISMAUI_F4-2.1.1-E7A83A?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/105454)

NODE currently targets **PrismaUI F4 2.1.1**.

### 🛠️ Workshop Framework

[![Workshop Framework version](https://img.shields.io/badge/WORKSHOP_FRAMEWORK-2.5.0%2B-2E8F79?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/35004)

Use **Workshop Framework 2.5.0 or newer**, including the author-provided Old-Gen replacer when required by your runtime.

### 🏙️ Sim Settlements 2

[![Sim Settlements 2 version](https://img.shields.io/badge/SIM_SETTLEMENTS_2-3.6.0%2B-2E8F79?style=for-the-badge&labelColor=123C30)](https://www.nexusmods.com/fallout4/mods/47976)

Use **Sim Settlements 2 3.6.0 or newer**. The base SS2 installation or the corresponding All Chapters Pack is supported.

> [!IMPORTANT]
> **NODE requires PrismaUI F4 2.1.1.**
>
> **`NODE.esp` is required and must be enabled.** It provides the companion quest used for SS2 settlement details and supported resident-management controls.

## Installation

### Mod Organizer 2 or Vortex — recommended

1. Install the required dependencies listed above for your game version.
2. Download NODE from [Nexus Mods](https://www.nexusmods.com/fallout4/mods/107925) or the [GitHub Releases page](https://github.com/NOBOBYoO/NODE/releases).
3. Install the archive with Mod Organizer 2 or Vortex.
4. Confirm that **`NODE.esp`** is enabled in your load order.
5. Launch Fallout 4 through **F4SE**.
6. Load your game and press **Home** to open NODE.

### Manual installation

1. Install all requirements first.
2. Open the NODE archive and copy its **`Data`** folder into the Fallout 4 installation folder.
3. Allow the NODE files to merge into the game's existing **`Data`** folder. Do not create a second `Data\Data` folder.
4. Enable **`NODE.esp`** with your preferred plugin manager.
5. Launch Fallout 4 through F4SE and press **Home** in-game.

### Updating NODE

Install the new version over the existing NODE installation and allow your mod manager to replace the older packaged files.

**NODE requires PrismaUI F4 2.1.1.**

`NODE.ini` is created automatically on first launch and is **not shipped in release archives**. Updating NODE therefore does not replace your existing preferences; newly introduced settings are added only when missing.

## Using NODE

1. Press **Home** while in-game to open the dashboard.
2. Use **Network Overview** to compare all owned settlements.
3. Use **Settlement Overview** to inspect one settlement in detail.
4. Open the **Population** tab to review residents, and select one to open their settler profile.
5. Open the **Plots** tab to review SS2 plots, and select one to open its Plot Profile.
6. Use **Settings** to change the open key, theme, Interface scale, settler renaming, refresh timing, motion, Status Indicator, and Console.
7. Press **Esc** to close NODE.

NODE begins building its settlement information after the game is ready. Large or heavily modded saves can take longer to complete their first network-wide update, but already prepared settlement information remains available as newer results arrive.

## Support and troubleshooting

- **Missing SS2 details:** Confirm that `NODE.esp`, Workshop Framework, and Sim Settlements 2 are enabled and that their versions match your game runtime.
- **NODE does not open:** Confirm that Fallout 4 was launched through F4SE and that PrismaUI F4 **2.1.1** is installed.
- **Interface hitching:** On a large save, enable **Reduce Animations**, or raise **Native settlement audit** and **SS2 detail refresh** under **Settings → Systems → Scans System → Advanced**.
- **Log location:** `Documents\My Games\Fallout4\F4SE\NODE.log`.

When reporting a problem, please include:

- Your exact Fallout 4 version.
- Your NODE version.
- `NODE.log`, `f4se.log`, and `PrismaUI_F4.log`.
- The affected settlement and clear reproduction steps, when applicable.

Please report issues through the [NODE Nexus Mods page](https://www.nexusmods.com/fallout4/mods/107925).

## AI usage disclosure

AI tools are used during NODE's development for automation, debugging, image generation, and implementation support. Design decisions, feature direction, review, testing, and release responsibility remain under the author's supervision.

## Credits

- **Workshop Framework** — [kinggath](https://www.nexusmods.com/fallout4/mods/35004)
- **Sim Settlements 2** — [kinggath and the Sim Settlements 2 Team](https://www.nexusmods.com/fallout4/mods/47976)
- **PrismaUI F4** — [StarkMP; Fallout 4 port by NomadsReach / Fallen World](https://www.nexusmods.com/fallout4/mods/105454)
- **Fallout 4 Script Extender (F4SE)** — [Ian Patterson, Stephen Abel, and Brendan Borthwick](https://f4se.silverlock.org/)
- **Address Library for F4SE Plugins** — [meh321](https://www.nexusmods.com/fallout4/mods/47327)

## Repository notice

This public repository contains NODE release information and approved downloadable packages. NODE's source code is maintained privately and is not distributed from this repository.

See [LICENSE](LICENSE) for the terms that apply to NODE's public release files.

---

<div align="center">
  <strong>NODE</strong><br>
  <sub>Your whole network of settlements, in one place.</sub><br><br>
  <a href="https://www.nexusmods.com/fallout4/mods/107925">Nexus Mods</a> ·
  <a href="https://github.com/NOBOBYoO/NODE/releases">Releases</a>
</div>
