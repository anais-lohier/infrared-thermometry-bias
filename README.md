# Measurement Uncertainty and Demographic Encoding in Infrared Facial Thermometry

Reproducible analysis code for a retrospective study examining whether administratively encoded ethnicity categories produce clinically meaningful differences in facial infrared temperature measurements.

**Preprint:** [Normative Temperature, Demographic Categories, and the Limits of Infrared Thermometry](https://www.medrxiv.org/content/10.64898/2026.10.19.26365925v1) (medRxiv, 2026)  
**Authors:** Anaïs Lohier, Angela G. Campbell, David Chartash

## Overview

Using a publicly available thermographic dataset ($N = 951$ adults, aged 18–30), the analysis evaluates inner-canthus maximum ($T_{\text{CEmax}}$) and full-face maximum ($T_{\max}$) temperatures across five ethnicity categories. ANOVA detected statistically significant differences ($p < 0.001$), with group mean differences of 0.2–0.3°C that fell within nominal device accuracy limits (±0.3–0.4°C). Monte Carlo simulations showed that the ordering of group means destabilizes under perturbations scaled to instrument noise.

## Repository contents

| File | Description |
|------|-------------|
| `thermometry_analysis.qmd` | Full reproducible analysis: cohort construction, descriptive statistics, ANOVA, Monte Carlo sensitivity, and figures |
| `data_pre_processed.csv` | Participant-level analytic dataset with averaged thermal features |
| `ICI_groups1and2.csv` | Original data from the PhysioNet source |
| `eta2_sensitivity.pdf` | Figure 3: Monte Carlo effect size sensitivity |
| `mean_facial_temp_combined.pdf` | Figure 2: Temperature distributions by ethnicity |

## Data source

Derived from [Facial and Oral Temperature Data](https://physionet.org/content/face-oral-temp-data/1.0.0/) (PhysioNet, Wang et al. 2023). See the original dataset for terms of use.

## Reproduction

Render the analysis in R with:

```bash
quarto render thermometry_analysis.qmd
```

Requires R packages: `dplyr`, `readr`, `tidyr`, `stringr`, `knitr`, `car`, `effectsize`, `ggplot2`, `patchwork`.

## Citation

If you use this code, please cite the preprint:

> Lohier A, Campbell AG, Chartash D. Normative Temperature, Demographic Categories, and the Limits of Infrared Thermometry. *medRxiv*. 2026. https://www.medrxiv.org/content/10.64898/2026.10.19.26365925v1
