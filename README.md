# IBD-NPM Reproducibility Package

This package contains the processed feature tables, experiment outputs, and evaluation scripts used for the study:

Intent--Behavior Discordance as an Explainable Analytical Signal for Malicious npm Package Triage

## Scope

The study is limited to the npm ecosystem. The processed artifacts support reproducibility of the reported experiments. Exact reconstruction from live registry sources may vary over time because package metadata and availability can change.

## Package Structure

- `data/features/attacked_feature_sets/`
  - Processed feature tables for clean and presentation-manipulated settings:
    - A0_Clean
    - A1_BlankBasic
    - A2_IntentSpoof
    - A3_RoleSpoofFull
    - A4_SelectiveDeception
    - A5_BenignReadmePrefix

- `results/main/`
  - Clean and matched evaluation outputs
  - Attack evaluation outputs
  - Resampling outputs
  - Calibration diagnostics
  - Stratified stability outputs

- `results/reviewer_stats/`
  - Additional uncertainty-aware analyses:
    - repeated clean evaluation
    - paired FullModel vs Full+Discordance comparison
    - attack-conditioned repeated analysis
    - heuristic capability-count sanity baselines

- `scripts/`
  - Main pipeline script used for corpus processing and experiment execution.

## Main Reproducibility Notes

The most stable way to reproduce the reported results is to use the processed feature tables included in this package. From-scratch reconstruction from live npm registry sources may not be temporally invariant.

## Required Python Packages

Recommended:
- Python >= 3.10
- pandas
- numpy
- scikit-learn
- scipy

## Random Seed

The main reported repeated analyses use random_state = 42.

## Data Availability Statement Draft

All processed feature tables, experiment outputs, configuration artifacts, and evaluation scripts necessary to reproduce the reported analyses are provided in the accompanying reproducibility package. The study uses publicly documented malicious-package sources and npm package metadata; however, exact regeneration from live online registries may vary over time due to package updates, removals, and metadata changes. Therefore, the processed artifacts are provided as the stable basis for reproducing the reported results.
