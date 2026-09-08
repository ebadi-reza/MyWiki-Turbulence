---
title: Ebadi 2016 — PhD dissertation (UNH)
type: source
threads:
  - non-equilibrium-pulsatile-flow
  - wall-heat-flux-experimental
  - cfd-validation-method
  - experimental-turbulence-measurement
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Ebadi (2016) — PhD Dissertation (University of New Hampshire)

**Full citation.** A. Ebadi, PhD dissertation, Department of Mechanical Engineering, University
of New Hampshire, 2016. (237 pp.) Reza's own dissertation — the umbrella document behind several of the journal papers.

## Chapter → paper map

| Thesis chapter | Corresponds to | Ingest status |
|---|---|---|
| 1 Introduction | — | skipped |
| 2 Flow, Simulation & Facility | background/DNS/facility | skipped (facility → [[neat-wind-tunnel]]) |
| 3 Exact integral method for wall heat flux | [[2015-ebadi-ijhmt]] | covered by paper |
| 4 Integral validation technique of RANS | [[2017-pond-compfluids]] | covered by paper |
| **5 Transition to turbulence in reciprocating channel flow** | [[2016-ebadi-ictam]]/[[2019-ebadi-jfm]] | **mined for lit review (below)** |
| 6 Experimental details & validation of flow facility | [[2019-biles-jfe]] (partial) | facility → [[neat-wind-tunnel]] |
| **7 Pulsatile boundary layer flow** | **unpublished** | **mined — see [[pulsatile-flow]]** |
| 8 Conclusions | — | skipped |
| **Appendices A/B/C** | **unpublished** | **mined (below)** |

Per Reza's direction, chapters 1–4 were skipped (covered by the journal papers), and the **lit review of ch. 5**, the **unpublished experimental data of ch. 7**, and the **appendices**
were mined for content not in any paper.

## Chapter 5 — reciprocating-flow literature review (unique content)

The results (four-layer structure, internal layer, conditions I & II) match [[2016-ebadi-ictam]]/[[2019-ebadi-jfm]]; the **literature review adds**:

- **Critical `Re_s` values** (thesis): `I→II ≈ 280` (Akhavan et al. 1991a), `II→III ≈ 500`, `III→IV ≈ 750`, `IV→V ≈ 3460`. ⚠️ **Conflict:** the later [[2019-ebadi-jfm]] gives `I→II ≈ 100`. Flagged on [[stokes-reynolds-number]]; not reconciled here. [source]
- **Theoretical transition-mechanism approaches:** *quasi-steady* linear stability (Von Kerczek &
  Davis 1974) predicts `Re_s,III→IV = 86` (far too low); *time-dependent* Floquet analysis
  (Blennerhassett & Bassom 2006) predicts `1416` (far too high). Conclusion: transition needs
  **both** retained time-dependency **and** order-one (large) velocity fluctuations — an analysis
  doing both has not been done. Studer et al. (2006) use a wavelet approach (two mechanisms: instability-driven vs laminar–turbulent interface). [source]
- **Unsteady length scale** `δ_t = u_τ/ω` (Akhavan et al. 1991a) — a *third* length scale for
  reciprocating flow, giving four log-law scenarios; see [[log-law]]. Current DNS = Case 2
  (modified log law, intercept `B₁(u_τ/hω)`). [source]
- Peak Reynolds stress at `y⁺ ≈ 1.9√h⁺` (steady channel; Afzal 1982; Wei et al. 2005a). [source]
- Momentum redistribution explained via **quadrant analysis** (Q1 outward interactions, Q2
  ejections, Q3 inward interactions, Q4 sweeps); regions of `u'v'>0` (Q1/Q3) redistribute between the **interior momentum sink** and the **centerline momentum source**. See [[turbulent-inertia]]. [source]

## Chapter 7 — pulsatile boundary layer flow (UNPUBLISHED)

The full experimental treatment lives on [[pulsatile-flow]]. Highlights: PIV in the [[neat-wind-tunnel|NEAT tunnel]] at three intermediate-regime frequencies (`ω⁺ = 0.007, 0.014, 0.020`); the highest frequency is **non-equilibrium** (perturbation wall shear stress leads the freestream by 40±10°, ≈Stokes 45°), the two lower are in **equilibrium**; time-averaged mean flow ≈ ZPGBL (weak mean–oscillatory coupling); reciprocating-vs-pulsatile synthesis (`Re_c=f(W)`; reciprocating linear `Re_c=700W`, `Re_s≃500`).

## Appendices (unpublished)

- **Appendix A — feedback controllers, thermocouple amplifier, enclosure box.** User-manual detail for the [[neat-wind-tunnel|thermal wall plate]] control hardware: per-plate SCR + NPN-transistor
  feedback circuit (isolates low-current DAQ from high-current heaters; SCR conducts half the AC cycle → ~60 V DC effective; 10 A SCR limit, 7.5 A max per plate), 6 PCB controller boards (12 active + 6 spare circuits), Analog Devices **AD594** thermocouple amplifiers (10 mV/°C), and a Hammond enclosure box with 5 cooling fans. See [[neat-wind-tunnel]]. [source]
- **Appendix B — modulation frequency of wall shear stress and heat flux.** Toy model: near the centerline, wall **shear stress modulates at the forcing frequency `ω`**, but wall **heat flux /
  Nu modulates at `2ω`**. Filed as [[wall-flux-modulation-frequency]]. [source]
- **Appendix C — experimental procedure.** Step-by-step PIV protocol (DaVis 8.3.1/8.0.6; dual
  HighSpeedStar cameras; calibration; laser at 14 A; AOI 448×1024 px at 7.2 kHz; tunnel oil cleanup). Distilled into [[piv]]. [source]

## Notation mapping (thesis vs canon)

| Thesis | Meaning | Canon ([[notation]]) |
|---|---|---|
| `δ_t = u_τ/ω` | unsteady length scale | `δ_t` (new) |
| `ω⁺ = ω/(u_τ²/ν)` | inner-normalized frequency | `ω⁺`; `= Str²/2` |
| `Str = ω/(u_τ/l_s)` | Strouhal number (on `l_s`, `u_τ`) | `Str` |
| `Ã(y,t)` | perturbation (oscillatory/coherent) component | triple decomposition |
| `W = δ√(ω/ν)` | Womersley (here on BL thickness `δ`) | canon `Wo` (channel uses `h`) |
| `l_s⁺` | inner-normalized Stokes-layer thickness | `l_s⁺` |

## Connections

- Threads: [[non-equilibrium-pulsatile-flow]] (ch. 5, 7), [[experimental-turbulence-measurement]]
  (ch. 6/7, appendices), [[wall-heat-flux-experimental]], [[cfd-validation-method]], [[high-Re-analytical-modeling]].
- New pages from mining: [[pulsatile-flow]], [[wall-flux-modulation-frequency]].
- Concepts touched: [[stokes-reynolds-number]], [[log-law]], [[turbulent-inertia]], [[four-layer-structure]], [[womersley-number]].
