# Text-to-Image Foundation Engines

## Overview
Commercial and open-weight models (like Midjourney, FLUX, Stable Diffusion) process language prompts using language encoders (CLIP, T5) to guide spatial diffusion generation.

## Diagram
```mermaid
flowchart LR
    Text["User Prompt"] -->|CLIP / T5 Encoders| Embeds["Text Embeddings"]
    Embeds -->|Cross-Attention| DiT["Denoising Backbone (DiT / U-Net)"]
    DiT -->|Generation| Output["Final Image"]
```

[Back to README](../README.md)
