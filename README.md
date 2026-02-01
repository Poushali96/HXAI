### Files

- **HXAI.ipynb**  
  Implements the full HXAI pipeline using **synthetically generated household energy data**.  
  This notebook is used for:
  - Controlled evaluation of privacy–utility trade-offs  
  - Privacy budget negotiation experiments  
  - System-level behavior analysis under repeated queries  

- **HXAIREAL.ipynb**  
  Implements HXAI using **only publicly available real-world datasets**.  
  This notebook reproduces the main experimental results reported on real data, including:
  - Zonal explanation aggregation  
  - Differential privacy noise injection  
  - Explanation utility, ranking stability, and semantic robustness analysis  

- **household_device_usage.csv**  
  A **synthetic energy consumption dataset** generated solely for experimental evaluation.  
  It does not contain real household data or personally identifiable information.

- **LICENSE**  
  Open-source license for code reuse.

---

## Data Sources

### Synthetic Data
Synthetic household energy consumption data are generated programmatically to support controlled experimentation, system-level evaluation, and privacy–utility trade-off analysis.  
No real households, users, or personal data are represented.

### Real Data (Publicly Available)
All real-data experiments rely exclusively on **open, publicly available benchmark datasets**, commonly used in energy and time-series research:

- **UCI Appliances Energy Prediction Dataset**  
  Hourly residential energy consumption with environmental and temporal features.

- **UCI Individual Household Electric Power Consumption Dataset**  
  Large-scale, minute-level household electricity usage data spanning multiple years.

- **UCI Bike Sharing Dataset (Hourly)**  
  Urban demand dataset with moderate feature correlation, used to test generalization beyond household energy data.

These datasets contain no personally identifiable information and are released for research purposes.  
Dataset access links, preprocessing steps, and feature construction are fully documented inside **HXAIREAL.ipynb**.

---

## Reproducibility

All experiments reported in the paper can be reproduced using the notebooks provided in this repository.

Each notebook:
- Is fully self-contained  
- Includes preprocessing, model training, explanation generation, and evaluation  
- Produces the figures and metrics reported in the paper  

Random seeds are fixed where applicable to ensure consistent and reproducible results.

---

## Ethical Considerations

HXAI is designed with privacy preservation as a first-class objective.  
Raw household-level data and noise-free explanations are never shared externally within the framework. Differential privacy mechanisms are explicitly enforced to bound information leakage under repeated and adaptive queries.

This repository contains **no sensitive data** and introduces **no new data collection mechanisms**.

---

## Anonymous Release Note

This repository is shared for **anonymous peer review only**.  
All identifying information has been removed or anonymized in compliance with double-blind review policies.

---

## Questions

For questions related to the methodology or reproduction of results, please refer to the accompanying paper.
