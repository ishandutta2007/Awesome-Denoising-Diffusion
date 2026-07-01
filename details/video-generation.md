# Spatio-Temporal Video Generation

## Overview
Video models extend spatial generation to temporal sequences by tokenizing video clips into 3D spacetime cubes (patches across width, height, and time).

## Diagram
```mermaid
flowchart TD
    Video["Video Clip"] -->|3D Patchification| Cubes["Spacetime Cubes"]
    Cubes -->|Temporal + Spatial Attention| DiT["Diffusion Transformer"]
    DiT -->|Denoising| Output["Generated Video Frames"]
```

[Back to README](../README.md)
