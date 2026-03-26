# Changelog

All notable changes to this package are documented here.
Format: [version] - date / what changed

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
