# Score-Based Generative SDEs

## Overview
This formulation models the noise injection and reverse denoising as continuous-time Stochastic Differential Equations (SDEs). By scaling the number of steps to infinity, it establishes a unified mathematical framework for diffusion models and score matching.

## Diagram
```mermaid
flowchart TD
    SDE["Forward SDE (Noise Injection)"] -->|Continuous Time| Noise["Noise Distribution"]
    Noise -->|Reverse SDE (Score Predictor)| Data["Data Distribution"]
```

## Benefits
- High-quality sample generation.
- Exact likelihood computation and ODE representation.

[Back to README](../README.md)
