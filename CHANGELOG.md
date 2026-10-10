# Changelog

## [0.6.0] - 2026-10-10

### ✨ Additions

- Added a **Plots** tab to each settlement. It lists every Sim Settlements 2 plot with its type, building plan, owner, occupants (current and max), level and size.
- Added the **Plot Profile** window, opened by selecting a plot. It shows the plot's stage model, its occupants and their status, building plan progress, power, operating costs, and its benefits and penalties with readable resource names. When the current stage's model can't be shown, another stage's model is shown instead, or **Model Not Available**. While another settler action is still running, the plot's last known details show right away with a notice. Occupant names open their settler profile, and closing it returns to the plot.
- Added **Assign / Reassign** to the Plot Profile, to pick a settler from the same settlement. The picker shows each settler's current job or home, highlights the SPECIAL stats SS2 uses for that building class, and lists the best fit first. On full plots it offers to replace an occupant, and an owner can be replaced outright or moved down to occupant.
- Added plot actions to the Plot Profile: refresh the plot, set its upgrade mode (settlement default, automatic or manual), and open SS2's plot menu or building plan selector. Demolish and scrap stay in SS2's own menu.
- Added a **Nobody's Leaders 3 compatibility** setting under the Settlers Renaming System. It only appears when Nobody's Leaders 3 is installed, and is on by default. Settlers that Nobody's Leaders 3 names after their settlement, such as Caroline Tenpines, keep those names everywhere, and any of them NODE renamed before get their Nobody's Leaders 3 name back.
- Added plot assignment to the settler profile. Settlers can be assigned to a home, job or hobby plot in their settlement, or moved from the one they have, without opening each plot first. The picker groups plots by the assignments Sim Settlements 2 allows on them, and full plots are listed but can't be picked. A home, job or hobby on a Sim Settlements 2 plot opens that plot's Plot Profile, and closing it returns to the settler.
- Added **Unassign hobby** to the settler profile, so a hobby plot can be freed the same way as a bed or job.
- Added a **Status** section to the settler profile, shown once Sim Settlements 2's advanced settler readings are unlocked: health, rads, vigor rating, and up to three ailments (injuries and diseases).
- Added a **Sim Settlements 2 disclosure** to the About page.

### 🔄 Changes

- Redesigned the settler profile. It now opens as a centered window, laid out like the Plot Profile, instead of the side panel, so everything about a settler is visible at once.
  - SPECIAL, info, assignments, flags and actions now sit side by side instead of in one long column.
  - The header shows the settler's name. An info column lists their type, settlement, role and bed, and flags a missing home or bed.
  - Home, job and hobby each have their own row, with buttons to open or change that plot.
  - Unassign, Move to Player and Transfer moved to an actions column on the right.
- Redesigned the **Scans Update Bar** as the **Status Indicator**, a compact pill at the top of the menu.
  - Settlement updates and Sim Settlements updates now show separately, with the current settlement, step and plots.
  - Selecting the pill opens details with recent activity and any waits on settler moves.
  - It only redraws when something changes, so the menu does less work while it is open.
  - Renamed its Settings toggle to **Status Indicator**.
- Changed native settlement audits and Sim Settlements 2 details to run on separate schedules: native audits every **120 seconds** and SS2 details every **180 seconds** by default, both under **Settings → Systems → Scans System → Advanced**. Full SS2 detail passes also wait while a settler action is running, so they no longer slow down settler changes.
- Changed the native audit setting to **120 seconds** for settings still on the old **30-second** default. This happens once, and custom values are kept.
- Changed settlement scans to skip repeated work, so background updates cost less during play. A changed settlement refreshes on its own instead of the whole list, Sim Settlements readings NODE already has are skipped, and the open settlement's plot details load faster.
- Changed where dashboard data is stored: each save's F4SE co-save, instead of one file per character, written only when the game saves. After loading a save, the dashboard opens right away with that save's own last known settlements, settlers and plots, then refreshes them in the background. Old files in **Data\F4SE\Plugins\NODE\cache** are removed on launch.
- Changed the Settlers Renaming System to keep its record of renamed settlers in each save instead of one file per character, so turning renaming off restores the right names for that save. Settlers who have died or left the game are dropped from the record, and an older save reads its character's old list once.

### 🛠️ Fixes

- Fixed loading an older save briefly showing settlements and settlers from a later point of the same character.
- Fixed the Population list showing **Settler** for settlers that other mods name through quests. Their given names now show.
- Fixed a settler change being dropped without notice when settler options were opened, or another change was made, before it started. Changes now wait in a short queue and report a failure if they can't run.
- Fixed the Settlers Renaming System skipping unnamed settlers called **Worker**, such as the ghouls at The Slog. They are now renamed with **Worker** kept in brackets, like faction settlers.

## [0.5.0] - 2026-09-25

### 🛠️ Fallout 4 1.10.163 Support Changes

> **Fallout 4 1.10.163** is now fully supported.
> Before this update, players on that version, could not load a save with NODE. The following notes represent what has changed to support this game version.
>
> OG is handled on its own internal module, separate from Next-Gen and Anniversary Edition, because some of NODE's systems froze that game version. Some of OG Settlement updates follow a different path than on newer versions, to avoid stalling the game.

- Settlements update one at a time instead of freezing the game shortly after load. The update bar shows the pass, waits **15 seconds**, then reads them again.
- Population Table and Settlers Renaming System only update as people move in or leave settlements.
- The **Caravan Network** card shows how many settlements are linked by provisioner routes, and a note that
- Full caravan resources are not supported on this game version. Shared caps, virtual storage, and material totals stay hidden. Next-gen and Anniversary Edition still show the full resource card.

> The following changes are general NODE changes like any other version:

### 🔄 Changes

