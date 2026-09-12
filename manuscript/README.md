# Manuscript package

## Working title

**Sensitivity of Two-Agent EF21 to Heterogeneous Regularity under Compression**

Authors: Pack Kwan Low and Fu-Hsing Wang.

Current manuscript snapshot: **12 September 2026**.

## Terminology

The source paper by Berg Thomsen, Taylor, and Dieuleveut labels the heterogeneous two-agent relation as **Empirical Law 4.3**. In this manuscript, the corresponding heterogeneous convergence characterization is referred to as the **Heterogeneity-Aware Convergence Law (HAC Law)**. HAC Law is a manuscript-defined name and shorthand; it is not presented as the source paper's formal title for the relation.

## Scope represented by the current manuscript

The manuscript independently reproduces the source cubic characterization over **10,500 parameter configurations** and analyzes the resulting contraction prediction under controlled communication compression and heterogeneous local regularity.

The current version contains:

- source PEP/Lyapunov validation context, including the PEPit fallback check and the `0.99 * rho_star` local tightness challenge;
- an independent 10,500-configuration reproduction and numerical audit;
- an equal-smoothness fixed-average baseline over 216,027 configurations;
- contraction-margin normalization and 99% retention boundaries;
- deterministic off-grid and boundary-refinement checks;
- a full-regularity fixed-average extension with 273,885 requested and 258,400 admissible configurations;
- the weighted-moment identity `K1-K2 = Var_w(q_i)`;
- an exact mismatch factorization through `(tau_L-tau_mu)^2`;
- proportional-alignment invariance on `tau_L = tau_mu`;
- a generic symbolic root certificate showing three distinct roots in `(0,1)` and `rho_star > sqrt(epsilon)`; and
- positive largest-root sensitivity `d rho_star / d K1 > 0` on the stated cubic-coordinate domain.

The central interpretation is that the reproduced cubic distinguishes **heterogeneity magnitude** from **regularity mismatch**: proportional heterogeneity can be invisible to the reproduced relation, whereas misalignment between smoothness and strong-convexity heterogeneity worsens the predicted contraction factor.

## Claim boundary

The source relation remains an empirical law rather than a theorem proved here. The numerical reproduction supports consistency on the audited domain but does not establish a universal approximation-error bound. The fixed-average factorization and cubic root-sensitivity analysis are restricted to the two-agent setting. Large stochastic machine-learning experiments and arbitrary-`n` extensions are outside the present manuscript scope.

Only submission-facing files should be placed in this directory. Internal research notes, workflow logs, review/novelty audits, OSF materials, and private laboratory records should remain outside this public repository.
