# Diffusion Transformers (DiT)

## Overview
Diffusion Transformers (DiT) replace the traditional convolutional U-Net backbone in diffusion models with a Vision Transformer (ViT) architecture. Images or latents are sliced into a sequence of patch embeddings, which are then processed by transformer blocks.

## Diagram
```mermaid
flowchart TD
    Input["Latent Input"] -->|Patchify| Patches["Patch Embeddings"]
    Patches -->|Linear Projection + Position Embeddings| Trans["Transformer Blocks (DiT)"]
    Trans -->|Linear + Depatchify| Output["Denoised Latent Output"]
```

## Key Features
- High scalability: follows predictable scaling laws similar to LLMs.
- Efficient representation of multi-modal data.

[Back to README](../README.md)
