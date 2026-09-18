# Prompt-DT Reproduction

This repository contains my reproduction study of:

"Prompting Decision Transformer for Few-Shot Policy Generalization"

The project aims to reproduce the main experimental pipeline of Prompt-DT and explore the influence of trajectory prompt length on few-shot policy generalization.

---

## 1. Paper

Prompt-DT introduces trajectory prompts into Decision Transformer to achieve few-shot adaptation in offline reinforcement learning.

The original paper evaluates the method on MuJoCo control environments.

---

## 2. Environment

- OS: Ubuntu (WSL)
- Python: 3.8
- Framework: PyTorch
- Device: CPU

---

## 3. Reproduction

The reproduction process includes:

### Environment Setup

- Install dependencies
- Configure MuJoCo environments
- Prepare expert datasets

### Training

The model is trained on HalfCheetahDir expert demonstrations.

### Evaluation

The trained model is evaluated on target tasks:

- cheetah_dir-0
- cheetah_dir-1

Metrics:

- Return Mean
- Return Std

---

## 4. Results

Experimental results are organized as:

results/
├── original/
│
└── new/

`original/` contains the reproduction experiment.

`new/` contains additional prompt length experiments.

---

## 5. Additional Analysis

An additional experiment investigates:

"How does changing test-time prompt length influence policy performance?"

The trained model remains fixed while only the testing prompt length changes.

Detailed settings and analysis are provided in:

results/new/README.md


---

## 6. Limitations

Due to limited computational resources, experiments were conducted with reduced training iterations.

Therefore, the additional experiments are mainly used for exploratory analysis.

A more rigorous evaluation requires:

- longer training schedules
- multiple random seeds
- statistical analysis

---

## Citation

```bibtex
@inproceedings{xu2022prompting,
title={Prompting Decision Transformer for Few-Shot Policy Generalization},
author={Xu et al.},
booktitle={ICML},
year={2022}
}
