[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/COoZjc-Y)
# ESE 5390 Fall 2025 Final Project

Our group project focuses on the structural sensitivity of MobileNetV2 to INT8 quantization and identifies which architectural components must be retrained to recover accuracy lost under Post-Training Quantization (PTQ). Standard PTQ caused substantial feature drift in depthwise separable bottlenecks, motivating a series of quantization-aware training (QAT) ablations guided by activation drift analysis. We progressively expanded the retraining scope from classifier-only updates to depthwise and 1x1 projection layers, showing that partial retraining is unstable unless both components co-adapt. Incorporating asymmetric activation quantization into selective QAT configuration yielded 93.25% top-1 accuracy on CIAR-10 (within ~2% of the 95.49% FP32 baseline) while reducing model size by ~4x, demonstrating that targeted, drift-aware retraining can achieve near-baseline performance at a fraction of the computation and memory cost of full-network QAT. 

## Reproducible Artifact

A complete reproducible implementation with modular code, setup instructions, and experiment configurations is available in the [`demo/`](demo/) folder. See [`demo/README.md`](demo/README.md) for installation and usage instructions.

## Authors
* Norman Zhang (nzhang11)
* Jay Katyan (jkatyan)
* Neel Shejwalkar (nshej)
