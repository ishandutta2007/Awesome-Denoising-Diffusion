# Latent Diffusion Models (LDMs)

## Overview
Latent Diffusion Models (LDMs) resolve the computational bottleneck of pixel-space diffusion models by performing the diffusion process in a lower-dimensional latent space. A trained Autoencoder (VAE) compresses high-resolution images into latents, where a U-Net is trained to perform denoising.

## Diagram
```mermaid
flowchart TD
    Pixel["Pixel Space Image (x)"] -->|Encoder (E)| Latent["Latent Space Representation (z)"]
    Latent -->|Diffusion Denoising Process| Denoiser["U-Net Denoiser (z_t)"]
    Denoiser -->|Decoder (D)| Recon["Reconstructed Image (x_hat)"]
```

## Significance
- Allows training and inference of high-quality image generators on consumer-grade GPUs.
- Forms the core framework for Stable Diffusion 1.x and 2.x.

[Back to README](../README.md)
