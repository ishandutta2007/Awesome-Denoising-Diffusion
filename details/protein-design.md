# De Novo Protein Design & Molecular Docking

## Overview
Diffusion models applied to biotech treat molecular atomic coordinates or protein backbones as point clouds. They denoise random structural fields into biochemically stable folds.

## Diagram
```mermaid
flowchart LR
    Rand["Random 3D Coordinates"] -->|SE(3)-Equivariant Denoising| Protein["Stable Protein Backbone"]
```

[Back to README](../README.md)
