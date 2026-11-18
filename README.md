# Does More Enthusiasm from Language Teachers Always Help?

**Functional Form and Cross-Country Variation in Reading Achievement in PISA 2018**

## Overview

This repository contains the supplementary materials and R code for the study examining the functional form of the association between perceived teacher enthusiasm and student reading achievement using PISA 2018 data.

The study investigates whether the association is approximately linear, exhibits diminishing returns, or reverses at higher levels of perceived teacher enthusiasm. It also examines the role of uniform responses to the four teacher enthusiasm items, within-school associations, mathematics achievement, and cross-country variation.

## Repository Contents

### Analysis Script

- `pisa_enthusiasm_analysis.R`: Main R script implementing data preparation, sample selection, statistical modelling, robustness analyses, country-level estimations, and subgroup analyses.

### Outputs

The `outputs/` directory contains the supplementary statistical results in CSV format:

| File | Description |
|---|---|
| `01_pooled_models.csv` | Pooled linear, quadratic, mixed-responder, school fixed-effects, mathematics, and related models |
| `02_interaction_uniform.csv` | Interaction models examining uniform response patterns |
| `04_sumscore_means.csv` | Reading achievement by enthusiasm-item sum score and response type |
| `05_gam_aic.csv` | AIC comparisons of linear, quadratic, and spline models |
| `06_country_full.csv` | Country-level estimates using the full analytical sample |
| `06_country_mixed.csv` | Country-level estimates restricted to mixed responders |
| `07_country_meta.csv` | Random-effects meta-analysis of country-level estimates |
| `08_english_subgroup.csv` | Models for students completing the questionnaire in English |
| `08b_english_interaction.csv` | Interaction analysis comparing English and other questionnaire-language groups |

## Data Source

The analysis uses the PISA 2018 student questionnaire dataset:

`CY07_MSU_STU_QQQ.sav`

The dataset is publicly available from the OECD PISA 2018 database:

https://www.oecd.org/pisa/data/2018database/

The original student-level dataset is not included in this repository. Researchers should obtain the dataset directly from the OECD and comply with its data-use conditions.

Place the downloaded SPSS file in the working directory before running the analysis script, or modify the data path specified at the beginning of the script.

## Software and Packages

The analysis was conducted using:

- R version 4.5.2
- haven
- data.table
- mgcv
- metafor
- ggplot2

The script sets the random seed to 2018 for the analysis step requiring random-number generation.

## Replication Instructions

1. Install R and the required packages.
2. Download the PISA 2018 student questionnaire dataset from the OECD.
3. Place `CY07_MSU_STU_QQQ.sav` in the working directory.
4. Run `pisa_enthusiasm_analysis.R`.
5. The script generates statistical output files in the designated output directory.

## Citation

Please cite the associated research article when using or referring to these supplementary materials.

**Manuscript title:** Does More Enthusiasm from Language Teachers Always Help? Functional Form and Cross-Country Variation in Reading Achievement in PISA 2018.

**Journal:** Sage Open.

## Contact

For questions concerning the analysis code or supplementary materials, please contact the corresponding author.
