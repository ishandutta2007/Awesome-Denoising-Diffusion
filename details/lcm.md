# Latent Consistency Models (LCM)

## Overview
Latent Consistency Models enable extremely fast image generation (1-4 steps) by learning a consistency function that directly maps any point along the flow trajectory to the origin (the clean image).

## Diagram
```mermaid
flowchart LR
    z_t["Latent Noisy (z_t)"] -->|Consistency Model Single Step| z_0["Clean Output (z_0)"]
```

[Back to README](../README.md)
