# James Webb Space Telescope (JWST)

> James E. Webb · launched 2021-12-25 (Ariane 5) · 6.5 m primary mirror · 18 hexagonal beryllium segments (n=6 hexagon direct instance) · L2 halo orbit · IR observatory.

## §1 Overview

NASA/ESA/CSA flagship infrared space telescope. Sun-Earth L2 (1.5 × 10⁶ km
from Earth) Lissajous orbit. Five-layer kapton sunshield (~22 × 12 m
deployed) keeps cold-side MIRI optics at 6.7 K (active cryocooler) and
NIRCam/NIRSpec/NIRISS at ~40 K (passive). First light commissioning 2022;
science ops since 2022-07. Already redefining high-z galaxy populations
(JADES, CEERS), exoplanet atmospheres (WASP-39b CO₂, K2-18b DMS candidate),
and primordial chemistry (METAL-poor stars in distant galaxies).

## §2 Mirror geometry — n=6 hexagonal segmented direct instance

**18 hexagonal mirror segments** arranged in a 2-ring honeycomb tile around
a central hex (1 + 6 + 12 = 19 hex slots, with center occupied by a hex
mirror and outer 6 corner positions filled = 18 active segments + 1 obscured
secondary support). Each segment: gold-coated beryllium, 1.32 m point-to-point
(flat-to-flat 1.142 m), 7-DOF actuated (6 rigid-body + 1 radius-of-curvature).
Aggregate effective collecting area ≈ 25.4 m². Folded for launch in 3 panels
(central 12 + 2 wings of 3 each).

The hexagonal geometry is **not** decorative — it is the unique
edge-shareable regular tiling that fits a circular aperture with
high fill factor (>98%) while permitting 7-DOF wavefront control without
mechanical interference between adjacent segments. **JWST's primary is the
clearest engineering instance of the n=6 hexagonal lattice** in any
operational space asset.

```
       ┌─┐ ┌─┐ ┌─┐
       └─┘ └─┘ └─┘            outer ring (6 segments)
     ┌─┐ ┌─┐ ┌─┐ ┌─┐
     └─┘ └C┘ └─┘ └─┘          inner ring (6) + center C
       ┌─┐ ┌─┐ ┌─┐
       └─┘ └─┘ └─┘
```

## §3 Spectral band

- NIRCam: 0.6 - 5.0 µm
- NIRSpec: 0.6 - 5.3 µm (multi-object MOS, IFU, fixed-slit)
- NIRISS: 0.8 - 5.0 µm (AMI, SOSS, WFSS)
- MIRI: 4.9 - 28.8 µm (imaging, MRS IFU, LRS, coronagraph) — cryocooler
  to 6.7 K

Diffraction limit at 2 µm ≈ 0.07″.

## §4 n=6 closed-form candidates — STRUCTURAL-EXACT for σ(6)=12

| symbol  | mapping                                          | grounding                |
|---------|--------------------------------------------------|--------------------------|
| σ(6)=12 | 12 vertices of inner+outer hex ring (flat geom)  | **STRUCTURAL-EXACT**     |
| τ(6)=4  | 4 instruments (NIRCam, NIRSpec, NIRISS, MIRI)    | **STRUCTURAL-EXACT**     |
| φ(6)=2  | 2 mirror temperatures (40 K passive / 6.7 K MIRI)| exact (binary cryo split)|
| J₂=24   | 18 segments + 6 secondary-mirror support struts  | candidate (1 mech basis) |

**This is the cleanest n=6 lattice instance among the 7 missions in this
substrate.** The 18 hexagonal segments × 6-fold symmetry of each hex = 108
shared edges; combined with 6 secondary struts (J₂ candidate) the entire
mechanical optical path is hex-derived.

## §5 F-gate structure

- **F-JWST-1** — Mirror segment phasing degradation: WFE rms drift
  <50 nm/yr through 2030; falsified if drift >150 nm/yr (would force
  re-phasing campaigns to dominate cycle time).
- **F-JWST-2** — z>15 galaxy luminosity function consistent with ΛCDM
  bottom-up assembly within factor 3 by cycle 5 (2026); falsified if
  required SFE > 100% at z=15 (would force non-standard stellar IMF or
  primordial BH seeding).
- **F-JWST-3** — Exoplanet biosignature DMS at K2-18b confirmed at >5σ
  by JWST cycle 6 transmission spectra; falsified if signal drops below
  1σ on independent re-observation.
- **F-JWST-4** — MIRI cryocooler operational lifetime ≥10 yr
  (2032-Q1); falsified by failure of ≥2 of 3 redundant compressor stages.

Propellant-limited mission lifetime: 20+ yr nominal (launch precision was
better than spec).
