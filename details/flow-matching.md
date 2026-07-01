# Flow Matching / Rectified Flow Models

## Overview
Flow Matching is a path-based training method for generative models that models the vector field of a probability flow ODE. Rather than predicting Gaussian noise, it learns to map source noise to destination data along straight trajectories.

## Diagram
```mermaid
flowchart LR
    Noise["Noise (t=0)"] -->|Straight-Line Trajectory (ODE Flow)| Data["Data (t=1)"]
```

## Advantages
- Straight trajectories allow extremely fast sampling (as few as 4 steps with consistency distillation).
- Stable, simulation-free training.

[Back to README](../README.md)
