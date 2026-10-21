# AQI Confidence Interval Analysis

## Project Overview

This project applies descriptive statistics and confidence intervals to Air Quality Index (AQI) data for six states where Ripple Renewable Energy (RRE) operates: California, Florida, Michigan, Ohio, Pennsylvania, and Texas.

The notebook compares state-level mean AQI, visualizes AQI distributions with a Seaborn boxplot, considers a proposed policy threshold of AQI 10, and estimates a 95% confidence interval for the state with the highest mean AQI.

## Project Objectives

- Explore and check the AQI dataset.
- Calculate and compare mean AQI across the six RRE states.
- Visualize the state-level distributions with a boxplot.
- Identify which state appears most likely to meet or exceed the policy threshold based on the sample.
- Calculate and interpret a 95% confidence interval for the highest-mean-AQI state.

## Key Findings

The current notebook reports the following mean AQI values, sorted from highest to lowest:

| State | Mean AQI |
|---|---:|
| California | 13.12 |
| Michigan | 9.11 |
| Florida | 6.50 |
| Ohio | 4.33 |
| Pennsylvania | 3.90 |
| Texas | 3.70 |

California has the highest reported mean AQI among the six states. Its reported mean is above the policy threshold of 10.

### California: 95% Confidence Interval

The current notebook reports these results for California:

- Sample size: 66 observations
- Sample mean AQI: 13.12
- Sample standard deviation: approximately 7.30
- Standard error: approximately 0.90
- Margin of error: approximately 1.79
- 95% t-confidence interval: **11.33 to 14.92**

**Interpretation:** Under the assumptions of the sampling method, this interval provides a range of plausible values for California's population mean AQI. A confidence interval describes uncertainty around an estimate; it does not show that a policy caused an outcome.

## Dataset Note and Limitations

The notebook's dataset uses the columns `date_local` and `aqi_log`. The AQI values are reconstructed from the log-transformed column using `numpy.exp()`.

The currently supplied CSV contains observations for **January 1, 2018 only**, rather than a time series across multiple dates. Therefore, the results should be treated as a learning exercise based on the available sample, not as evidence of long-term air quality trends or a causal policy impact. Confirm that the dataset is the intended source and rerun the notebook before relying on the reported findings.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook

## Repository Contents

| File | Purpose | Status |
|---|---|---|
| `RRE_AQI_Analysis.ipynb` | Main notebook containing the analysis, visualizations, and confidence interval calculation | Already in the repository |
| `requirements.txt` | Python libraries needed to run the notebook | Already in the repository |
| `README.md` | Project overview, findings, setup instructions, and limitations | This file |
| `c4_epa_air_quality.csv` | Source dataset required to rerun the notebook | **Needs to be added** |
| `RRE_AQI_Analysis.html` | Optional HTML export of the notebook for easy viewing in a browser | Optional |
| `confidence_interval_one_page_guide.pdf` | Optional one-page visual guide to confidence intervals | Optional |

## How to Run the Project

1. Download or clone this repository.
2. Add `c4_epa_air_quality.csv` to the project folder, alongside the notebook.
3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Open `RRE_AQI_Analysis.ipynb` in Jupyter Notebook or JupyterLab.
5. Make sure the notebook loads the CSV using a relative path, for example:

   ```python
   aqi = pd.read_csv("c4_epa_air_quality.csv")
   ```

6. Run the notebook cells from top to bottom to regenerate the results.

## References

- [Seaborn boxplot documentation](https://seaborn.pydata.org/generated/seaborn.boxplot.html)
- [Pandas documentation](https://pandas.pydata.org/docs/)
- [SciPy statistics documentation](https://docs.scipy.org/doc/scipy/reference/stats.html)

---

This is a learning project demonstrating practical use of Python and statistical reasoning. Interpret the results in light of the dataset's coverage and assumptions.
