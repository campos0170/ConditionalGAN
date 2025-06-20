# ConditionalGAN: Generating Single-Molecule Spike Traces

This repository contains code and documentation for training a **Conditional Generative Adversarial Network (cGAN)** to generate realistic single-molecule (SM) current traces. The work is part of an ongoing PhD dissertation focused on leveraging deep generative models for signal generation and augmentation in nanoscience experiments.

## 📘 Overview

Single-molecule datasets often lie at two extremes:

- **Big Data:** High-dimensional, noisy, and heterogeneous traces with rich but obscured physical information.
- **Small Data:** Long experimental hours with only a fraction of usable data due to the inherent limitations of nanopore and STM experiments.

This project addresses both extremes by using a cGAN to generate high-fidelity, synthetic current traces conditioned on class labels (e.g., spike vs. no spike). These synthetic traces can support data augmentation, improve downstream analysis, and enhance the interpretability of experiments.

## 🧠 Model Architecture

The Conditional GAN consists of:

- A **Generator** trained to produce realistic current traces from noise vectors and labels.
- A **Discriminator** trained to distinguish between real and synthetic traces while considering conditional labels.
- Optional components include skip connections, FFT-based losses, and auxiliary classifiers.

## 📈 Dataset

The training data consists of current vs. time signals recorded from nanopore or STM-based experiments. Each trace includes spike events which are believed to encode meaningful physical properties like molecular translocation, folding, or binding states.

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/campos0170/ConditionalGAN.git
   cd ConditionalGAN
