# JBHI-1: Calibration-Aware Multimodal Deep Learning for Diabetic Retinopathy

This repository contains the experimental artifacts, evaluation results, and figures associated with the JBHI submission on calibration-aware and seed-stable deep learning models for diabetic retinopathy (DR) classification.

The focus of this work is not only predictive performance, but also **probability calibration**, **robustness across random seeds**, and **generalization behavior** on APTOS and Messidor-2 benchmarks.

---

## Repository Structure

JBHI_1/
├── configs/ # Experiment configurations, seeds, environment metadata
├── figures/ # Figures used in the manuscript
├── metrics_fixed/ # Final, cleaned evaluation metrics (used for reporting)
├── predictions/ # Selected model probability outputs (CSV)
├── sdi/ # Stability / diagnostic analysis outputs
├── splits/ # Dataset split definitions (JSON)
├── tables/ # Tables used in the manuscript
├── JBHI_1.pdf # Submitted manuscript (JBHI version)
└── .gitignore

yaml
Copy code

---

## Datasets

Experiments are conducted using publicly available retinal fundus datasets:

- **APTOS 2019** (primary evaluation)
- **Messidor-2** (external validation)

Dataset files are **not included** in this repository due to licensing constraints.  
All experiments are reproducible using the provided split definitions and configurations.

---

## Experimental Protocol

- Multiple architectures evaluated (e.g., ResNet, EfficientNet, ViT variants)
- Multiple random seeds per configuration
- Calibration analysis performed on uncalibrated and calibrated outputs
- Metrics aggregated across seeds for robustness assessment

Reported results are based on **finalized metrics only** (`metrics_fixed/`) to avoid ambiguity or metric leakage.

---

## Reproducibility Notes

- Training checkpoints and logs are intentionally excluded to keep the repository lightweight and reviewer-friendly.
- All configuration files, dataset splits, and final metrics required to reproduce reported results are included.
- Environment and dependency snapshots are provided in `configs/`.

---

## Manuscript

`JBHI_1.pdf` corresponds to the version submitted to IEEE Journal of Biomedical and Health Informatics.

Figures and tables in the manuscript directly map to the contents of the `figures/` and `tables/` directories.

---

## Disclaimer

This repository is intended for **research transparency and reproducibility**.  
It is not optimized as a plug-and-play training framework.

---

## Contact

For questions related to the experiments or repository structure, please contact the corresponding author listed in the manuscript.
