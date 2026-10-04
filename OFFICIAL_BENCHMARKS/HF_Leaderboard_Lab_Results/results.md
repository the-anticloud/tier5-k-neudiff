# HF_Leaderboard_Lab_Results

**Project:** `K_NEUDIFF`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `google/neural-tangents`  
**Commit:** `c17e770bb74f`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **55.53 ms** |
| Min latency | 45.98 ms |
| Max latency | 66.13 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **38** |
| Tokenization latency | 3.01 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5849 |
| Classification latency | 170.6 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_NEUDIFF (google/neural-tangents) — 95 files, 27129 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'ne', '##udi', '##ff', '(', 'google', '/', 'neural', '-', 'tangent', '##s', ')', '—', '95', 'files', ',', '271', '##29']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_