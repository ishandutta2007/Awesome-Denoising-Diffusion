# Denoising Diffusion Probabilistic Models (DDPM)

## Overview
Denoising Diffusion Probabilistic Models (DDPM) are generative models that learn the data distribution by reversing a gradual noise-injection process. Inspired by nonequilibrium thermodynamics, DDPM defines a forward Markov chain that progressively adds Gaussian noise to the data, and a reverse Markov chain that learns to remove the noise.

## Mathematical Formulation
The forward process is defined as:
$$q(x_1, \dots, x_T | x_0) = \prod_{t=1}^T q(x_t | x_{t-1})$$
$$q(x_t | x_{t-1}) = \mathcal{N}(x_t; \sqrt{1 - \beta_t} x_{t-1}, \beta_t \mathbf{I})$$

The reverse process is trained to approximate these transitions:
$$p_\theta(x_0, \dots, x_T) = p(x_T) \prod_{t=1}^T p_\theta(x_{t-1} | x_t)$$
$$p_\theta(x_{t-1} | x_t) = \mathcal{N}(x_{t-1}; \mu_\theta(x_t, t), \Sigma_\theta(x_t, t))$$

## Diagram
```mermaid
flowchart LR
    x0["Clean Data (x0)"] -->|Forward Noise Step| xt["Noisy Data (xt)"]
    xt -->|Forward Noise Step| xT["Pure Gaussian Noise (xT)"]
    xT -->|Reverse Denoising Step (Learned U-Net)| xt
    xt -->|Reverse Denoising Step (Learned U-Net)| x0
```

## Pros and Cons
- **Pros:** High-fidelity sample generation, stable training compared to GANs.
- **Cons:** Extremely slow sampling due to hundreds of sequential evaluation steps.

[Back to README](../README.md)
