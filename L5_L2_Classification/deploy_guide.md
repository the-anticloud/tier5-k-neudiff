# Deploy Guide — K_NEUDIFF
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, diffusers 0.27+, PAX 27B (guidance), AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, diffusers 0.27+, A100 GPU for training. T4 for sampling.

## Environment
A100 80GB for training diffusion models. T4 for sampling. 32GB RAM.

## AIOSS Integration
```bash
aioss init --module K_NEUDIFF --output ./k_neudiff.aioss
aioss append --chain ./k_neudiff.aioss --payload ./output.bin --module K_NEUDIFF
aioss verify --chain ./k_neudiff.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_NEUDIFF",
    aioss_chain="./K_NEUDIFF.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_NEUDIFF.aioss --verbose
python -m K_NEUDIFF.tests.smoke
```
