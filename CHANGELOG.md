# Changelog

All notable changes to this package are documented here.
Format: [version] - date / what changed

---

## [1.0.7] - 2026-03-26
### Fixed
- Icon loading rewritten: fire all 16 requests in parallel via EditorApplication.update polling
- Removed broken Task.Run approach (unsafe for UnityWebRequest on main thread)
- Icon opacity raised 10% → 38%, scrim reduced 62% → 44% so icons are actually visible
- Icons enlarged 96px → 110px for better presence on screen

---

## [1.0.6] - 2026-03-26
### Changed
- Background now shows a live collage of GD game icons loaded from gamedistrict.co
- Icons tile in a brick-offset grid behind the card at 10% opacity
- Dark scrim (62%) over icons keeps card fully readable
- Diagonal hatch + yellow radial glow retained on top of icon layer
- Graceful: collage appears as icons load async, falls back to hatch-only offline

---

## [1.0.5] - 2026-03-26
### Changed
- Background overhauled to match gamedistrict.co website aesthetic
- Pure black base (#050505) replaces charcoal
- 45° diagonal hatch pattern tiled across bg (GD site visual signature)
- Subtle yellow radial glow at window center — mirrors GD hero sections
- Card surfaces darkened to contrast cleanly against the black bg

---

## [1.0.4] - 2026-03-26
### Changed
- Background replaced with pure black + subtle yellow dot-grid pattern
- "Scanning is free" text now white (was grey-on-grey, hard to read)
- Footer text opacity raised for legibility

---

## [1.0.3] - 2026-03-26
### Changed
- UI palette updated to match Game District logo exactly
- Background shifted from near-black to logo charcoal (#3A3A3A family)
- Accent yellow pinned to logo #FFD300
- Text updated to pure white matching logo wordmark

---

## [1.0.2] - 2026-03-26
### Fixed
- Added missing `.meta` file for `HOW_TO_PUBLISH_UPM.md`
- Added missing `.meta` file for `Editor/Resources/README.txt`
- Resolves "has no meta file, but it's in an immutable folder" errors in UPM

---

## [1.0.1] - 2026-03-26
### Fixed
- Added missing `.meta` files for `Editor/` folder and all `.cs` scripts
- Resolves "Asset has no meta file" errors when installing via UPM

---

## [1.0.0] - 2026-03-26
### Added
- Initial release
- SRP, OCP, LSP, ISP violation detection (regex-based, no Roslyn)
- Per-principle ratings 1–5 based on SOLID Easy Rating Guide
- AI-powered fix generation via Claude API
- Behavioral Contract Check — verifies public API preserved before applying fixes
- Moved method detection — SRP splits no longer flagged as removals
- PDF export — project summary + per-file detailed reports matching DriveToDeliver format
- Folder-scoped scanning — select specific Assets subfolder
- Game District checkpoint card UI theme (yellow/black)
- SDK file auto-exclusion (Adjust, AppMetrica, MaxSdk, Firebase, etc.)
- Settings button always visible in top bar
- Cost confirmation prompt before calling Claude API
- API key clear warning before removing key
