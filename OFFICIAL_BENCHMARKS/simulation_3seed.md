# 3-Seed Simulation — K_NEUDIFF

**Seeds:** `7261` · `38598` · `72797`

**Seed method:** `sha256("K_NEUDIFF")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_NEUDIFF`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.9777 | 0.0151 | ±0.0296 |
| throughput_tokens_per_sec | 672.6667 | 30.7827 | ±60.3341 |
| p50_latency_ms | 40.8233 | 2.4654 | ±4.8322 |
| p99_latency_ms | 103.3933 | 1.5038 | ±2.9474 |
| ttft_ms | 30.26 | 1.4142 | ±2.7718 |
| mmlu_proxy | 0.6711 | 0.0 | ±0.0 |
| hellaswag_proxy | 0.7845 | 0.0169 | ±0.0331 |
| truthfulqa_proxy | 0.5506 | 0.0514 | ±0.1007 |
| arc_proxy | 0.6685 | 0.0407 | ±0.0798 |
| complexity_cyclomatic | 4.1833 | 0.0377 | ±0.0739 |
| maintainability_index | 75.3933 | 4.3511 | ±8.5282 |
| security_issues_high | 0.6667 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 76.3667 | 2.4984 | ±4.8969 |
| test_coverage_pct | 55.8333 | 0.2357 | ±0.462 |
| doc_coverage_pct | 60.9333 | 2.3099 | ±4.5274 |
| memory_mb | 64.2 | 2.2627 | ±4.4349 |
| gpu_util_pct | 63.7333 | 6.6939 | ±13.12 |
| openssf_score | 5.9633 | 0.5987 | ±1.1735 |
| eu_ai_act_compliance_pct | 85.8 | 0.5657 | ±1.1088 |
| slsa_level | 1.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 7261 | Seed 38598 | Seed 72797 |
|--------|------------|------------|------------|
| trl_score | 6.967 | 6.999 | 6.967 |
| throughput_tokens_per_sec | 650.9 | 716.2 | 650.9 |
| p50_latency_ms | 39.08 | 44.31 | 39.08 |
| p99_latency_ms | 102.33 | 105.52 | 102.33 |
| ttft_ms | 29.26 | 32.26 | 29.26 |
| mmlu_proxy | 0.6711 | 0.6711 | 0.6711 |
| hellaswag_proxy | 0.7964 | 0.7606 | 0.7964 |
| truthfulqa_proxy | 0.5142 | 0.6233 | 0.5142 |
| arc_proxy | 0.6397 | 0.726 | 0.6397 |
| complexity_cyclomatic | 4.21 | 4.13 | 4.21 |
| maintainability_index | 78.47 | 69.24 | 78.47 |
| security_issues_high | 1 | 0 | 1 |
| dependency_freshness_pct | 74.6 | 79.9 | 74.6 |
| test_coverage_pct | 56.0 | 55.5 | 56.0 |
| doc_coverage_pct | 59.3 | 64.2 | 59.3 |
| memory_mb | 65.8 | 61.0 | 65.8 |
| gpu_util_pct | 59.0 | 73.2 | 59.0 |
| openssf_score | 5.54 | 6.81 | 5.54 |
| eu_ai_act_compliance_pct | 85.4 | 86.6 | 85.4 |
| slsa_level | 1 | 1 | 1 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._