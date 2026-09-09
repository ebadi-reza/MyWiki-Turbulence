---
title: Anisotropy invariant map
type: method
threads:
  - non-equilibrium-pulsatile-flow
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Anisotropy invariant map (AIM)

**What it is.** A way to characterize the *shape* of the turbulence — how fluctuating energy is distributed among the three velocity components — independent of its magnitude (Lumley & Newman 1977). Built from the Reynolds-stress **anisotropy tensor**

$$
b_{ij} = \frac{\langle u'_i u'_j\rangle}{q^2} - \frac{1}{3}\delta_{ij}, \qquad q^2=\langle u'_i u'_i\rangle
$$

subtracting the isotropic part leaves the departure from isotropy. Its invariants are `I_a = 0`, `II_a = b_{ij}b_{ji}`, `III_a = b_{ij}b_{jk}b_{ki}`. Plotting **II_a vs III_a** places every realizable state inside the **Lumley triangle**:

- **origin** → 3-component isotropic turbulence (spherical stress tensor);
- **two curving sides** → axisymmetric turbulence: "cigar-shaped" (one component larger, toward one-component) and "disk/planet-shaped" (one component smaller);
- **top straight line** → two-component turbulence (one component ≈ 0).

## What it tells you

The location in the triangle is a **structure fingerprint**. In wall turbulence the viscous sublayer lies on the two-component line (wall suppresses wall-normal fluctuations); moving outward, streamwise streaks push the state toward the one-component corner.

## Where it appears in Reza's threads

- [[non-equilibrium-pulsatile-flow]] ([[2019-ebadi-jfm]]): the AIM is the diagnostic for the streak cycle — near-wall turbulence moves **toward one-component** as streaks strengthen during acceleration, then **shifts back** at streak breakdown, pinning the onset of the nonlinear development stage. ([[2019-ebadi-jfm|source]])
- Expected to recur in the experimental (PIV) work.

Reference: J.L. Lumley & G.R. Newman, "The return to isotropy of homogeneous turbulence,"
*J. Fluid Mech.* 82 (1977) 161–178.
