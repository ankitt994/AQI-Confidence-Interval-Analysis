# AQI Confidence Interval Analysis

## Project Overview

This project analyzes Air Quality Index (AQI) data for six states where RRE operates: California, Florida, Michigan, Ohio, Pennsylvania, and Texas. The analysis compares average AQI across these states, visualizes the distribution with a Seaborn boxplot, and calculates a 95% confidence interval for the state with the highest mean AQI.

## Objectives

- Compare mean AQI across the six RRE states.
- Visualize state-level AQI distributions with a boxplot.
- Identify which state may be most affected by a policy focused on higher AQI.
- Estimate a 95% confidence interval for the highest-mean-AQI state.

## Key Findings

Mean AQI by state, sorted from highest to lowest:

| State | Mean AQI |
|---|---:|
| California | 13.12 |
| Michigan | 9.11 |
| Florida | 6.50 |
| Ohio | 4.33 |
| Pennsylvania | 3.90 |
| Texas | 3.70 |

California has the highest mean AQI in this analysis.

### California: 95% Confidence Interval

- Sample size: 66 observations
- Sample mean AQI: 13.12
- Sample standard deviation: approximately 7.30
- Standard error: approximately 0.90
- Margin of error: approximately 1.79
- 95% t-confidence interval: **11.33 to 14.92**

Interpretation: Based on this sample and the t-interval method, the estimated interval for California's population mean AQI is approximately 11.33–14.92.

## Tools and Libraries

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy (for statistical calculations, if used in the notebook)

## Repository Contents

- `README.md` — project overview, methods, and findings.
- `requirements.txt` — Python package dependencies.
- `RRE_AQI_Analysis.html` — exported notebook/report, to be added.
- `c4_epa_air_quality.csv` — source dataset, to be added.
- `RRE_AQI_Analysis.ipynb` — editable Jupyter notebook, to be added later.

## How to Run

1. Clone or download this repository.
2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `RRE_AQI_Analysis.ipynb` in Jupyter Notebook or JupyterLab after the notebook is added.
4. Ensure the CSV dataset is in the expected project folder before running the analysis.

## Notes and Limitations

- The findings describe the dataset and analysis performed; they do not establish that a policy caused a change in AQI.
- The policy implication is a data-based interpretation, not a causal estimate.
- The confidence interval is an estimate based on the available California sample and the t-distribution method.
