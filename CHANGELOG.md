# Changelog

All notable changes to **hexa-scope** are documented here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and SemVer.

## [1.0.0] — 2026-05-06

### Added

- Initial extraction from `canon@c0f1f570`.
- 2-verb cp -R seed:
  - `observatory/` ← `domains/physics/cosmic-observatory/`
  - `obs_astronomy/` ← `domains/space/observational-astronomy/`
- 7-mission overview docs (`docs/missions/`):
  - Hubble · JWST · LSST · Roman · LUVOIR · Origins · HabEx
- `cli/hexa-scope.hexa` placeholder dispatcher (sub-command: observatory / obs_astronomy / mission `<name>` / selftest).
- `tests/test_selftest.hexa` verb counter sanity.
- `examples/jwst_hexagon_n6.md` — JWST 18-segment hexagonal mirror = n=6 invariant **direct hardware instance** writeup.
- `LICENSE` (MIT), `hexa.toml`, `install.hexa`, `RELEASE_NOTES_v1.0.0.md`.

### Status

spec-first; .hexa CLI 작동 wiring TBD (cycle ~26 candidate). hexa-cosmos / hexa-space / hexa-rtsc cross-link 명시.
