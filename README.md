# Measurement Uncertainty and Demographic Encoding in Infrared Facial Thermometry

This repository contains the reproducible analysis code for a retrospective study examining whether administratively encoded ethnicity categories produce clinically meaningful differences in facial infrared temperature measurements.

## Overview

Using a publicly available thermographic dataset ($N = 951$ adults, aged 18–30), the analysis evaluates inner-canthus maximum ($T_{\text{CEmax}}$) and full-face maximum ($T_{\max}$) temperatures across five ethnicity categories. While ANOVA detected statistically significant differences ($p < 0.001$), group mean variations of 0.2–0.3°C fell within nominal device accuracy limits (±0.3–0.4°C). Monte Carlo simulations showed that group-mean ordering destabilizes under perturbations scaled to instrument noise.

## Repository Contents

| File | Description |
|------|-------------|
| `thermometry_analysis.qmd` | Full reproducible analysis: cohort construction, descriptive statistics, ANOVA, Monte Carlo sensitivity, and figures |
| `data_pre_processed.csv` | Participant-level analytic dataset with averaged thermal features |
| `ICI_groups1and2.csv` | Original data from PhysioNet source |
| `eta2_sensitivity.pdf` | Figure 3: Monte Carlo effect size sensitivity |
| `mean_facial_temp_combined.pdf` | Figure 2: Temperature distributions by ethnicity |

## Data Source

Derived from [Facial and Oral Temperature Data](https://physionet.org/content/face-oral-temp-data/1.0.0/) (PhysioNet, Wang et al. 2023). See the original dataset for terms of use.

## Reproduction

Render the analysis in R with:
```bash
quarto render thermometry_analysis.qmd
```

Requires R packages: `dplyr`, `readr`, `tidyr`, `stringr`, `knitr`, `car`, `effectsize`, `ggplot2`, `patchwork`.
