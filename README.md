# Educational-Returns-in-a-Malaysian-University

Analysis code for the study **"Towards Career Success: Perceived Educational Returns and Career Satisfaction Among University Students in Malaysia"**.

The study examines how three perceived educational returns (employability confidence, perceived skill relevance and income expectations) relate to career satisfaction among university students in Malaysia, and whether employability confidence mediates these relationships.

## Sample

- Online questionnaire (Google Forms), 20 five-point Likert items: five each for employability confidence (EMP1–EMP5), skill relevance (SR1–SR5), income expectations (IE1–IE5) and career satisfaction (CS1–CS5).
- Analysed sample: **N = 380** university students. Respondents aged below 18 are excluded in the first data step of the notebook, before any result is computed or printed.

## Data availability

The survey dataset is **not publicly available**. It can be requested from the corresponding author for reasonable research purposes. The notebook expects the file `edu_return_data.xlsx` in the same folder as the notebook.

## Contents

| File                             | Description                                                                                               |
| -------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `edu_return_analysis_N380.ipynb` | Full analysis, with outputs, for N = 380                                                                  |
| `analysis_results.xlsx`          | Exported results: descriptives, correlations, regression, SEM fit and paths                               |
| `mediation_results.xlsx`         | Exported mediation results: regression paths and bootstrap indirect effects                               |
| `figure2_expectation_gap.png`    | Distribution of the income expectation–career satisfaction gap (scores rescaled with the 1–5 scale range) |

## Analyses in the notebook

1. Data screening (missing values, outliers)
2. Descriptive statistics and demographics
3. Reliability (Cronbach's α)
4. Exploratory factor analysis (Bartlett's test, KMO, four-factor oblimin solution)
5. Pearson correlations
6. Multiple regression with collinearity diagnostics (VIF)
7. Covariance-based structural equation model (semopy), with SRMR
8. Career satisfaction by education level (ANOVA)
9. Income expectation–career satisfaction gap score: both scores rescaled to 0–1 with the theoretical range of the five-point scale, (x − 1)/4, then differenced
10. Robustness checks (outlier sensitivity, bootstrap confidence intervals, Spearman correlations, HC3 standard errors)
11. Mediation through employability confidence (regression-based, equivalent to PROCESS Model 4; 5,000 bootstrap resamples, seed 42)

## Requirements

Python 3.11 with:

```
pandas 2.3.3
numpy 2.0.2
scipy 1.13.1
statsmodels 0.14.6
scikit-learn 1.6.1
semopy 2.3.11
pingouin 0.5.5
factor_analyzer 0.5.1
matplotlib 3.9.4
seaborn 0.13.2
missingno
openpyxl 3.1.5
```

## How to run

1. Place `edu_return_data.xlsx` (obtained on request) in this folder.
2. Open `edu_return_analysis_N380.ipynb` in Jupyter and run all cells.

## Citation

[To be added after publication.]

## License

MIT
