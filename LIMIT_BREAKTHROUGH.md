<!-- @created: 2026-05-12 -->
<!-- @wave: M (limit-breakthrough audit) -->
<!-- @scope: telescope / observatory observational limits -->
<!-- @policy: LATTICE_POLICY.md §1.2 — n=6 격자 anchors NOT used here -->
---
type: limit-breakthrough-audit
wave: M
session: 2026-05-12
domain: space-telescope-and-observation-substrate
verbs: observatory + obs_astronomy + post-Hubble missions (LUVOIR/Origins/HabEx)
policy_ref: LATTICE_POLICY.md §1.2
---

# LIMIT_BREAKTHROUGH.md — hexa-scope real-limits audit

> **Frame**: telescope substrate is bounded by classical optics
> (diffraction), photon statistics (Poisson noise), detector physics
> (read noise, dark current), and survey-area scaling. Diffraction is a
> HARD wall in classical imaging but exploitable via fluorescence
> super-resolution in microscopy contexts and via interferometry for
> astronomy.

---

## §1 Domain

hexa-scope wraps space-telescope mission substrate: Hubble (2.4 m, UVOIR),
JWST (6.5 m effective, 18 hex segments, IR), LSST/Rubin (8.4 m, optical
survey), Roman (2.4 m, wide-field IR), and post-Hubble proposals
(LUVOIR-A 15 m, Origins 5.9 m far-IR, HabEx 4 m + starshade). Microscopy
verbs (if present) inherit the same diffraction wall in inverse direction.

---

## §2 Real limits

### §2.1 Diffraction (HARD — classical optics)

Rayleigh / Abbe diffraction limit: angular resolution θ ≈ 1.22 λ / D
(circular aperture), or spatial resolution d ≈ λ / (2·NA) in microscopy.

| Telescope | λ (typical) | D | θ_diff |
|---|---|---|---|
| Hubble | 500 nm | 2.4 m | ~0.05 arcsec |
| JWST | 2 µm | 6.5 m | ~0.07 arcsec |
| LUVOIR-A (proposed) | 500 nm | 15 m | ~0.008 arcsec |
| Microscope (oil immersion) | 500 nm | NA 1.4 | d ≈ 180 nm |

**HARD** in classical regime. Exploitable in two ways:

1. **Interferometry** (astronomy) — effective aperture = baseline B; θ ≈ λ/B. Event Horizon Telescope: B ≈ Earth-diameter, λ = 1.3 mm → θ ≈ 25 µas. Not classical diffraction breaking; it's *aperture synthesis*.
2. **Super-resolution fluorescence** (microscopy) — STED / STORM / PALM / SIM. These do **NOT break the diffraction limit of imaging**; they exploit time-domain switching of fluorophores so that single emitters are localized below the PSF. Honest framing: it's structured-illumination + temporal sparsity, not optical breakthrough.

### §2.2 Photon noise (HARD — quantum statistical)

Poisson SNR = √N for N detected photons. Sets:
- minimum integration time: t ∝ 1/A·τ·η for target SNR (A aperture area, τ throughput, η QE)
- limiting magnitude scales as m_lim ∝ 1.25·log₁₀(A·t) — doubling aperture buys ~0.75 magnitude per unit time.

### §2.3 Detector physics (HARD-ish — engineering)

| Limit | Typical value | Notes |
|---|---|---|
| Read noise (CCD/CMOS) | ~1–5 e⁻ RMS (sCMOS); ~0.1 e⁻ EMCCD | Engineering improvable; near-zero with photon counting |
| Dark current | ~0.001 e⁻/pix/s at -100°C; ~10 e⁻/pix/s room temp | Cooling-dominated |
| Quantum efficiency | ~95% peak Si CCD; ~80% HgCdTe NIR; ~50% MKID single-photon | Material-bounded |
| Full-well capacity | ~10⁵ e⁻/pix (CCD); ~10⁴ (CMOS) | Sets dynamic range |
| Pixel pitch | ~5–15 µm (current Si); diffraction at telescope must sample 2× per Nyquist | Detector-aperture coupling |

### §2.4 Numerical aperture ceiling (HARD — geometric)

For lens in medium of refractive index n: NA = n·sin(θ) ≤ n. Vacuum n=1 → NA ≤ 1; oil immersion n≈1.515 → NA ≤ ~1.5 (Leica HC PL APO 100x NA 1.4 commercial). Solid-immersion n>2 possible but mechanically restrictive. **HARD geometric wall.**

### §2.5 Survey area / time scaling (SOFT — engineering)

Etendue A·Ω (aperture × field-of-view) sets survey throughput. LSST/Rubin: 8.4 m × 9.6 deg² FoV → highest étendue among current ground systems. Survey time scales as N·t_per_pointing / (FoV·overlap).

