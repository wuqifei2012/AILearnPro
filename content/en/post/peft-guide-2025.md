---
title: "Practical Guide to Parameter-Efficient Fine-Tuning in 2025"
summary: "A comprehensive practical guide to PEFT methods including LoRA, QLoRA, AdaLoRA, and more — with code examples and benchmarks."
description: "Everything you need to know about parameter-efficient fine-tuning, from theory to practice."
date: 2025-10-20
authors:
  - admin
tags:
  - "Fine-tuning"
  - "LLM"
  - "Tutorial"
---

Parameter-efficient fine-tuning (PEFT) has become essential for adapting large language models to specific tasks without the computational cost of full fine-tuning.

## Why PEFT Matters

Full fine-tuning of a 70B parameter model requires hundreds of GPUs and days of training. PEFT methods like LoRA achieve comparable performance with 1000x fewer trainable parameters.

## Methods Compared

### LoRA (Low-Rank Adaptation)
Injects trainable rank decomposition matrices into transformer layers while keeping pre-trained weights frozen. Simple, effective, widely adopted.

### QLoRA (Quantized LoRA)
Combines 4-bit quantization with LoRA, enabling fine-tuning of 65B parameter models on a single GPU.

### AdaLoRA
Adaptively allocates parameter budgets based on importance scoring, achieving better performance with fewer parameters.

### IA³ (Infused Adapter by Inhibiting and Amplifying Inner Activations)
Scales inner activations of pretrained models with three tiny learnable vectors per layer.

## Code Example

```python
from peft import LoraConfig, get_peft_model

config = LoraConfig(
    r=16,
    lora_alpha=32,
    target_modules=["q_proj", "v_proj"],
    lora_dropout=0.1,
)
model = get_peft_model(base_model, config)
model.print_trainable_parameters()
# trainable params: 4,194,304 || all params: 7,424,243,712
```

## Benchmark Results

On the GLUE benchmark, LoRA achieves 98.2% of full fine-tuning performance with 0.1% of trainable parameters. QLoRA maintains this with 4-bit quantization, reducing memory usage by 75%.
