# Fine-Grained Layout Control Deficit

## Overview
While text prompts capture general concepts, they lack precision for pixel-level layout, human posture, or edge alignment. ControlNet and IP-Adapter solve this by introducing secondary conditioning networks.

## Diagram
```mermaid
flowchart LR
    Pose["Pose Skeleton / Depth Map"] -->|ControlNet| Features["Spatial Feature Control"]
    Text["Text Prompt"] -->|Base U-Net/DiT| Image["Generated Image"]
    Features -->|Inject| Image
```

[Back to README](../README.md)
