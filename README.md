
![DALL·E-2025-01-23-09 33](https://github.com/user-attachments/assets/41335c7c-1862-40ff-a5dc-4eef8acbbb3b)
# Preference Alignment

This repository explores methods for aligning language models with human preferences. While supervised fine-tuning adapts models to specific tasks or domains, preference alignment ensures that their outputs match human expectations and values. The focus here is on two innovative algorithms: **Direct Preference Optimization (DPO)** and **Odds Ratio Preference Optimization (ORPO)**.

---

## Overview

Preference alignment methods typically involve multiple stages:
1. **Supervised Fine-Tuning (SFT):** Adapts models to specific tasks or domains.
2. **Preference Alignment:** Refines outputs to better align with human preferences.

This repository highlights:
- **DPO**, a simpler alternative to traditional RLHF (Reinforcement Learning from Human Feedback), which directly optimizes model behavior using preference data.
- **ORPO**, a novel approach that combines instruction tuning and preference alignment into a unified, single-stage process.

---

## Key Components

### Direct Preference Optimization (DPO)
DPO simplifies preference alignment by eliminating the need for separate reward models and reinforcement learning. Instead, it directly optimizes language models using preference datasets, offering a more stable and efficient alternative to RLHF. This repository includes:
- A detailed implementation of DPO using pre-trained models.
- Notebooks of fine-tuning models on preference datasets to improve alignment.

---

### Odds Ratio Preference Optimization (ORPO)
ORPO introduces a unified approach to instruction tuning and preference alignment, combining:
- Negative log-likelihood loss with an odds ratio term at the token level.
- A single-stage training process that eliminates the need for reference models.
- Improved computational efficiency and strong performance on benchmarks.

This repository demonstrates:
- ORPO fine-tuning workflows.
- Comparisons between ORPO and DPO on various datasets.

---

## Notebooks Overview

This repository includes interactive notebooks to demonstrate DPO and ORPO in practice:

### DPO Training
- **Description:** Fine-tune models using preference datasets with the DPOTrainer.
- **What's Inside:**
  - Fine-tuning a model with `trl-lib/ultrafeedback_binarized`.
  - Experimenting with your own preference datasets.
- **Notebook:** [DPO Fine-Tuning](./notebooks/dpo_finetuning.ipynb)

### ORPO Training
- **Description:** Explore the unified approach of ORPO for both instruction tuning and preference alignment.
- **What's Inside:**
  - Training a model using instruction and preference data.
  - Experimenting with different loss weightings and configurations.
  - Comparing ORPO results with DPO.
- **Notebook:** [ORPO Fine-Tuning](./notebooks/orpo_finetuning.ipynb)

---

## Why Explore DPO and ORPO?

- **DPO:** Provides a straightforward and efficient alternative to RLHF, making preference alignment accessible without complex setups.
- **ORPO:** Offers an innovative single-stage training method, reducing computational overhead while achieving strong results.

This repository is a practical guide to implementing these algorithms and understanding their potential for improving language model alignment.

