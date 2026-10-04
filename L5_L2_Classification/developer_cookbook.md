# Developer Cookbook — K_NEUDIFF
**Stack:** Python 3.11, PyTorch 2.10+, diffusers 0.27+, PAX 27B (guidance), AIOSS_FORMAT
**Domain:** Neural diffusion: diffusion models for embodied AI state generation in Anticloud

## Sample robot state
```python
from k_neudiff import NeuralDiffusion

diff = NeuralDiffusion(
    checkpoint="./neudiff_checkpoint/",
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./neudiff.aioss"
)

sample = diff.sample(
    condition="robot arm in pre-grasp configuration for cylindrical object",
    n_samples=16
)
for s in sample.states:
    print(f"Joint config: {s.joint_angles}, fidelity: {s.fidelity:.2f}")
```

## Generate trajectory distribution
```python
trajectories = diff.sample_trajectories(
    start_state=current_robot_state,
    goal="move end-effector to target position",
    n_trajectories=100
)
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
