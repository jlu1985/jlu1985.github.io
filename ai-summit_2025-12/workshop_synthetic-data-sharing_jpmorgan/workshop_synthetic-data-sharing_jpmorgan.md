Synthetic Data sharing - securing our data for sharing between production and other environments while ensuring privacy using statistical methods

## Why Synthitic Data?

Real Data is valuable and importnat but it
- difficult to obtain
- sensitive
- costly to label
- 

## What is synthetic data?
A variation of real data or data inspired by real process

- Created by Transformation of real data
- Created by simulation

## How can synthetic data be used?

- Liberate
- Augment
- Test

## Levels of Synthetic Data
### Level 1: Obscure PII

mask the PII

### Level 2: Obsure PII + Noise

add some fake values

### Level 3: Synthesized Rows

use statistical models to generate new rows

### Level 4: Synthesized Rows + Test

Tendency the model memorieze the data

### Level 5: Calibrated Simulation

Real System: NYSE

Simulation: ABIDES

Synthetic Data: Training Logs

### Level 6: Uncalibrated Simulation

Real System: Documents
Simulation: Bayesian Network
Sythnetic Data: Sythesized Documents


# Agenda

## Introduction to Financial Data
## Tabular Data

The most common format in commercial finance are tabular data:

| ID  | Age | Credit Score | Trans Amount|
|-----|-----|--------------|-------------|
| 001 | 25  | 700          | 100.00      |
| 002 | 45  | 650          | 250.00      |
| 003 | 35  | 800          | 300.00      |

### Generation and Evaluation (Level3)

- Tranditional Approaches:
  - Cons: Hard to setup automatically, require manual work
- Gaussan Distribution

#### Generative Models for tabular data (Level 3)

Deep Learning Approaches

1. GAN-based: CTGAN, AdsGAN
   - Generative Adversarial Networks use two competing neural networks to generate synthetic data. CTGAN (Conditional Tabular GAN) is specifically designed for tabular data with mixed data types.

2. VAE-based: TVAE
   - Variational Autoencoders compress data into a latent space and reconstruct it. TVAE (Tabular VAE) learns probabilistic representations of data distributions for generating new samples.

3. Normalizing Flows: FourierFlow
   - Normalizing flows transform simple distributions into complex ones through invertible functions. FourierFlow uses Fourier features to model dependencies in tabular data effectively.

4. Diffusion-based: TabDDP
   - Diffusion models gradually add noise to data and learn to reverse the process. TabDDP applies this approach to tabular data generation by learning the denoising process.

5. LLM-based: GReaT (Generative Relation Tabular)
   - Large Language Models can be repurposed for tabular data by treating columns as tokens and rows as sequences. GReaT leverages LLM's generative capabilities to produce realistic synthetic tabular records.

#### Synth City

Open-Source python library (Cambridge University)

### Evaluate Synthetic Data

Goal: How similar is syntethic data to real data?

Distribution-Level Metrics:

1. Kolmogorov-Smirnov Test
    a. Compare marginal distributions
2. Chi-Squared Test
    a. Compare categorical distributions    
3. Wasserstein Distance:
    a. Earth mover's distance
4. Maximum Mean Discrepancy (MMD)
    a. Kernel-based distance metric
5. Correlation Analysis
    a. Correlation matrices comparison

### Evaluate Synthetic Data - Downstream Performance

Does systhetic data work for ML tasks?
Machine Learning Utility:

1. Train on Synthetic, Test on Real (TSTR)
    a. Train ML model on synthetic data, evaluate on real data


Sythn City Tutorial
### Privacy and