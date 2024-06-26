# Generative vs. Predictive Models in Massive MIMO Channel Prediction

This repo is the implementation of our paper "Generative vs. Predictive Models in Massive MIMO Channel Prediction", <em>currently under review</em>.


## Highlights
- This work evaluates AE-based Generative and Predictive models, finding that Generative models excel in noisy settings. 
- Furthermore, we introduce a Vector Quantization (VQ)-based generative AE model (VQ-VAE) specifically for noisy mMIMO channel prediction. 
- The VQ-VAE model significantly surpasses traditional AE and other generative models, achieving up to approximately 15 [dB] NMSE accuracy gains over standard AEs and about 9 [dB] over VAE models.

<div align="center">
<img src="figure/fig1.png" alt="overview_vqvae" width="600" style="float:center" />
</div>


## Results

### Comparative Analysis: 
- [Qualitative Analysis] Comparison of Prediction Results from Generative and Predictive Models under Good ($γ$ = 30 [dB]) and Noisy ($γ$ = 0 [dB]) Channel Conditions (Latent dim. = 64).
<div align="center">
<img src="figure/fig2.png" alt="overview_vqvae" width="400" style="float:center" />
</div>

### OOD (Out-of-Distribution) Resultss

- [Generalization Capability] Prediction Results of the Proposed VQ-VAE on Out-Of-Distribution (OOD) Channels ($γ$ = 30 [dB], Latent dim. = 64).
<div align="center">
<img src="figure/fig3.png" alt="overview_vqvae" width="400" style="float:center" />
</div>

### Complexity Analysis

| #       | Inference time [s] | Training time [s]  | Memory [MB]  |
| ------- | ------------------ | ------------------ | ------------ |
| AE      | 3.374              | 329                | 358          |
| VAE     | 4.442              | 691                | 838          |
| VQ-VAE  | 5.340              | 1448               | 3776          |
