# Lab 3: Bottom-Up Steel Emissions with Uncertainty

**Group:** `aidams-lab3-gronier-viardlaroque-afopa-beghin`  
**Group Members:**
- Pollux Gronier (B00822392) — Submitter
- Saty Viard Laroque (B00822312)
- Fabrice Afopa (B00817356)
- Eliott Beghin (B00824999)

**Repository:** https://github.com/Polluxgnr/lab3

---

## Overview

This project implements a bottom-up emissions accounting pipeline and comprehensive uncertainty quantification for China's steel industry (2020–2030) using the Global Iron and Steel Tracker (GIST) dataset.

- **Part A (Emissions Pipeline):** Operational status filtering, technology classification (BF-BOF, EAF, Other), technology-level utilization, plant-level production attribution, emission factor mapping (Hasanbeigi 2019), company aggregation, and 2025–2030 projections.
- **Part B (Uncertainty Quantification):**
  - Aleatoric vs. Epistemic vs. Scenario uncertainty classification.
  - Verification against official statistics (worldsteel macro accounts) uncovering the reporting coverage gap (~9.5% coverage in 2023).
  - Like-for-like matched plant utilization rates eliminating denominator bias.
  - Non-parametric bootstrapping and optional Bayesian credible intervals.
  - Monte Carlo simulation (1,000 draws) combining utilization and emission factor distributions.
  - Policy scenario analysis (baseline S0, -30% BF-BOF capacity retirement S1, -10% demand drop S2) and IPCC calibrated communication for financial risk committees.

---

## Requirements & Environment

Python 3.10+ with standard data science packages:
```bash
pip install numpy pandas matplotlib scipy openpyxl jupyter nbconvert
```

---

## How to Run

1. Place the tracker Excel dataset in the working directory:
   - `Plant-level_data_Global_Iron_and_Steel_Tracker_June_2026_V1.xlsx` (or set `GIST_PATH` environment variable).
2. Open and run the notebook:
   ```bash
   jupyter notebook lab3.ipynb
   ```
   Select **Kernel -> Restart & Run All**.
3. All cells run sequentially in under 30 seconds with pre-computed outputs preserved in the repository version.
