# Habitable Exoplanet Observatory (HabEx, proposal)

> Astro2020 Decadal exoplanet-direct-imaging flagship concept. Merged with LUVOIR into the **Habitable Worlds Observatory (HWO)**. HabEx contributed the coronagraph + starshade direct-imaging architecture; LUVOIR contributed UV/general-astrophysics scope.

## §1 Overview

HabEx was the 2020 decadal concept study for a 4 m-class **off-axis
unobscured** monolithic optical/UV/near-IR telescope optimized for direct
imaging of habitable-zone exoplanets via simultaneous coronagraph + 52 m
external starshade. The unobscured pupil (no secondary-mirror spider arms)
delivers cleaner PSF for 10⁻¹⁰ contrast at small inner working angles.
HabEx + LUVOIR were merged by Astro2020 into HWO; HabEx's contribution is
the **coronagraph/starshade direct-imaging chain** as the ExoEarth Survey
backbone.

## §2 Mirror geometry

4 m **monolithic** unobscured off-axis primary (no segmentation). The
unobscured architecture is HabEx's distinguishing feature vs LUVOIR's
hex-segmented approach:
- pro: PSF symmetry, no diffraction spikes from spider arms
- con: monolithic 4 m fused-silica blank, fairing-limited; mass penalty

External 52 m **starshade** (formation flight, ~76,000 km separation)
delivers external occulter for exoEarth direct imaging. Hex-petal
starshade design (typically 20-32 petals; *not* n=6 directly).

## §3 Spectral band

- UV: 115-450 nm (UVS spec)
- Optical: 450-1000 nm (HCG coronagraph + camera)
- Near-IR: 0.95-1.8 µm

Contrast target: 10⁻¹⁰ at 60 mas inner working angle (with starshade);
10⁻⁹ at 100 mas (coronagraph alone).

## §4 n=6 closed-form candidates

| symbol  | mapping                                          | grounding              |
|---------|--------------------------------------------------|------------------------|
| σ(6)=12 | 12 spectral channels (UVS+HCG+NIR partition)     | candidate              |
| τ(6)=4  | 4 instruments (UVS, HCG, HWC, starshade)         | **STRUCTURAL-EXACT**   |
| φ(6)=2  | 2 contrast modes (coronagraph / starshade)       | exact (binary)         |
| J₂=24   | starshade petal count 24 (4×6 hex sub-petals)    | candidate (24 design)  |

The starshade petal count is design-flexible; some HabEx concepts used 24
petals which would map cleanly to J₂=24.

## §5 F-gate structure

- **F-HABEX-1** — Starshade formation-flight tech demoed at TRL 5+ by
  2028; falsified at TRL <4 (would force coronagraph-only architecture).
- **F-HABEX-2** — Direct-imaging contrast 10⁻¹⁰ at 60 mas validated on
  hex-segmented or unobscured testbed by 2030; falsified at >10⁻⁹.
- **F-HABEX-3** — HabEx scope absorbed into HWO design without losing
  exoEarth direct-imaging capability; falsified if HWO drops the
  starshade option entirely.
- **F-HABEX-4** — N≥25 nearby (d<10 pc) FGK habitable-zone planet
  candidates characterized in HWO ExoEarth Survey by 2050; falsified
  at N<5 (would close the rocky-planet biosignature window).

Status: **proposal**, scope merged into HWO. HabEx is no longer a
standalone mission but persists as the direct-imaging architectural
spine of HWO.
