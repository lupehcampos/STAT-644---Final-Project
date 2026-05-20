# An Investigation of Sleep Duration and Depression Among University Students: A Gender-Stratified Analysis

This repository contains the statistical analysis and research documentation for investigating the association between sleep duration and depression, with gender as a stratifying variable. This project utilizes categorical data analysis techniques, specifically the Cochran-Mantel-Haenszel (CMH) test and logistic regression, to assess effect modification.

## Project Overview
* **Research Question**: Is there a conditional association between sleep duration and depression, and does gender modify this relationship?
* **Data Source**: Student Depression Dataset (Kaggle).
* **Institution**: Air Force Institute of Technology (AFIT), Department of Math and Statistics.

## Methodology
The study employs a two-part statistical framework:
1. **CMH Test**: Used to evaluate the conditional association between sleep and depression, controlling for gender.
2. **Logistic Regression**: Used to estimate odds ratios and evaluate effect modification via interaction terms $(\beta_5, \beta_6, \beta_7)$.

### Statistical Model
The log-odds of depression ($Y_r$) are modeled as:
$$\log\left(\frac{P(Y_r=1)}{1-P(Y_r=1)}\right) = \beta_0 + \beta_1 S_{1r} + \beta_2 S_{2r} + \beta_3 S_{3r} + \beta_4 G_r + \beta_5(S_{1r} \cdot G_r) + \beta_6(S_{2r} \cdot G_r) + \beta_7(S_{3r} \cdot G_r)$$
*Where $S_{jr}$ represents sleep duration indicator variables and $G_r$ is the gender indicator.*

## Repository Structure
```text
├── data/              # Source datasets (raw and processed)
├── scripts/           # R/Python code for statistical modeling
├── tex/               # LaTeX source files for the report
├── figures/           # Visualizations and diagnostic plots
└── README.md          # Project documentation
