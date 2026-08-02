# 🎓 Fine-Tuning

> Adapting a model to your task by further training it and adjusting weights.

## When to Fine-Tune

✅ **Do it when:**
- Prompt engineering + RAG aren't enough
- Need consistent structured output
- Working with smaller models needing task-specific boost
- Doing **model distillation** (small model imitating a large one)

❌ **Don't do it when:**
- Need a general-purpose model
- Just starting to experiment
- Simpler approaches haven't been fully explored

## RAG vs. Fine-Tuning

| Problem Type | Solution |
|--------------|----------|
| Missing information (e.g., private company data) | **RAG** |
| Wrong behavior (bad format, off-topic) | **Fine-tuning** |
| Both | Start with **RAG**, then add fine-tuning |

## Memory Bottleneck

Fine-tuning uses **more memory than inference** because of backprop.

Memory footprint depends on:
- Total parameters
- Trainable parameters
- Numerical precision (bits per value)

### Reduction Techniques

- **Gradient checkpointing** — recompute activations vs. storing them (slower but less memory)
- **Quantization** — use fewer bits per parameter (32-bit → 16-bit → 8-bit → 4-bit)
- **PEFT** — parameter-efficient fine-tuning (only train a small subset)

### Quantization Notes

- Inference is fine with 4–8 bits
- Training needs **mixed precision** (some 32-bit, some lower)
- ⚠️ Load models in their intended format (fp16 vs. bf16 can break quality)

## PEFT (Parameter-Efficient Fine-Tuning)

Two families:

### 1. Adapter-Based (Additive)
Add small new modules to the model.

- **LoRA (Low-Rank Adaptation)** — most popular
  - Decomposes weight matrices into smaller products (A × B)
  - Only trains A and B; original weights frozen
  - Can merge back into original weights → **no inference latency**
  - Best applied to Transformer attention modules

### 2. Soft Prompt-Based
Add trainable special tokens.

## Multi-Task Fine-Tuning

| Approach | Description | Trade-offs |
|----------|-------------|-----------|
| **Simultaneous** | Train on all tasks at once | Harder, needs more data |
| **Sequential** | Task A, then Task B | Risk: **catastrophic forgetting** |
| **Model merging** | Train separately, then combine | Flexible, no GPU needed for merging |

### Merging Methods
- **Summing** — add weights (most common)
- **Layer stacking** (Frankenmerging)
- **Concatenation** — least recommended

## Practical Workflow

1. Test fine-tuning code on cheapest/fastest model
2. Test data on a mid-size model
3. Run experiments on target model
4. Map price-performance frontier, pick winner

## Key Hyperparameters

| Parameter | Effect |
|-----------|--------|
| **Learning rate** | Too high = fluctuating loss; too low = slow. Start large, decay. |
| **Batch size** | Larger = faster but more memory. Small batches → use gradient accumulation. |
| **Epochs** | Small data → 4-10 epochs; Millions → 1-2 epochs |
| **Prompt loss weight** | Default 10%. How much prompts contribute to loss vs. responses |

📖 [Back to book summary](../00-book-overview/summary.md)
