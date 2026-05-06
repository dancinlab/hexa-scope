# hexa-scope v1.0.0 — Release Notes

**Release date**: 2026-05-06
**Provenance**: extracted from [n6-architecture@c0f1f570](https://github.com/need-singularity/n6-architecture)
**License**: MIT

## Highlights

- 🛰️ **Space telescope substrate** under n=6 invariant lattice (σ=12 / τ=4 / φ=2 / J₂=24).
- **JWST 18-segment hexagonal primary mirror** = n=6 invariant **direct hardware instance**. 가장 강한 falsifier 후보로 §F-SCOPE-1 preregister 예정.
- 7-mission overview (Hubble · JWST · LSST · Roman · LUVOIR · Origins · HabEx) — pre-Hubble~post-Hubble 50-yr 망원경 lifecycle.
- 2-verb cp -R 시드: `observatory/` (이론) + `obs_astronomy/` (운영).

## What's in

- 2 verb 시드 (cp -R 전체)
- 7 mission overview docs
- `cli/hexa-scope.hexa` placeholder dispatcher
- `tests/test_selftest.hexa`
- `examples/jwst_hexagon_n6.md`
- LICENSE / hexa.toml / install.hexa / README / CHANGELOG

## What's not (yet)

- 작동 .hexa CLI (mission browser / mirror geometry calculator / spectral band selector) — cycle ~26 candidate.
- Real telescope data ingest (MAST archive / Vizier query) — v1.2.0 target.
- JWST 18-hexagon ↔ n=6 invariant Bayesian audit (posterior fit).

## Cross-link

- [hexa-cosmos](https://github.com/need-singularity/hexa-cosmos) — 이론 cosmology cousin
- [hexa-space](https://github.com/need-singularity/hexa-space) — 운영 cousin
- [hexa-rtsc](https://github.com/need-singularity/hexa-rtsc) — cryogenic optics 의존
