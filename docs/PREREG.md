# Preregistration — `research-lottery-apriori`
 
**Pillar:** `research-lottery-apriori`  
**Title:** Lottery Draws Epistemic Null Baseline (ECT-2026-003)
**Date:** 2026-06-14  
**ORCID Identifier:** `0009-0004-9601-5617`

## Charter (one paragraph)

Treat draws as a controlled randomness lab; forbid exploitable next-draw claims without preregistered nulls. This study registers the baseline null causal performance of random draws, verifying that historical sequences (e.g. lag 1, lag 2 draws) and exogenous parameters (e.g. day of week, temperature, white noise) show zero causal links to next-draw sums under OCCA constraint-based searches.

## Primary question (Layer A)

- **Question:** Do historical lottery draw sums (lag1_draw_sum, lag2_draw_sum) or exogenous covariates (day_of_week, temperature, noise_1) causally influence the next draw sum?
- **Expected DAG:** Empty (no directed or undirected edges between past history/covariates and the next draw sum).
- **Primary metric:** Discovered directed edges and information coefficient.
- **Direction / threshold:** $\alpha = 0.05$ for PC algorithm. The number of discovered directed edges must equal 0. The absolute information coefficient of any nonlinear transformation must not beat the phase-shuffled Spectral MC null ($p > 0.05$).

## Null / negative controls

- **Null model:** Phase-shuffled Spectral Monte Carlo (FFT surrogate paths).
- **Caps:** Capped at $N = 25$ runs for local smokes (`runs/smoke.yaml`); $N = 1000$ for full remote promotion validation with run ID `charter_lottery_epistemic_prereg_run_01`.

## Truth scope & ethics

- **Scope:** Observational lottery draw sequences. This serves as an epistemic control baseline under the **ECT-2026** standard.
- **Data rights:** Utilizes public lottery records pinned in `datasets.yaml`.

## Promotion rules

Numbers enter `BEST_ANSWERS_OVERVIEW` (meta) only after `methodology_preamble.assert_run_card` passes in the same environment that produced the artifact. Follow the meta checklist [PROMOTION_CHECKLIST.md](https://github.com/SVG-campus/Research-Apriori/blob/main/docs/PROMOTION_CHECKLIST.md) before editing canonical summaries.
