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
- Explain confidence intervals through a visual, beginner-friendly infographic.

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

## Confidence Interval Infographic

The repository includes a three-page PDF carousel that explains confidence intervals visually, including the core idea, interpretation, and key statistical concepts.

[**View the three-page Confidence Interval Infographic (PDF)**](confidence_intervals_carousel.pdf)

## Dataset Note and Limitations

The notebook's dataset uses the columns `date_local` and `aqi_log`. The AQI values are reconstructed from the log-transformed column using `numpy.exp()`.

The supplied CSV contains observations for **January 1, 2018 only**, rather than a time series across multiple dates. Therefore, the results should be treated as a learning exercise based on the available sample, not as evidence of long-term air quality trends or a causal policy impact. Confirm that the dataset is the intended source and rerun the notebook before relying on the reported findings.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook

## Repository Contents

| File | Purpose |
|---|---|
| `README.md` | Project overview, findings, setup instructions, and limitations |
| `RRE_AQI_Analysis.ipynb` | Jupyter Notebook containing the analysis, visualizations, and confidence interval calculation |
| `RRE_AQI_Analysis.html` | HTML export of the notebook for easy viewing in a browser |
| `c4_epa_air_quality.csv` | Source dataset used by the notebook |
| `requirements.txt` | Python package dependencies |
| `confidence_intervals_carousel.pdf` | Three-page visual infographic explaining confidence intervals |

## How to Run the Project

1. Clone or download this repository.
2. Ensure `c4_epa_air_quality.csv` is in the same folder as the notebook.
3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Open `RRE_AQI_Analysis.ipynb` in Jupyter Notebook or JupyterLab.
5. Load the dataset using a relative path:

   ```python
   aqi = pd.read_csv("c4_epa_air_quality.csv")
   ```

6. Run the notebook cells from top to bottom to reproduce the analysis.

## References

- [Seaborn boxplot documentation](https://seaborn.pydata.org/generated/seaborn.boxplot.html)
- [Pandas documentation](https://pandas.pydata.org/docs/)
- [SciPy statistics documentation](https://docs.scipy.org/doc/scipy/reference/stats.html)

---

This is a learning project demonstrating practical use of Python and statistical reasoning. Interpret the results in light of the dataset's coverage and assumptions.
