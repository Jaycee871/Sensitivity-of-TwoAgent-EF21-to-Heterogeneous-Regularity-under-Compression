# Sensitivity of the Two-Agent EF21 Empirical Law to Heterogeneous Regularity under Compression

Curated public reproducibility repository for the working manuscript **“Sensitivity of the Two-Agent EF21 Empirical Law to Heterogeneous Regularity under Compression.”**

Authors: Pack Kwan Low and Fu-Hsing Wang, Department of Information Management, Chinese Culture University.

## Scientific scope

This study does **not** claim a new general convergence theorem for heterogeneous EF21. It independently reproduces the **two-agent Empirical Law 4.3** reported by Berg Thomsen, Taylor, and Dieuleveut and studies the structure and sensitivity of the resulting cubic contraction prediction under controlled communication compression and heterogeneous local regularity.

The manuscript separates two notions that can otherwise be conflated:

- **heterogeneity magnitude** — how different the workers' local regularity constants are; and
- **regularity mismatch** — whether smoothness and strong-convexity heterogeneity are proportionally aligned across the two workers.

All statements about the predicted contraction factor remain conditional on the reproduced Empirical Law 4.3.

## Current manuscript snapshot — 12 September 2026

### 1. Equal-smoothness controlled baseline

The baseline fixes two workers with equal local smoothness while varying local strong-convexity imbalance at fixed average conditioning.

- 381 heterogeneity-ratio values × 189 compression levels × 3 conditioning strata.
- **216,027 controlled configurations** in total.
- Stronger local strong-convexity imbalance reduces the available contraction margin.
- Heavier compression increases the relative heterogeneity burden.
- The study reports normalized contraction-margin penalties, 99% retention boundaries, off-grid stress tests, and boundary-refinement checks.

At compression error `epsilon = 0.95`, continuous bisection gives a 99% retention boundary of approximately `tau = 0.4076217487` for `kappa_bar = 2` and `tau = 0.1798561595` for `kappa_bar = 10`; the full audited range `tau >= 0.05` satisfies the criterion for `kappa_bar = 100`.

### 2. Full-regularity fixed-average analysis

The equal-smoothness restriction is then removed. Both arithmetic means are held fixed while smoothness and strong-convexity heterogeneity vary independently through `tau_L` and `tau_mu`.

- **273,885 requested cells**, of which **258,400 are admissible** under the local regularity condition `mu_i <= L_i`.
- The reproduced empirical step size remains fixed at fixed average regularity and compression.
- `K2` is invariant and equals `((kappa_bar - 1)/(kappa_bar + 1))^2`.
- The remaining regularity dependence is carried by the nonnegative gap `K1 - K2`.
- Exactly,

  `K1 - K2 = Var_w(q_i)`, where `q_i = (L_i - mu_i)/(L_i + mu_i)`.

Under the fixed-average parameterization, this gap factors through `(tau_L - tau_mu)^2`. Therefore the proportional path `tau_L = tau_mu` is an exact zero-mismatch valley: the workers may remain heterogeneous in raw `L_i` and `mu_i`, but the reproduced cubic is unchanged from the homogeneous controlled cubic at the same average conditioning and compression.

### 3. Generic cubic root and sensitivity certificate

A separate Wolfram Language symbolic audit establishes, on the stated cubic-coordinate domain:

- three distinct real roots, all in `(0, 1)`;
- the selected largest root satisfies `rho_star > sqrt(epsilon)`; and
- at fixed `K2`, `d rho_star / d K1 > 0`.

Combined with the fixed-average mismatch factorization, this means every admissible nonzero regularity mismatch strictly worsens the reproduced largest-root contraction prediction relative to the aligned path.

## Repository layout

- `data/` — curated manuscript-facing numerical summaries and symbolic-certificate summaries.
- `src/ef21_stability/` — minimal numerical implementation of the reproduced two-agent Empirical Law 4.3 and controlled regularity analyses.
- `scripts/reproduce_key_results.py` — compact reproduction script for the public results.
- `requirements.txt` — Python dependencies.
- `manuscript/` — submission-facing manuscript notes/package area.

The private research workspace is intentionally not mirrored here. Internal research logs, exploratory notes, novelty-audit materials, OSF workflow files, model/tool interaction records, and unpublished working artifacts are excluded.

## Reproducibility

Install dependencies with:

```bash
python -m pip install -r requirements.txt
```

Then run:

```bash
python scripts/reproduce_key_results.py
```

The public JSON summaries include the equal-smoothness landscape, compression–heterogeneity interaction, contraction-margin retention boundaries, full-regularity mismatch geometry, and the generic symbolic root/sensitivity certificate.

## Interpretation guardrail

The key result is deliberately narrow: **the reproduced two-agent EF21 Empirical Law is sensitive to regularity mismatch, not merely to the magnitude of local heterogeneity.** The source empirical law itself is not promoted to a theorem, and the full fixed-average factorization and cubic sensitivity result are not claimed for arbitrary numbers of agents.

Archival citation/DOI information will be added when the public release is frozen.
