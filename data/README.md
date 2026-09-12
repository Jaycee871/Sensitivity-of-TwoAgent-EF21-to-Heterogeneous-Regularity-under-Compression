# Public data package

This directory contains **derived manuscript-facing summaries**, not the complete internal research workspace.

The current public package supports the two-stage analysis of the reproduced **two-agent EF21 Empirical Law 4.3** under communication compression and heterogeneous local regularity.

## Included files

- `baseline_stability_summary.json` — equal-smoothness controlled baseline and contraction predictions.
- `interaction_and_retention_summary.json` — dense **216,027-cell** compression–heterogeneity study, normalized penalties, slow-region summaries, and contraction-margin retention boundaries.
- `robustness_summary.json` — off-grid robustness checks, boundary refinement, and fixed-stratum symbolic cross-checks.
- `full_regularity_mismatch_summary.json` — full-regularity fixed-average audit with **273,885 requested cells / 258,400 admissible cells**, the invariant `K2`, the exact `K1-K2` factorization, weighted-variance identity, aligned-path checks, and mismatch penalties.
- `symbolic_root_certificate.json` — generic Wolfram Language certificate for the reproduced cubic root structure and the positive largest-root sensitivity to `K1`.

## Structural result represented by the data

For the full-regularity fixed-average parameterization,

`K1 - K2 = Var_w(q_i)`, with `q_i = (L_i - mu_i)/(L_i + mu_i)`.

The closed form contains `(tau_L - tau_mu)^2`, so the proportional path `tau_L = tau_mu` is an exact zero-mismatch path. Along that path, the reproduced cubic coincides with the homogeneous controlled cubic at the same average conditioning and compression. Away from it, the mismatch is positive; together with the symbolic result `d rho_star / d K1 > 0`, this yields a strictly worse reproduced largest-root prediction for every admissible nonzero mismatch.

## Guardrail

These files contain derived numerical and algebraic results used to support the manuscript. Internal notes, exploratory artifacts, model/tool interaction records, novelty-review materials, OSF workflow files, and private research logs are intentionally excluded.

All contraction claims remain conditional on the reproduced two-agent Empirical Law 4.3. The public package does not claim a new general EF21 convergence theorem or an extension of the full cubic analysis to arbitrary numbers of agents.