- A full settlement read now takes about **3 seconds** while the dashboard is open, and about **10 seconds** while it is closed.
- If Sim Settlements details stop updating, NODE tries them again **30 seconds** later. Those details no longer stay off for the rest of the session. This would happen in cases where the player would stay IDLE in situations where the game timescale is set to 0.

### 🛠️ Fixes

- **Fallout 4 1.10.163** no longer freezes on the main menu when loading a save.
- The NODE badge now properly shows in the Prisma dock.

### 👊 Special Thanks

Thanks to these players for debugging and playtesting this version on Fallout 4 1.10.163:

- [tanmau](https://www.nexusmods.com/profile/tanmau?gameId=1151)
- [DarkZZZ](https://www.nexusmods.com/profile/DarkZZZ)

## [0.4.0] - 2026-09-21

### 🔄 Changes

- NODE now requires **PrismaUI F4 2.1.1**. Update Prisma before updating NODE; older Prisma UI builds are no longer supported.
- On a new game, the Network page now shows that no workshops are owned yet, and that settlement updates only start after a workshop is claimed.
- **Settlements Update Bar** is now **Scans Update Bar**.
- Settings → Systems now includes **Scans System**, with **Scans Update Bar** nested under it to show or hide the bar at the top of the menu.
- **Scans System** now includes an **Advanced** toggle for extra scan settings.
- Sub-settings now sit indented under their parent, including renaming, scans, and console.

### 🛠️ Fixes

- Starting a new game no longer stutters every couple of seconds. NODE was still checking for settlements every 2 seconds even though no workshops were owned yet.
- Turning off **Scans Update Bar** no longer shifts the dashboard up. The bar hides, and the space at the top stays in place.

## [0.3.0] - 2026-09-14

### ✨ Additions

- Introducing the **Settlers Renaming System**: generic settlers named Settler now get a gender-specific first name, and a surname. People in the same settlement may share a surname, so a few of them can feel like family. Unique named people are left alone.
- Added a **Settlers Renaming System** setting, to toggle the system. Turning off the system restores all settlers names to Settler again.
- Minutemen, Nuka-World gangs, and similar workshop groups can also receive names, with the group kept in parentheses. That option can be turned off on its own.
- Settings now include **Interface scale**, so you can make the whole dashboard smaller or larger to fit your screen resolution.
- Settler profiles now include **Unassign bed** and **Unassign job**, so you can free a bed or workplace without moving that person out of the settlement.
- NODE now appears in the **Prisma Dock** on the ESC menu, with the NODE badge, a short description, and a link to the Nexus page.

### 🔄 Changes

- The Console page is now off by default. Turn on **Enable Console** in Debug settings to show it in the sidebar. **Console debug mode** is nested under that setting, for extra diagnostic lines in the in-game console and NODE.log.
- Background settlement updates are gentler: NODE now refreshes settlement numbers every **15 seconds**, waits **0.5 seconds** after a change before updating that settlement's roster, and updates **one settlement at a time**. The full network check is still every **30 seconds**.

### 🌿 QoL Improvements

- Population table now sorts NPCs alphabetically.
- The **Settlements Update** setting is now labeled **Settlements Update Bar**, so it is clearer that it shows or hides the bar at the top of the menu.

## [0.2.0] - 2026-09-04

### 🔄 Changes

- NODE now requires **PrismaUI F4 2.1**. Update Prisma before updating NODE; older Prisma UI builds are no longer supported.
- The dashboard opens, closes, and takes keyboard input with Prisma 2.1. Gamepad controls are not included yet.
- Settlement Updates now shows what kind of refresh is running (totals, recent changes, a full check, or indexing) and how far it has got (for example **7 / 20**), instead of naming each workshop in turn.
- Heavy world checks now run when something actually changed, not on every routine pass, so longer play sessions stay smoother.

### 🛠️ Fixes

- **Fixed:** Greatly reduced hitches caused by background updates and constant updated UI paint
- **Fixed:** NODE now only updates the UI on actual value changes.

## [0.1.1] - 2026-08-31

### ✨ Additions

- Added a **Changelog** page as the last sidebar option.

### 🛠️ Fixes

- **Fixed:** A startup crash that could occur when using NODE with Fallout 4 versions 1.11.191 and 1.11.221.
- **Fixed:** Interface controls could become unreachable or unresponsive at high resolutions, including the Population tab at 4K.
- **Fixed:** The dashboard now maintains reliable input focus when opening or returning to it.
- **Fixed:** The Settlement Updates bar now fills left to right across the whole network instead of jumping to a few of the same settlements.
- **Fixed:** Opening the dashboard no longer wipes an in-progress update, so the bar keeps showing the current settlement.
- **Fixed:** Sim Settlements 2 details no longer hide the Settlement Updates bar while a network pass is running.
- **Fixed:** Loading a save no longer repeats a "character id was not ready" message. Saved settlement data loads once the character is available.

### 🔄 Changes

- Saved settlement data is restored as soon as a save loads, so last session's settlements are already there when the dashboard opens.
- Settlement updates wait until the save has finished loading, so loading a save is lighter.
- Console and log messages are clearer.
- Sim Settlements 2 detail lines appear in the console only when Console Debug is on.

### 🌿 QoL Improvements

- The changelog sits on a dark translucent panel so the text stays readable over the dashboard background.
- NODE now adapts text, controls, tables, navigation, the status panel, and background visuals for compact displays, 1440p, ultrawide, and 4K resolutions.
- Compact displays now reorganize settlement information and provide scrolling where needed to keep the complete population roster accessible.

### 👊 Special Thanks

I want to thank the following users for reporting issues and helping me test this new version:  

- @wysiwyg  
- @DarkZZZ  
- @tanmau

## [0.1.0] - 2026-08-27

- First beta release.

