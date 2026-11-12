# Climate Statistics Analysis

Descriptive statistics and statistical inference on daily temperature, surface solar radiation and total precipitation for ten grid cells of a region in Spain (2014–2025), written in Python with Jupyter notebooks.

## What is inside

| File | Content |
|---|---|
| `code/descriptive_statistics.ipynb` | Project 1: descriptive statistics |
| `code/inference.ipynb` | Project 2: statistical inference |
| `docs/report_descriptive_statistics.pdf` | Report for project 1 (in Spanish) |
| `docs/report_inference.pdf` | Report for project 2 (in Spanish) |

## Project 1 – Descriptive statistics

- **Distributions** of temperature, radiation and precipitation, and how they change with weekday, month and year (coefficient of variation to compare variables).
- **Relationships** between the ten cells and between the three variables: scatter plots and correlation matrices.
- **Monthly and yearly profiles:** mean vs. median profile and evolution of the deciles (p10–p90).
- **Two groups of cells** chosen from the correlation analysis, comparing the mean and variance of temperature in each group over time.

## Project 2 – Statistical inference

- **Hypothesis tests** on the mean summer temperature of cell 01 against a claimed 30 °C, with two alternative hypotheses.
- **Distribution fitting:** Kolmogorov–Smirnov tests, QQ-plots, kernel density estimates and maximum-likelihood fits for radiation, temperature and precipitation.
- **Bootstrap confidence intervals** for the quarterly means of the three variables.
- **Monte Carlo simulation** of temperatures using the fitted distributions, compared with the real data.

## Run it

Requires Python 3.10 or newer.

```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn jupyter
jupyter notebook
```

The notebooks read three CSV files from the same folder as the notebook:
`G01A_2m_temperature.csv`, `G01A_surface_solar_radiation_downwards.csv` and `G01A_total_precipitation.csv`.
The datasets were provided by the course and are **not included** in this repository.
Each file has one row per day, columns for the ten cells (`TEMP_CELDA01`…`TEMP_CELDA10`, and the same for `IRRAD_` and `PRECIP_`) and the calendar columns `FECHA`, `DIASEM`, `DIA`, `MES`, `ANNO`.
