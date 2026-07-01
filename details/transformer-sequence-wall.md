# Transformer Sequence Length Wall

## Overview
Generating high-resolution images or videos requires dividing latent maps into a large number of patch tokens. This scales the self-attention computation quadratically ($O(N^2)$), causing memory bottlenecks on GPUs.

## Solutions
- **FlashAttention:** IO-aware register caching.
- **Grouped-Query Attention (GQA):** Query pooling to optimize memory access.

## Diagram
```mermaid
flowchart TD
    Img["1024x1024 Image"] -->|Patches| Seq["Long Token Sequence (N)"]
    Seq -->|Quadratic Bottleneck| Attn["Self-Attention O(N^2) VRAM Wall"]
    Attn -->|Optimize| Flash["FlashAttention / GQA Acceleration"]
```

[Back to README](../README.md)
