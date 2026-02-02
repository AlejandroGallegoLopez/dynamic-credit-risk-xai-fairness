# Dynamic Credit Risk, XAI, Fairness and Governance – Research Project

Research project from the Internal Student Program at Universidad de Sevilla:  
**“Dynamic Risk Modeling and Financial Decision Systems: XAI, Profitability and Fairness.”**

This repository focuses on what happens AFTER a baseline credit scoring model is built:
- global & local explainability (SHAP, LIME)
- fairness analysis and bias mitigation
- robustness and governance for real-world deployment.

> All data used here is synthetic or public. Real institutional data and some internal configurations are not included.

---

## 1. Project Overview

The project is structured in several phases:

1. **Global Explainability with SHAP**  
   - Global feature importance and dependence analysis for a reference XGBoost model.  
   - Economic interpretation of key drivers (external scores, credit utilization, goods price, etc.).  
   - Early detection of sensitive variables (e.g. gender) and equity concerns.

2. **Local Explainability with LIME and Client Profiles**  
   - Local explanations for representative client profiles (good payer, borderline, bad payer).  
   - Operational rules derived from LIME to support human risk committees.  
   - Traceability of model decisions at individual level.

3. **Fairness and Bias Analysis**  
   - Group-based metrics: approval rates, FPR, FNR, AUC by group.  
   - Disparate Impact Ratio and 4/5 rule.  
   - Identification of asymmetric error trade-offs between groups.

4. **Bias Mitigation and Adversarial Robustness**  
   - Reweighting, threshold adjustment and fairness-aware strategies.  
   - Adversarial robustness analysis: minimal perturbations to flip decisions and most vulnerable features.

5. **Governance & Trust Framework**  
   - Risk zones (low/medium/high) and human-in-the-loop policies.  
   - Fairness flags (GREEN/AMBER/RED) and decision rules.  
   - Roles & responsibilities (Data Science, Risk, Compliance, MLOps) and monitoring.

---

## 2. Repository Structure

```text
src/
  data_preprocessing/   # loaders, cleaning, train/test splits
  feature_engineering/  # domain & statistical features
  modeling/             # model training, scoring
  xai/                  # SHAP & LIME utilities
  fairness/             # fairness metrics & dashboards
  mitigation/           # reweighting, thresholds, mitigation strategies
  governance/           # risk zones, flags, monitoring helpers

notebooks/
  01_shap_global.ipynb          # SHAP global importance & dependence
  02_lime_local_profiles.ipynb  # local LIME explanations & client profiles
  03_fairness_metrics.ipynb     # DI, FPR/FNR, group metrics
  04_bias_mitigation.ipynb      # reweighting, threshold tuning by group
  05_robustness_governance.ipynb# adversarial robustness & governance

reports/
  resolution_T1_shap.pdf        # phase 1: SHAP global analysis
  resolution_T2_lime_fairness.pdf # phase 2: LIME and fairness setup
  resolution_T3_mitigation_governance.pdf # mitigation & governance summary

results/
  figures/                      # SHAP plots, LIME profiles, fairness panels, robustness plots
  metrics/                      # CSVs with model & fairness metrics

data/
  synthetic/                    # synthetic datasets
  README.md                     # schema & instructions

```

## 3. Academic Context

This repository collects the research work from the Internal Student Program:
Department of Economic Analysis and Political Economy, Universidad de Sevilla

Topic: Dynamic credit risk modeling with XAI, profitability and fairness

Focus:
- SHAP/LIME-based explainability
- fairness metrics and bias mitigation
- adversarial robustness and governance for high‑risk AI systems (credit scoring)
