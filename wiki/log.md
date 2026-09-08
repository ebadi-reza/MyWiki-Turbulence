---
title: Log
type: index
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Log — chronological record of ingests, queries, lints

Append-only. Prefix each entry `## [YYYY-MM-DD] ingest|query|lint | title`.
`grep "^## \[" log.md | tail -5` shows recent activity.

## [2026-09-03] ingest | Ebadi, Mehdi & White (2015), IJHMT — exact integral method for wall heat flux
- First source ingested (raw/my-work/2015_Ebadi_IJHMT.pdf). Thread 4 (wall-heat-flux-experimental); links to thread 5.
- Discussed takeaways with Reza before writing; Reza approved plan, renamed the shared concept page to [[triple-integral-identity]].
- Created: sources/2015-ebadi-ijhmt.md, concepts/{triple-integral-identity, wall-heat-flux, stanton-number}.md, methods/whittaker-smoother.md, threads/wall-heat-flux-experimental.md.
- Updated: notation.md (added Φ, φ', v'φ', α, Pe, Gr_x, St, δ_T; refined q″_w), index.md.
- No [UNVERIFIED] claims — all content is verified-to-source. Notation mapping recorded on the source page.
- Follow-up: consider ingesting Mehdi & White skin-friction papers (momentum sibling) if Reza has copies.

## [2026-09-03] ingest | Ebadi, White, Pond & Dubief (2016), ICTAM — transition in reciprocating channel flow
- Second source ingested (raw/my-work/2016_Ebadi_ICTAM.pdf). Thread 3 (non-equilibrium-pulsatile-flow). 2-page conference abstract; precursor to Pond 2017 and Ebadi JFM 2019/2020.
- Discussed takeaways with Reza first; Reza confirmed the 5-regime classification and Wei et al. four-layer structure as foundational (recur in later papers).
- Created: sources/2016-ebadi-ictam.md, threads/non-equilibrium-pulsatile-flow.md, concepts/{stokes-reynolds-number, four-layer-structure, turbulent-inertia, internal-shear-layer}.md, methods/dns.md.
- Updated: notation.md (added Re_s, l_s, U_m, φ phase angle, turbulent inertia; flagged φ vs φ' clash), index.md.
- Key facts: Re_s=648 type III, Re_s=1019 type IV; III→IV threshold Re_s>750; turbulence onset in early decelerating phases via internal shear layer. All verified-to-source.

## [2026-09-03] decision | Defer 2016 PhD thesis to gap-filler role
- Reza's call: hold off ingesting raw/my-work/2016_Ebadi_PhD_Thesis.pdf (237 pp) for now.
- Ingest the focused journal papers first (polished/citable versions), then mine the thesis for gaps.
- Thesis chapters flagged as likely NOT covered by other sources (revisit later): "Integral Validation Technique of RANS Turbulence Models" (thread 5, CFD validation, incl. Reynolds analogy) and the reciprocating-transition / pulsatile-BL / facility+PIV chapters. Confirm exact chapter mapping when we return to it.

## [2026-09-03] ingest | Pond, Ebadi, Dubief & White (2017), Computers & Fluids — integral validation technique of RANS models
- Third source ingested (raw/my-work/2017_Pond_CompFluids.pdf). Primary thread 5 (cfd-validation-method); also 3 and 4. Reza = 2nd author. Corresponds to the thesis "Integral Validation Technique" chapter (fills that gap).
- Discussed takeaways first; Reza confirmed: keep Wo canonical (record paper's α usage), single combined reynolds-analogy page (Pr_T folded in).
- Created: sources/2017-pond-compfluids.md, threads/cfd-validation-method.md, concepts/{womersley-number, reynolds-analogy}.md, methods/rans-turbulence-models.md.
- Updated: concepts/triple-integral-identity.md (added explicit τ_w momentum-side expression; confirmed CFD-validation link), notation.md (Wo w/ α-usage note, Re_p, Pr_T, ν_T, α_T; coordinate-convention & θ/λ clash notes), index.md.
- Key facts: standard technique says RANS within ~20% but integral technique shows physics missed via cancellation of errors (term II* under ~40%, term III* opposite sign/π out of phase/>100%); Reynolds analogy (constant Pr_T) breaks down in reciprocating flow (Pr_T from DNS highly variable). Cases Re_s=648 (Wo=20.47), Re_s=1019 (Wo=17.72). All verified-to-source.
- Notation clashes flagged: α=Womersley vs thermal diffusivity; z=wall-normal vs spanwise; θ=temperature vs momentum thickness. Kept canon, recorded per-source.

## [2026-09-03] ingest | Ebadi, White, Pond & Dubief (2019), JFM — mean dynamics & transition in oscillatory channel flow
- Fourth source ingested (raw/my-work/2019_Ebadi_JFM.pdf). Primary thread 3 (non-equilibrium-pulsatile-flow); bridges to thread 2. Reza = 1st author. Mature full-length version of the 2016 ICTAM abstract.
- Discussed takeaways first; Reza approved log-law as its own concept page and (after a refresher) the anisotropy-invariant-map as a standalone method page.
- Created: sources/2019-ebadi-jfm.md, concepts/log-law.md, methods/anisotropy-invariant-map.md.
- Updated: threads/non-equilibrium-pulsatile-flow.md (OCF-vs-pulsatile terminology; full 5-stage transition mechanism), concepts/{stokes-reynolds-number (full critical-Re ladder 100/500/750/3460), turbulent-inertia (source/sink + centreline vs wall momentum source), internal-shear-layer (y/l_s≈1 accel/decel refinement), four-layer-structure (A*/B*/C*/D* terms, regions i–iv, transition metric)}, notation.md (b_ij, IIa/IIIa, turbulent inertia, u'_rms), index.md.
- Key facts: transition requires nonlinear development stage (streak breakdown) to begin during acceleration (Re_s>750); transient log law κ≈0.4/B<5.2 at higher Re_s; four-layer structure emerges for Re_s=801,1009 not 648; centreline momentum source unique to OCF. Canonical coordinates (y=wall-normal) — matches canon. All verified-to-source.

## [2026-09-03] ingest | Ebadi, Cuevas Bautista, White, Chini & Klewicki (2020), JFM Rapids — UTZ/TF heat-transfer model
- Fifth source ingested (raw/my-work/2020_Ebadi_JFM.pdf). Primary thread 2 (high-Re-analytical-modeling); also thread 4. Reza = 1st author. NOT oscillatory-flow — it's the passive-scalar (heat) companion to Cuevas Bautista et al. 2019 (2019_Bautista_JFM, next).
- Discussed takeaways first; Reza agreed to (1) ingest Bautista next to complete the pair, (2) create UMZ/VF concept now as a stub (source of record = Bautista 2019).
- Created: sources/2020-ebadi-jfm.md, threads/high-Re-analytical-modeling.md (was missing), concepts/{uniform-temperature-zones, self-similar-hierarchy}.md, concepts/uniform-momentum-zones.md (STUB — expand at Bautista ingest).
- Updated: concepts/log-law.md (scalar log law + κ_θ), notation.md (κ_θ, φ_c=1.62, φ_θc, W_θ, θ_τ, Pr_t, UMZ/VF, UTZ/TF, δ⁺=Re_τ note), index.md.
- Key facts: temperature field = UTZs separated by TFs (ramp–cliff); four-layer structure of mean scalar eq (Zhou et al. 2017); Fife parameter φ_c=(1+√5)/2≈1.62; validated vs Pirozzoli DNS δ⁺=4088, Pr=0.2/0.71/1.0; kurtosis Pr-sensitive, mean/heat-flux not; streamwise Pr_t≈2. Coordinates/α match canon. All verified-to-source.

## [2026-09-03] ingest | Cuevas Bautista, Ebadi, White, Chini & Klewicki (2019), JFM — UMZ/VF model of the turbulent boundary layer
- Sixth source ingested (raw/my-work/2019_Bautista_JFM.pdf). Thread 2 (high-Re-analytical-modeling). Reza = 2nd author. Source of record for the UMZ/VF concept; momentum-side companion to 2020_Ebadi (UTZ/TF).
- Pre-approved by Reza (ingest-next + flesh-out-UMZ/VF).
- Created: sources/2019-bautista-jfm.md. Expanded concepts/uniform-momentum-zones.md from stub → full.
- Updated: concepts/self-similar-hierarchy.md (φ_c²=1/κ, L=⌊1.04lnδ⁺−2⌋, discrete y⁺/ΔU⁺ relations, W⁺ momentum), concepts/four-layer-structure.md (added momentum region-scaling Table 1; y⁺≈2.6√δ⁺ inertial onset), threads/high-Re-analytical-modeling.md, notation.md (W/f_w/Ξ/L/ω_z), index.md.
- Key facts: VF thickness f_w/δ≈1.3/√δ⁺ (~Taylor microscale), velocity jump per VF > u_τ; Fife φ_c=(1+√5)/2≈1.62, φ_c²=1/κ; L=⌊1.04lnδ⁺−2⌋ inertial layers; validated vs Lee&Moser DNS δ⁺≈5200; uniquely reproduces sub-Gaussian skewness/kurtosis; dT/dy=v'ω_z−w'ω_y (model captures v'ω_z). Coordinates match canon. All verified-to-source.
- Note: thread 2 open item — possible analysis page comparing UMZ/VF vs UTZ/TF.

## [2026-09-03] ingest | Biles, Ebadi, Allard & White (2019), JFE — thermal boundary layer wall plate & NEAT wind tunnel
- Seventh source ingested (raw/my-work/2019_Biles_JFE.pdf). Primary thread 1 (experimental-turbulence-measurement); links to 4, 3, 5. Reza = 2nd author. Apparatus + measurement paper.
- Discussed takeaways first; Reza clarified thread 6 (ramp) has NO source (unpublished, installed in UNH Flow Physics Facility tunnel) — do not map anything to it. NEAT is a separate rig. Approved thread-1 assignment and keeping κ_T vs κ_θ distinct.
- Created: sources/2019-biles-jfe.md, threads/experimental-turbulence-measurement.md (was missing), threads/wind-tunnel-ramp.md (records no-source status), methods/{piv, ir-thermography, neat-wind-tunnel}.md.
- Updated: concepts/log-law.md (thermal law of wall Θ⁺=(1/κ_T)ln y⁺+C₂(Pr), κ_T≈0.48, κ_T-vs-κ_θ warning, nonequilibrium sensitivity), concepts/stanton-number.md (Colburn analogy + step correlation), threads/{wall-heat-flux-experimental, non-equilibrium-pulsatile-flow}.md, notation.md (κ_T, C₁/C₂, Θ deficit), index.md.
- Key facts: NEAT open-circuit indraft tunnel; 12-section thermal wall plate ±0.5°C (20–65°C); rotor-stator → PULSATILE (non-zero mean) freestream; τ_w via Mehdi–White integral from PIV; temperature law-of-wall far more sensitive to nonequilibrium than velocity law-of-wall. All verified-to-source.
- IMPORTANT provenance note: thread 6 ramp = Reza's unpublished work in UNH Flow Physics Facility; no paper to ingest.

## [2026-09-03] ingest | Wengrove, Ebadi, White & Foster (2020), Exp. Fluids — momentum integral method for skin friction in separated flows
- Eighth source ingested (raw/my-work/2020_Wengrove_ExpFluids.pdf). Primary thread 1 (experimental-turbulence-measurement); links to 5 and 4. Reza = 2nd author. Momentum sibling of the 2015 heat-flux method (Ebadi IJHMT), stress-tested in separated/curved flows.
- Discussed takeaways first, then wrote (final my-work source).
- Created: sources/2020-wengrove-expfluids.md, concepts/wall-skin-friction.md (new hub, mirrors wall-heat-flux).
- Updated: concepts/triple-integral-identity.md (named MW-MIM = Mehdi–White momentum integral method; separated/curved validation, cos α slope correction, flow-reversal resolution requirement), threads/experimental-turbulence-measurement.md, notation.md (τ_w/C_f expanded, s-n coords, α wall slope, y_s), index.md.
- Key facts: MW-MIM captures C_f(x) through separation if flow-reversal region resolved (35–75% of y_s for <20% error); s-n coords beat x-y on curved walls, or use C_f=C_fxy/cosα; term III dominates, II&III cancel in separation → negative τ_w. All verified-to-source.
- MILESTONE: all 8 papers in raw/my-work/ now ingested. Only the deferred 2016 PhD thesis remains (gap-filler).

## [2026-09-03] ingest | Ebadi (2016) PhD thesis — gap-fill (Ch. 5 lit review, Ch. 7 unpublished pulsatile PIV, appendices)
- Ninth source ingested (raw/my-work/2016_Ebadi_PhD_Thesis.pdf), per Reza's direction: skip Ch.1-4 (covered by papers), mine Ch.5 (lit review), Ch.7 (unpublished experimental data), and appendices. Text extracted via pypdf (poppler unavailable for page-range render).
- Created: sources/2016-ebadi-thesis.md, concepts/pulsatile-flow.md (resolves the long-standing [[pulsatile-flow]] forward-link; the unpublished PBL experiments), analyses/wall-flux-modulation-frequency.md (Appendix B toy model: τ_w at ω, q″_w/Nu at 2ω).
- Updated: concepts/log-law.md (unsteady length scale δ_t=u_τ/ω + 4 log-law scenarios; DNS=Case 2), concepts/stokes-reynolds-number.md (FLAGGED Re_s,I→II conflict 100 vs 280 [REVIEW]; Re_c=700W reciprocating), concepts/turbulent-inertia.md (interior momentum sink + quadrant analysis), methods/piv.md (Appendix C procedure), methods/neat-wind-tunnel.md (Appendix A control hardware), threads/non-equilibrium-pulsatile-flow.md, notation.md (δ_t, ω⁺, Str, Ã, l_s⁺), index.md, overview.md.
- Key NEW facts: PBL experiments ω⁺=0.007/0.014/0.020 (intermediate regime); highest freq non-equilibrium (τ̃_w leads freestream 40°≈Stokes), two lower in equilibrium; κ=0.45/0.42/0.47 vs ZPGBL 0.41; reciprocating Re_c=700W (Res≃500); four ω⁺ frequency regimes. Appendix B: wall heat flux modulates at 2× forcing freq.
- CONFLICT flagged for Reza: Re_s,I→II ≈100 (2019 JFM) vs ≈280 (thesis). [UNVERIFIED] tag on the critical-ω⁺ conjecture (Reza's own, "more work required").
- MILESTONE: all raw/my-work/ sources ingested, thesis included. Thread 6 (ramp) still has no source.

## [2026-09-03] decision | Re_s,I→II conflict resolved — keep both
- Reza confirmed: keep both ≈100 (2019 JFM) and ≈280 (thesis). Not an error — the I→II onset (first velocity fluctuations) is very sensitive to initial/background disturbances, so scatter across studies is expected/genuine. Updated concepts/stokes-reynolds-number.md accordingly (removed [REVIEW], marked resolved).

## [2026-09-03] ingest | Romero, Zimmerman, Philip, White & Klewicki (2022), JFM 937:A30 — inertial sublayer in APG TBLs
- Tenth source ingested (raw/references/2022_Romero_JFM.pdf — copied from Reza's Downloads; NOT Reza-authored, so filed under raw/references/ not my-work/). Provided by Reza as the published source for the FPF ramp (thread 6). Text via pypdf.
- Primary: thread 6 (wind-tunnel-ramp) — the ramp was BUILT BY A. Ebadi (Reza) & J. Klewicki at UNH (paper acknowledgement). Also threads 1 (hot-wire), 2 (inertial sublayer/scaling patches), non-equilibrium (APG).
- Created: sources/2022-romero-jfm.md, methods/{hot-wire-anemometry, flow-physics-facility}.md, concepts/adverse-pressure-gradient-tbl.md. Rewrote threads/wind-tunnel-ramp.md from placeholder → real content.
- Updated: concepts/{self-similar-hierarchy (scaling patches → log OR power law), four-layer-structure (APG 4-term MMB, TI-crossing decouples), log-law (APG behavior)}, threads/{experimental-turbulence-measurement, high-Re-analytical-modeling}, notation.md (β Clauser, K, Δ Rotta–Clauser, ϵ scaling patch), index.md, overview.md.
- Ramp facts: built by Ebadi & Klewicki; installed in UNH Flow Physics Facility (2.8×6 m, 72 m fetch); ceiling-mounted (measurements on flat floor → PG without curvature); FPG(−0.4m/3.1m)→ZPG(~7m)→APG(+0.5m/5.3m)→ZPG(~20m).
- Physics facts: APG MMB = 4 terms (VF/TI/MI/PG); inertial onset y⁺≈1.5√δ⁺ (APG) vs 3√δ⁺ (ZPG); TI zero-crossing decouples from onset in APG; APG u²⁺ no log decay/not self-similar but distance-from-wall scaling holds; -uv⁺>1 (uτ scaling breaks); scaling patches → log (single scale) or power law (multiple, σ=1/3 Stratford). κ≈0.384, B≈4.4. All verified-to-source.
- MILESTONE: thread 6 now sourced. All 6 threads have real content.

## [2026-09-03] correction | Ramp builder = C.J. Klewicki (not J. Klewicki)
- Correcting the entry above: the FPF ramp was built by A. Ebadi & **C.J. Klewicki** (Joseph Klewicki's son), per Reza. This is a DIFFERENT person from the paper's author / self-similar-hierarchy framework author **Joseph C. Klewicki**. Source, thread, and FPF pages updated to disambiguate; the "J. Klewicki" in that prior line should read "C.J. Klewicki".
