# Vera C. Rubin Observatory / LSST

> Vera C. Rubin (1928-2016) · first light 2025-Q4 · 8.4 m primary (M1+M3 monolith) · 10-yr Legacy Survey of Space and Time · Cerro Pachón, Chile (ground-based but cross-listed for survey synergy with JWST/Roman).

## §1 Overview

NSF/DOE ground-based wide-field survey telescope. Not a space telescope —
included in this substrate because LSST is the **time-domain anchor** for
Roman, JWST follow-up, and post-Hubble UV (LUVOIR/HWO) cross-calibration.
3.2 Gpix LSSTCam (largest astronomical CCD ever built, 189 sensors,
9.6 deg² field of view per pointing). Survey strategy: ~1000 visits per
pointing over 10 yr; nightly ~20 TB raw, ~15 PB final image archive,
~500 PB processed. Alert stream ~10⁷ alerts/night via brokers
(ANTARES, Lasair, Fink, ALeRCE).

## §2 Mirror geometry

Three-mirror anastigmat (TMA) with **monolithic M1+M3** (single 8.4 m
fused-silica blank with M1 = 8.4 m outer annulus, M3 = 5.0 m inner
concave) cast by Steward Observatory Mirror Lab. M2 = 3.4 m convex.
Effective f/1.234. **Not segmented** — single huge cast monolith
(hex-aware *only* in CCD raft layout, not mirror).

## §3 Spectral band

Six broadband filters: u/g/r/i/z/y, 320-1080 nm. Single-exposure depth
~24 mag (r-band, 30 s); coadded 10-yr depth ~27 mag.

## §4 n=6 closed-form candidates

| symbol  | mapping                                          | grounding              |
|---------|--------------------------------------------------|------------------------|
| σ(6)=12 | 12 × 9 raft layout = 21 rafts (≠ 12, mismatch)   | **MISMATCH** (21 rafts)|
| τ(6)=4  | 4 main survey programs (WFD, DDF, NES, GP)       | exact                  |
| φ(6)=2  | binary deep-vs-wide survey strategy              | exact                  |
| J₂=24   | 24-hr nightly cadence × 365 × 10                 | calendar               |

**Honest caveat**: LSST's CCD raft layout is 21 (3×3 grid + corners) which
breaks the σ(6)=12 expectation. This is a real **n=6 lattice mismatch case**
worth recording. The τ(6)=4 four-program structure is the cleanest mapping.

## §5 F-gate structure

- **F-LSST-1** — Survey image-quality (PSF FWHM) ≤0.7″ median over 10 yr;
  falsified if median >1.0″ after first 2 yr.
- **F-LSST-2** — Type Ia SN Hubble-diagram dispersion ≤0.10 mag with full
  10-yr sample; falsified if >0.15 mag (would invalidate dark-energy
  equation-of-state w-precision target σw ≈ 0.02).
- **F-LSST-3** — Solar system small-body discovery rate ≥10× pre-LSST by
  yr-5; falsified at <3×.
- **F-LSST-4** — Alert latency ≤60 s for ≥99% of alerts through yr-3;
  falsified at <90% within latency.

Survey end nominal: 2035-Q4. Followup synergies with JWST (HighZ candidates),
Roman (microlensing), Euclid (weak lensing crosscheck).
