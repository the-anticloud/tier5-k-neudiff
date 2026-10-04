# L5 Narrow / L2 General Classification — K_NEUDIFF
**Platform:** Anticloud | **Tier:** TIER_5_WORLD_NEURO_EMBODIED | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_NEUDIFF applies diffusion model techniques to embodied AI: generating diverse, physically plausible robot states, trajectory distributions, and environment configurations for TIER_5 and TIER_9 training.

## L2 General
L2 General: K_NEUDIFF provides generative state diversity for any Anticloud embodied training pipeline. TIER_9 robot manipulation diversity and TIER_5 world model diversity both use K_NEUDIFF.

## PAX 27B Integration
PAX 27B provides text-conditioned guidance for K_NEUDIFF: language descriptions of desired robot behaviors guide the diffusion sampling process toward the intended distribution.

## AIOSS Audit Chain
Every diffusion sample (conditioning hash + denoising trajectory hash + final sample hash + fidelity score) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
No external regulatory. ISO/IEC 42001 (AI system capability documentation).
