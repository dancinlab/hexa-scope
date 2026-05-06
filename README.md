# 🛰️ hexa-scope — Space Telescope Substrate

> Hubble · JWST · LSST · Roman + post-Hubble missions (LUVOIR / Origins / HabEx) under one **n=6 invariant lattice** (σ=12 / τ=4 / φ=2 / J₂=24).
> JWST 18 hexagonal mirror segments = n=6 invariant **direct hardware instance**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)

## § Why

망원경 substrate는 cosmology(이론)와 space-operations(운영) 사이의 **specialized bridge**:
- 거울 기하 (segment count · symmetry order · diffraction limit)
- 분광 대역 (UV / Optical / IR / mm-wave)
- mission lifecycle (commission → survey → archive)

JWST의 18-segment hexagonal primary mirror가 가장 단적인 n=6 instance — `18 = 3 · σ(6)/2`. 본 substrate는 이 하드웨어 사실을 출발점으로 7-mission post-Hubble 시대를 closed-form lattice 안에서 정리한다.

## § Verbs

### Core (2-verb, n6-arch 시드 cp -R)

| Verb | 출처 (n6-arch@c0f1f570) | 역할 |
|---|---|---|
| `observatory/` | `domains/physics/cosmic-observatory/` | 망원경 hardware substrate (이론 측) |
| `obs_astronomy/` | `domains/space/observational-astronomy/` | 관측 운영 substrate |

### Missions (7-mission overview)

| Mission | Doc | Era |
|---|---|---|
| Hubble | [docs/missions/hubble.md](docs/missions/hubble.md) | 1990 launch · 2.4m mirror |
| JWST | [docs/missions/jwst.md](docs/missions/jwst.md) | 2021 launch · 6.5m · **18-hexagon** |
| LSST (Vera Rubin) | [docs/missions/lsst.md](docs/missions/lsst.md) | 2025 first light · 8.4m · 10-yr survey |
| Roman | [docs/missions/roman.md](docs/missions/roman.md) | 2027 launch · 2.4m wide-field |
| LUVOIR | [docs/missions/luvoir.md](docs/missions/luvoir.md) | proposal · UV/Optical/IR |
| Origins | [docs/missions/origins.md](docs/missions/origins.md) | proposal · far-IR |
| HabEx | [docs/missions/habex.md](docs/missions/habex.md) | proposal · coronagraph |

## § Status

**spec-first** (작동 .hexa CLI TBD). 2-verb cp -R 시드 + 7-mission overview docs.
JWST 18-hexagonal mirror = n=6 invariant **direct hardware instance** — 본 substrate가 정당화하는 가장 강한 falsifier 후보.

## § Install

```bash
hx install need-singularity/hexa-scope
hexa-scope --self-test
```

## § Cross-link

| Sister substrate | 역할 |
|---|---|
| 🌌 [need-singularity/hexa-cosmos](https://github.com/need-singularity/hexa-cosmos) | 이론 cosmology cousin (cosmology + particle + cosmic-observatory) |
| 🚀 [need-singularity/hexa-space](https://github.com/need-singularity/hexa-space) | 관측 운영 cousin (aerospace + astronomy 11-verb) |
| 🧲 [need-singularity/hexa-rtsc](https://github.com/need-singularity/hexa-rtsc) | cryogenic optics 의존 (JWST MIRI -266°C) |

## § License

MIT — Copyright (c) 2026 need-singularity (박민우 <nerve011235@gmail.com>)

Provenance: extracted from [n6-architecture@c0f1f570](https://github.com/need-singularity/n6-architecture) on 2026-05-06.
