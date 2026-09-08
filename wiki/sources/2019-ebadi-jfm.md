---
title: Ebadi, White, Pond & Dubief (2019) — Mean dynamics and transition to turbulence in oscillatory channel flow
type: source
threads:
  - non-equilibrium-pulsatile-flow
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Ebadi, White, Pond & Dubief (2019) — Mean dynamics & transition in oscillatory channel flow

**Full citation.** A. Ebadi, C.M. White, I. Pond, Y. Dubief, "Mean dynamics and transition to turbulence in oscillatory channel flow," *J. Fluid Mech.* **880** (2019) 864–889. doi:10.1017/jfm.2019.706. (Reza = first author; White UNH, Dubief UVM.) The mature, full-length treatment of the DNS work seeded by [[2016-ebadi-ictam]].

## One-paragraph summary

DNS study giving a **phase-resolved, mechanistic description of transition to turbulence
in oscillatory channel flow (OCF)** — purely oscillatory / reciprocating flow with cycle-averaged **zero** mean (distinct from [[pulsatile-flow|pulsatile]], which oscillates about a non-zero mean). Three [[stokes-reynolds-number|Stokes Reynolds numbers]] are analyzed — Re_s = 648 (type III), 801 and 1009 (type IV) — spanning the III→IV boundary. The key finding: **transition to turbulence occurs when the nonlinear development stage (near-wall streak breakdown) begins during the *accelerating* portion of the cycle**. This triggers explosive growth of the near-wall Reynolds stress, the diminishing importance of a **[[turbulent-inertia|centreline momentum source]]**, the emergence of a locally accelerating/decelerating **[[internal-shear-layer|internal layer]]** at the edge of the Stokes layer (`y/l_s≈1`), and a wall-normal rearrangement of the mean forces that **culminates in the [[four-layer-structure|four-layer structure]]** of the mean momentum balance — the signature of steady wall turbulence, and here proposed as an excellent metric for whether a flow has transitioned.

## Setup

- Cartesian domain, **canonical convention** (x streamwise, **y wall-normal**, z spanwise);
  cosinusoidal pressure-gradient forcing, net-zero flow rate per period. [source]
- Three DNS: **Re_s=648** (T=30, Wo=20.5), **801** (T=30, Wo=25.1), **1009** (T=40, Wo=17.7).
  Finite-difference code (Dubief et al. 2005), up to 384³; phase-averaged over 10 periods,
  32 phases/period (48 for Re_s=801). Steady turbulent channel at Reτ=1000 (JHTDB) as
  reference. [source] (Uses `α` for [[womersley-number|Womersley]], per that paper's usage.)

## Mean momentum balance (inner-normalized)

$$\underbrace{\frac{d\langle P\rangle^+}{dx^+}}_{A^*}
+\underbrace{\frac{\partial^2\langle u\rangle^+}{\partial y^{+2}}}_{B^*}
+\underbrace{\frac{\partial\langle -u'v'\rangle^+}{\partial y^+}}_{C^*}
-\underbrace{\frac{\partial\langle u\rangle^+}{\partial t^+}}_{D^*}=0$$

A* pressure gradient, B* viscous force, C* [[turbulent-inertia]], D* local acceleration (unsteady term). The four-term balance (vs three for steady) is why OCF needs richer analysis than the single ratio `B*/C*`.

## Key results / numbers (cited to this paper)

- **Critical Re_s ladder** (compiled from literature): `I→II≈100`, `II→III≈500`, **`III→IV≈750`**, `IV→V≈3460`. [source]
- **Transition criterion:** the nonlinear development stage (streak breakdown) must begin
  during **acceleration** → happens for Re_s=801, 1009; at Re_s=648 it begins during deceleration (too late) so the flow stays weakly transitional. [source]
- **Transient log law** at the two higher Re_s during early deceleration (`⟨u⟩⁺=(1/κ)ln y⁺+B`): at Re_s=1009, `1/κ→≈2.5` (κ≈0.4) for `π/2≲φ≲11π/16`; **B always < 5.2** and depends on (Re_s,φ). Steady reference: κ≈0.4, B≈5.2. Slope from the indicator function `y⁺ d⟨u⟩⁺/dy⁺`. See [[log-law]]. [source]
- **Second momentum source:** OCF has both a **wall momentum source** and a **centreline momentum source** in the turbulent-inertia profile (the latter unique to OCF, dominant in
  early acceleration). The phase where the centreline source loses leading-order importance
  ≈ the phase where the log region emerges. [source]
- **Internal layer** centred at `y/l_s≈1` (edge of Stokes layer): locally accelerating on the wallward side, decelerating on the other; seen as a "kink" in the local-acceleration profile for the two higher Re_s (absent at Re_s=648). [source]
- **Four-layer structure** (ratio `B*/C*`) emerges for Re_s=801, 1009 at exactly the phases with steady-like turbulence; never for Re_s=648. [source]
- **Anisotropy invariant map** (Lumley–Newman): near-wall turbulence → one-component during acceleration (streaks), shifts back at streak breakdown. See [[anisotropy-invariant-map]]. [source]
- **Co-spectra** of the Reynolds-stress gradient `k_x⁺ ∂Φ⁺_{−u'v'}/∂y⁺` track the wall momentum source moving down/left (to smaller λ⁺, toward the wall) at the onset of the  nonlinear development stage. [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| x, **y**, z | streamwise, **wall-normal**, spanwise | matches canon ✅ |
| `α` | Womersley number | canon uses `Wo` (records α as usage) |
| `l_s`, `Re_s`, `Re_p`, `U_m` | Stokes length / Re / peak Re / amplitude | matches canon |
| A*, B*, C*, D* | MMB terms (pressure, viscous, turbulent inertia, unsteady) | descriptive |
| `y_m` | wall-normal peak location of Reynolds stress | recorded here |
| `b_ij`, IIa, IIIa | anisotropy tensor & invariants | see [[anisotropy-invariant-map]] |

## Connections

- Thread: [[non-equilibrium-pulsatile-flow]] (Reza's mature contribution).
- Concepts: [[stokes-reynolds-number]], [[four-layer-structure]], [[turbulent-inertia]],  [[internal-shear-layer]], [[log-law]].
- Methods: [[dns]], [[anisotropy-invariant-map]].
- Bridges to [[high-Re-analytical-modeling]] via the log law and the Wei et al. / Klewicki similarity-hierarchy framework.
- Key references: Wei et al. (2005); Klewicki, Fife & Wei (2009); Elsnab et al. (2011); Klewicki, Ebner & Wu (2011); Akhavan et al. (1991a,b); Ozdemir et al. (2014); Lumley & Newman (1977).
