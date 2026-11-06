# Changelog

All notable changes to this project are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

## [0.1.12] - 2026-11-06

### Changed
- Updated the slicer API wrapper to the version BamBuddy 1.3.0 asks for. The Slice dialog now also lists the filaments Bambu Studio keeps in brand subfolders, such as COEX and SUNLU: 1928 Bambu filaments instead of 1792. Update this App when you update BamBuddy to 1.3.0 ([maziggy/bambuddy#3234](https://github.com/maziggy/bambuddy/issues/3234)).
- **The automatic filament pick can change.** When several presets fit a plate equally well, the wrapper now lists real filaments before support materials and Bambu Lab's own first, so some plates get a different pick, for example Generic PA instead of Bambu Support For PA/PET. Check the filament in the Slice dialog if you relied on the old pick.

### Fixed
- Your own presets based on a filament in a brand subfolder now slice with all the settings they inherit, and a printer preset saved under a name of its own now slices ([maziggy/bambuddy#3234](https://github.com/maziggy/bambuddy/issues/3234), [maziggy/bambuddy#3250](https://github.com/maziggy/bambuddy/issues/3250)).

## [0.1.11] - 2026-09-29

### Added
- The App documentation now states the upstream licenses: the wrapper is AGPL-3.0 and its source is linked from `DOCS.md`, while the Bambu Studio CLI follows Bambu Lab's own terms. The packaging in this repository stays MIT.
- The image now carries an OCI license label, `MIT AND AGPL-3.0-only`, covering both the MIT packaging and the AGPL-3.0 wrapper it ships.

### Fixed
- The link to the upstream fork pointed at a repository that does not exist (`ha-app-bambu-stdio-api`), so the attribution led nowhere.

### Changed
- The repository moved to the GitHub username `giorgioparri` (previously `naked-head`) and the container image is now published as `ghcr.io/giorgioparri/ha-app-bambu-studio-api-{arch}`. Nothing to do — this update pulls from the new location on its own, and GitHub redirects the old repository URL. If you are adding the repository for the first time, use `https://github.com/giorgioparri/homeassistant-addons`.
- Documentation uses "App" throughout, following Home Assistant's 2026.2 rename of add-ons.

## [0.1.10] - 2026-08-21
Bump Bambu Studio from 02.08.02.60 to 02.08.02.61.

## [0.1.9] - 2026-08-15
Bump Bambu Studio from 02.07.01.62 to 02.08.02.60.

## [0.1.8] - 2026-06-23
- Bump Bambu Studio from 02.07.01.57 to 02.07.01.62.

## [0.1.7] - 2026-06-22
- Revert Bambu Studio from 02.07.01.62 to 02.07.01.57: v02.07.01.62 ships no Linux AppImage.
- Harden AppImage URL detection: match any Ubuntu asset instead of pinning to `ubuntu-22.04` naming.
- Add explicit error message when no AppImage asset is found for the requested version.
- Fix `url` in config.yaml pointing to upstream fork instead of this repository.

## [0.1.6] - 2026-06-22
- Bump Bambu Studio from 02.07.01.57 to 02.07.01.62.

## [0.1.5] - 2026-06-08
- Fix dependencies for Bambu Studio 02.07.01.57.

## [0.1.4] - 2026-06-08
- Bump Bambu Studio from 02.06.00.51 to 02.07.01.57.

## [0.1.3]
- Fork from https://github.com/griffinmartin/ha-app-bambu-studio-api.

[Unreleased]: https://github.com/giorgioparri/homeassistant-addons/compare/bambu-studio-api-v0.1.12...HEAD
[0.1.12]: https://github.com/giorgioparri/homeassistant-addons/compare/bambu-studio-api-v0.1.11...bambu-studio-api-v0.1.12
[0.1.11]: https://github.com/giorgioparri/homeassistant-addons/compare/bambu-studio-api-v0.1.10...bambu-studio-api-v0.1.11
[0.1.10]: https://github.com/giorgioparri/homeassistant-addons/compare/bambu-studio-api-v0.1.9...bambu-studio-api-v0.1.10
[0.1.9]: https://github.com/giorgioparri/homeassistant-addons/compare/bambu-studio-api-v0.1.8...bambu-studio-api-v0.1.9
