# Denoising Diffusion Implicit Models (DDIM)

## Overview
Denoising Diffusion Implicit Models (DDIM) generalize DDPM to non-Markovian forward processes. Because the forward process is deterministic given $x_0$, the generation process can skip steps, allowing much faster sampling without retraining the model.

## Diagram
```mermaid
flowchart LR
    x_T["Noise (x_T)"] -->|Deterministic ODE Step| x_t["Intermediate (x_t)"]
    x_t -->|Deterministic ODE Step| x_0["Clean Sample (x_0)"]
```

## Features
- Shorter sampling times (20-50 steps instead of 1000).
- Deterministic encoding/reconstruction.

[Back to README](../README.md)
