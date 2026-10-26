# Educational-Returns-in-a-Malaysian-University

Analysis code for the study **"Towards Career Success: Perceived Educational Returns and Career Satisfaction Among University Students in Malaysia"**.

The study examines how three perceived educational returns (employability confidence, perceived skill relevance and income expectations) relate to career satisfaction among university students in Malaysia, and whether employability confidence mediates these relationships.

## Sample

- Online questionnaire (Google Forms), 20 five-point Likert items: five each for employability confidence (EMP1–EMP5), skill relevance (SR1–SR5), income expectations (IE1–IE5) and career satisfaction (CS1–CS5).
- Responses received up to 15 July 2026 (the cut-off for the conference extended abstract) are analysed; later responses are not part of this study.
- Analysed sample: **N = 380** university students. Respondents aged below 18 are excluded in the first data step of the notebook, before any result is computed or printed.

## Data availability

The survey dataset is **not publicly available**. It can be requested from the corresponding author for reasonable research purposes. The notebook reads the Google Forms export `Towards Career success (Responses) (1).xlsx` from the same folder as the notebook and encodes it there: the answer labels (e.g. "Agree (4)") are converted to their 1–5 codes, and responses after the cut-off and respondents aged below 18 are removed.

## Contents

| File                             | Description                                                                                               |
| -------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `edu_return_analysis_N380.ipynb` | Full analysis, with outputs, for N = 380                                                                  |
| `analysis_results.xlsx`          | Exported results: descriptives, correlations, regression, SEM fit and paths                               |
| `mediation_results.xlsx`         | Exported mediation results: regression paths and bootstrap indirect effects                               |
| `figure2_expectation_gap.png`    | Distribution of the income expectation–career satisfaction gap (scores rescaled with the 1–5 scale range) |
| `requirements.txt`               | Package versions used to run the notebook                                                                 |

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

**Python 3.11 or newer** (the pinned numpy, scipy and scikit-learn versions do not install on older Python). The notebook was run with Python 3.11.2 and the versions in `requirements.txt`:

```
pandas==2.3.0
numpy==2.4.6
scipy==1.17.1
statsmodels==0.14.6
scikit-learn==1.8.0
semopy==2.3.11
pingouin==0.7.0
factor_analyzer==0.5.1
matplotlib==3.10.3
seaborn==0.13.2
missingno==0.5.2
openpyxl==3.1.5
```

## How to run

1. Place `Towards Career success (Responses) (1).xlsx` (obtained on request) in this folder.
2. Open `edu_return_analysis_N380.ipynb` in Jupyter with a Python 3.11+ kernel.
3. Run the first cell, which installs the packages above (or run `pip install -r requirements.txt` beforehand), then restart the kernel.
4. Run all cells.

## Citation

[To be added after publication.]

## License

MIT
