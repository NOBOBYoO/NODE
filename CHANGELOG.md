# Changelog

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
