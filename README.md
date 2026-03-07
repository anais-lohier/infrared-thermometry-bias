# Measurement Uncertainty and Demographic Encoding in Infrared Facial Thermometry

This repository contains the analysis code for the retrospective study examining the relationship between administratively encoded ethnicity and facial infrared temperature measurements.

## Project Overview
The study evaluates whether statistically detectable differences in facial temperature across demographic groups are clinically meaningful or simply artifacts of measurement resolution. Using a dataset of $N=951$ adults, the analysis focuses on:
- Inner-canthus maximum ($T_{CEmax}$).
- Full-face maximum ($T_{max}$).

## Key Findings

**Statistical vs. Clinical Significance:** While ANOVA showed significant differences ($p < 0.001$), group mean variations ($0.2–0.3^{\circ}C$) remained within the nominal accuracy limits of IRT systems ($\pm0.3–0.4^{\circ}C$).

**Sensitivity:** Monte Carlo simulations demonstrate that group-mean ordering destabilizes when accounting for device-level noise.

**Conclusion:** Observed differences likely reflect statistical regularities at the resolution boundary rather than intrinsic physiological differentiation.

## Contents

`preprocessing/`: Scripts for aggregating round-level measurements and assessing within-subject repeatability.

`analysis/:` Fixed-effects ANOVA models and Kruskal-Wallis robustness checks.simulations/: Monte Carlo perturbation scripts for sensitivity analysis.

`figures/:` Code to generate distribution violin plots and effect size stability graphs.

## Data Source
[PhysioNet Facial and Oral Temperature Data](https://physionet.org/content/face-oral-temp-data/1.0.0/)
