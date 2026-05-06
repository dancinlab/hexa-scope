# Nancy Grace Roman Space Telescope

> Nancy Grace Roman (1925-2018, "mother of Hubble") · planned launch 2027-05 (no later than 2027-Q4) · 2.4 m primary (ex-NRO donated) · L2 halo · wide-field IR + coronagraph technology demo · WFIRST renamed 2020.

## §1 Overview

NASA flagship next after JWST. Two main instruments: Wide Field Instrument
(WFI) — 0.281 deg² FoV (≈100× JWST NIRCam), and Coronagraph Instrument
(CGI) — technology demonstration for ~10⁻⁹ contrast at ~0.1″ (HabEx/HWO
precursor). Three core community surveys: HLWAS (High-Latitude Wide Area),
HLTDS (High-Latitude Time-Domain), GBTDS (Galactic Bulge Time-Domain).
Microlensing exoplanet census target ~1400 cold/free-floating planets.

## §2 Mirror geometry

Single monolithic 2.4 m primary (same diameter as Hubble; mirror was a
spare donated by NRO in 2012). Three-mirror anastigmat off-axis design
(unlike Hubble's on-axis Ritchey-Chrétien) → wide unvignetted FoV. Single
monolithic primary — **not** segmented; the n=6 hex tiling does **not**
appear at the primary level.

## §3 Spectral band

- WFI: 0.48 - 2.30 µm (R, Z, Y, J, H, F184 + grism + prism)
- CGI: 575/660/730/825 nm (4 narrow bands for tech demo)

Pixel scale 0.11″/pix; FoV 0.281 deg² (18 SCAs × 4096²).

## §4 n=6 closed-form candidates

| symbol  | mapping                                          | grounding             |
|---------|--------------------------------------------------|-----------------------|
| σ(6)=12 | 12 WFI filter+grism+prism elements (8+1+1+2 cal) | candidate (~12 elem)  |
| τ(6)=4  | 4 CGI narrow bands (575/660/730/825 nm)          | **STRUCTURAL-EXACT**  |
| φ(6)=2  | 2 instruments (WFI, CGI)                         | exact (binary instr)  |
| J₂=24   | 24-yr post-launch ÷ 5-yr primary = 4.8 cycles    | weak (calendar)       |

The τ=4 CGI band partition is structurally exact. WFI element count of ~12
is the candidate σ=12 mapping but exact filter wheel inventory is nominally
8 broadband filters + grism + prism + 2 calibration positions.

## §5 F-gate structure

- **F-ROMAN-1** — Wide-area survey delivers ≥1 Gpix/exposure photometric
  catalog with ≥5σ depth at H=27 by yr-2; falsified at depth <H=26.
- **F-ROMAN-2** — Microlensing exoplanet sample N≥1000 by end of GBTDS
  (yr-5); falsified at N<300.
- **F-ROMAN-3** — CGI raw contrast ≤10⁻⁸ at 0.5″ inner working angle in
  flight; falsified at >10⁻⁷ (would push HabEx requirements to the next
  decade).
- **F-ROMAN-4** — Cosmology w-precision σw ≤0.02 from BAO + WL + SN
  joint analysis; falsified at >0.05.

Primary mission 5 yr; propellant for 10 yr possible. CGI is a tech demo
only — operational HabEx/HWO direct-imaging planet science depends on
demonstrated contrast.
