# Model Size & GPU Memory Limits

Local LLMs must fit into your GPU’s available VRAM to run correctly.

---

## Why Model Loading Can Fail

If a model requires more VRAM than your GPU provides, it cannot be loaded safely.

This may result in:
- Load failures
- Crashes
- Severe performance degradation

---

## Common Examples

- 7B models → ~6–8 GB VRAM
- 13B models → ~12–16 GB VRAM
- Larger models require significantly more memory

Actual usage depends on:
- Quantization
- Context size
- Runtime configuration

---

## What YLCA Agent Does

Before loading a model, YLCA Agent:
- Checks available GPU memory
- Estimates model memory requirements
- Prevents unsafe model loading when possible

---

## Recommended Actions

If a model does not fit:
- Select a smaller or more compressed model
- Switch to CPU execution
- Reduce context length if supported
