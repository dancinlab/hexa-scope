# 🛰️ hexa-scope — Space Telescope Substrate

> Hubble · JWST · LSST · Roman + post-Hubble missions (LUVOIR / Origins / HabEx) under one **n=6 invariant lattice** (σ=12 / τ=4 / φ=2 / J₂=24).
> JWST 18 hexagonal mirror segments = n=6 invariant **direct hardware instance**.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20102618.svg)](https://doi.org/10.5281/zenodo.20102618)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)
[![verbs](https://img.shields.io/badge/verbs-2_spec-blue.svg)](cli/hexa-scope.hexa)
[![missions](https://img.shields.io/badge/missions-7_concept-blueviolet.svg)](docs/missions/)
[![closure](https://img.shields.io/badge/closure-4%2F4_PASS-brightgreen.svg)](verify/run_all.hexa)
[![lattice](https://img.shields.io/badge/lattice_policy-real--limits--first-success.svg)](LATTICE_POLICY.md)
[![limits](https://img.shields.io/badge/limit_breakthrough-Wave_M-informational.svg)](LIMIT_BREAKTHROUGH.md)

## Why

망원경 substrate는 cosmology(이론)와 space-operations(운영) 사이의 **specialized bridge**:
- 거울 기하 (segment count · symmetry order · diffraction limit)
- 분광 대역 (UV / Optical / IR / mm-wave)
- mission lifecycle (commission → survey → archive)

JWST의 18-segment hexagonal primary mirror가 가장 단적인 n=6 instance — `18 = 3 · σ(6)/2`. 본 substrate는 이 하드웨어 사실을 출발점으로 7-mission post-Hubble 시대를 closed-form lattice 안에서 정리한다.

## Status

**spec-first** (작동 .hexa CLI TBD). 2-verb cp -R 시드 + 7-mission overview docs.
JWST 18-hexagonal mirror = n=6 invariant **direct hardware instance** — 본 substrate가 정당화하는 가장 강한 falsifier 후보.

## Install

```bash
# 1. Install hexa-lang (ships `hexa` + `hx` package manager)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/dancinlab/hexa-lang/main/install.sh)"

# 2. Install hexa-scope
hx install hexa-scope          # global, pulls latest from registry
```

## Run

```bash
hexa-scope observatory               # cosmic-observatory spec (md seed)
hexa-scope obs_astronomy             # observational-astronomy spec (md seed)
hexa-scope mission hubble            # HST · 1990 · 2.4 m monolith
hexa-scope mission jwst              # JWST · 2021 · 6.5 m · 18 hex segments (n=6!)
hexa-scope mission lsst              # Vera Rubin / LSST · 2025 · 8.4 m TMA
hexa-scope mission roman             # Roman · 2027 · 2.4 m wide-field IR + CGI
hexa-scope mission luvoir            # LUVOIR proposal → HWO (UV/O/IR)
hexa-scope mission origins           # Origins proposal (far-IR)
hexa-scope mission habex             # HabEx proposal → HWO (coronagraph/starshade)
hexa-scope status                    # print substrate status table
hexa-scope selftest                  # sentinel sweep
hexa-scope help                      # full --help
```

## Verify

`hexa-scope`는 spec-first 4-script closure 패턴을 따른다 (sister of hexa-matter / hexa-space / hexa-cosmos):

```bash
hexa run verify/run_all.hexa      # aggregate sweep — 4/4 scripts must PASS
```

| Script | Anchor | Source |
|---|---|---|
| `verify/spec_presence.hexa` | 2 verbs + 7 mission docs present on disk | LATTICE_POLICY §1.3 rule 1 |
| `verify/lattice_arithmetic.hexa` | σ·φ = n·τ = J₂ = 24 (aux only — never sole) | LATTICE_POLICY §1.3 rule 1 |
| `verify/real_limits_anchor.hexa` | Diffraction λ/D · Photon √N · NA ≤ n · c-bound · CMB | LIMIT_BREAKTHROUGH Wave M |
| `verify/closure_consistency.hexa` | CLI · toml · README · AGENTS scoreboard agree | LATTICE_POLICY §1.3 rule 4 |

**Honesty (raw#10 C3)**: NASA / ESA / JAXA / CNSA / NSF use *their own* published ICDs — HST 2.4 m, JWST 6.5 m / 18 hex segments, LSST 8.4 m, Roman 2.4 m, ELT 39 m, TMT 30 m, GMT 25 m. JWST's 18 = 3·σ(6)/2 is a *coincidence* (Ariane-5 fairing fold geometry, per `LIMIT_BREAKTHROUGH.md §5`), not a claim that NASA designs to n=6.

**Future missions** (LUVOIR-A 15 m / LUVOIR-B 8 m / Origins 5.9 m / HabEx 4 m) remain **CONCEPT · funding-pending** per NASA Astro2020 decadal study — they have **not** flown. Markers preserved in `docs/missions/{luvoir,origins,habex}.md` and in the audit.

## Cross-link

| Sister substrate | 역할 |
|---|---|
| 🌌 [dancinlab/hexa-cosmos](https://github.com/dancinlab/hexa-cosmos) | 이론 cosmology cousin (cosmology + particle + cosmic-observatory) |
| 🚀 [dancinlab/hexa-space](https://github.com/dancinlab/hexa-space) | 관측 운영 cousin (aerospace + astronomy 11-verb) |
| 🧲 [dancinlab/hexa-rtsc](https://github.com/dancinlab/hexa-rtsc) | cryogenic optics 의존 (JWST MIRI -266°C) |

## License

MIT — Copyright (c) 2026 dancinlab (박민우 <nerve011235@gmail.com>)

Provenance: extracted from [canon@c0f1f570](https://github.com/dancinlab/canon) on 2026-05-06.