### §2.6 Cosmic limits (HARD — physics)

| Limit | Value | Notes |
|---|---|---|
| Cosmic microwave background last-scattering | z ≈ 1100, t ≈ 380 kyr after Big Bang | No EM observation pre-CMB; gravitational waves only |
| Hubble horizon, current particle horizon | ~46.5 Gly comoving | Sets observable-universe size |
| Anthropic bound on observer location | Carter 1974, Bostrom 2002 | Statistical, not deterministic |
| c-bound on round-trip observation | 1 ly/yr | Interstellar probes have multi-decade light-travel |

### §2.7 Atmospheric / location limits

| Limit | Value | Notes |
|---|---|---|
| Atmospheric seeing (best ground sites) | ~0.4–0.6 arcsec | AO + lucky imaging reduces; ELTs reach near-diffraction |
| Atmospheric absorption bands | H₂O / CO₂ / O₃ blocks far-IR + much UV | Drives space deployment |
| Sky background | ~22 mag/arcsec² (dark site V-band); ~higher in IR (thermal) | Limits faint-source SNR |

---

## §3 Assessment

| Wall | Can break? | How |
|---|---|---|
| Diffraction λ/2NA (single classical aperture) | NO (HARD) | Interferometry synthesizes aperture; super-res switches in time domain — neither breaks the limit *of a single static aperture* |
| Photon Poisson noise | NO (HARD) | Quantum statistical floor; only mitigation is more aperture × time × QE |
| Detector read noise | PARTIAL (engineering) | EMCCD / SPAD / MKID approach single-photon counting |
| Atmospheric seeing | PARTIAL (engineering) | AO, interferometry, or space deployment |
| Cosmic horizon / CMB-pre opacity | NO (HARD physics) | GW + ν observations only beyond CMB |
| c-bound on interstellar imaging | NO (HARD physics) | Multi-decade latency per round-trip |

---

## §4 Top-3 highest-impact unmovable walls

1. **Diffraction θ ≈ 1.22λ/D for any single classical aperture** (HARD).
   The reason JWST has a 6.5 m mirror and LUVOIR-A proposes 15 m: there
   is no cheaper way to push θ down at fixed λ. Super-resolution
   techniques are domain-restricted (fluorescence microscopy) and do
   not apply to broadband astronomical imaging.
2. **Photon-noise SNR = √N** (HARD). Doubling aperture quadruples
   collecting area but only doubles SNR — drives the unfavorable cost
   scaling of large telescopes (D⁴ rule for ground, D²·⁷ for space).
3. **c-bound + cosmic-event-horizon** (HARD physics). No telescope
   sees pre-CMB EM directly; no telescope sees beyond the current
   particle horizon ever (universe expansion takes regions out of
   causal contact).

---

## §5 Caveats

- **Super-resolution ≠ diffraction breaking.** STED / STORM / PALM
  exploit time-domain fluorophore switching; they are *single-emitter
  localization*, not broadband sub-λ imaging. Astronomy cannot use
  these techniques (no labeled fluorophores in the universe).
- **Interferometry is aperture synthesis, not diffraction breaking.**
  Effective D = baseline; the formula still holds.
- **NA ≤ n is geometric**, not optical-quality. Achievable NA is
  further bounded by aberration correction.
- **No n=6 lattice anchors used** (per LATTICE_POLICY §1.2). JWST's
  18-segment hexagonal mirror happens to equal 3·σ(6) but the choice
  was made for fold/stow geometry inside Ariane 5 fairing, not for
  any number-theoretic reason. Treat as coincidence.
- **Cost scaling makes the wall economic in practice.** ELTs (GMT,
  TMT, E-ELT) plateau near 30–40 m on ground for cost / engineering;
  space mirrors plateau near 15 m proposed for similar reasons.

---

## §6 References

- Born & Wolf, *Principles of Optics*, 7th ed., §8 (diffraction).
- Hell, S.W. & Wichmann, J. (1994). *Breaking the diffraction resolution limit by stimulated emission.* Optics Letters — STED original.
- Betzig, E. et al. (2006). *Imaging intracellular fluorescent proteins at nanometer resolution.* Science — PALM.
- Rust, M.J., Bates, M., Zhuang, X. (2006). *Sub-diffraction-limit imaging by STORM.* Nature Methods.
- Event Horizon Telescope Collaboration (2019). *First M87 black-hole image.* ApJL.
- Gardner, J.P. et al. (2006). *The James Webb Space Telescope.* Space Sci. Rev.
- Ivezić, Ž. et al. (2019). *LSST: from science drivers to reference design.* ApJ.
- LUVOIR Final Report (2019), NASA.
- Carter, B. (1974). *Large number coincidences and the anthropic principle.*

---

*End of LIMIT_BREAKTHROUGH.md (hexa-scope, Wave M).*
