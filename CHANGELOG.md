# Changelog

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
- The dashboard uses Prisma 2.1's current view lifecycle: panel role, focus, Escape handling, and game-thread page events. Gamepad controller actions are not enabled yet and will come in a later update.
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
- **Fixed:** Loading a save no longer spams "Save cache skipped; character id was not ready yet." Saved settlement data now loads once the character id is available.



### 🔄 Changes

- Saved settlement data is restored as soon as a save loads, so NODE already has last session's picture before you open the dashboard.
- Settlement scans no longer start during save load but rather post-load, this should reduce the workload during save load.
- Console and log messages are now clearer to their porpuse and meaning
- Sim Settlements 2 detail traces now require Console Debug to be enabled, otherwise they would spam the console.



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
