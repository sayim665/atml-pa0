# ATML — Assignment 0

EE-5102 / CS-6304 Advanced Topics in Machine Learning — Assignment 0 (Introduction)

**Deadline:** 20 August 2026
**Status:** In progress

## Overview

This repo contains code, experiments, and results for PA0, covering four areas:

1. **Task 1 — ResNet-152**: transfer learning on CIFAR-10, skip-connection ablation, feature hierarchy visualization, transfer learning comparisons.
2. **Task 2 — Vision Transformers**: pretrained ViT classification, CLS-token attention map visualization, patch masking robustness, CLS vs mean-pooled linear probes.
3. **Task 3 — CLIP**: zero-shot classification on STL-10, modality gap analysis, Procrustes alignment.
4. **Task 4 — VAE**: variational autoencoder on MNIST, latent space visualization, reconstruction and generation quality, comparison with Doersch's reference implementation.

The full write-up with analysis and discussion is in [`report/`](./report), built from the NeurIPS LaTeX template.

## Repo structure

```
atml-pa0/
├── task1_resnet/       # ResNet-152 transfer learning + ablations
├── task2_vit/          # ViT classification + attention visualization
├── task3_clip/         # CLIP zero-shot + modality gap
├── task4_vae/          # VAE on MNIST
├── figures/            # Saved plots/visualizations used in the report
├── report/             # NeurIPS-format LaTeX report
├── requirements.txt
└── README.md
```

Each task folder contains:
- `*.ipynb` — the Colab notebook for that task (also viewable directly on GitHub)
- `results/` — saved metrics, checkpoints (small ones only), and figures specific to that task

## Setup

All experiments were run on Google Colab (free-tier T4 GPU). To reproduce locally:

```bash
python -m venv venv
source venv/bin/activate       # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

## Notes

- Individual submission; developed independently. GPT/Claude used for coding assistance per assignment guidelines, with the requirement that I understand and can explain the underlying model dynamics — see report for discussion tied to each experiment.
- Datasets (CIFAR-10, STL-10, MNIST) are downloaded on the fly via `torchvision.datasets` and are not committed to this repo.
