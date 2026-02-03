# Automated EDA Report — unseen_inference_dataset

## Dataset Overview

- Rows: **1599**
- Columns: **12**
- Duplicates: **240**


### Inferred Types (first 15)

- fixed acidity: float64

- volatile acidity: float64

- citric acid: float64

- residual sugar: float64

- chlorides: float64

- free sulfur dioxide: float64

- total sulfur dioxide: float64

- density: float64

- pH: float64

- sulphates: float64

- alcohol: float64

- quality: int64


### Missing Value Summary (Top 10)

| column               |   missing_count |   missing_pct |
|:---------------------|----------------:|--------------:|
| fixed acidity        |               0 |             0 |
| volatile acidity     |               0 |             0 |
| citric acid          |               0 |             0 |
| residual sugar       |               0 |             0 |
| chlorides            |               0 |             0 |
| free sulfur dioxide  |               0 |             0 |
| total sulfur dioxide |               0 |             0 |
| density              |               0 |             0 |
| pH                   |               0 |             0 |
| sulphates            |               0 |             0 |

## Basic Data Quality Checks

- Columns with one value: []

- High-missing columns (>40%): []


## Descriptive Statistics

No categorical columns detected.


### Numeric (Top rows)

| column               |     min |       max |       mean |   median |    mode |         std |       iqr |   outlier_low |   outlier_high |   outlier_pct |   n_nonnull |
|:---------------------|--------:|----------:|-----------:|---------:|--------:|------------:|----------:|--------------:|---------------:|--------------:|------------:|
| fixed acidity        | 4.6     |  15.9     |  8.31964   |  7.9     |  7.2    |  1.7411     |  2.1      |      3.95     |       12.35    |          3.06 |        1599 |
| volatile acidity     | 0.12    |   1.58    |  0.527821  |  0.52    |  0.6    |  0.17906    |  0.25     |      0.015    |        1.015   |          1.19 |        1599 |
| citric acid          | 0       |   1       |  0.270976  |  0.26    |  0      |  0.194801   |  0.33     |     -0.405    |        0.915   |          0.06 |        1599 |
| residual sugar       | 0.9     |  15.5     |  2.53881   |  2.2     |  2      |  1.40993    |  0.7      |      0.85     |        3.65    |          9.69 |        1599 |
| chlorides            | 0.012   |   0.611   |  0.0874665 |  0.079   |  0.08   |  0.0470653  |  0.02     |      0.04     |        0.12    |          7    |        1599 |
| free sulfur dioxide  | 1       |  72       | 15.8749    | 14       |  6      | 10.4602     | 14        |    -14        |       42       |          1.88 |        1599 |
| total sulfur dioxide | 6       | 289       | 46.4678    | 38       | 28      | 32.8953     | 40        |    -38        |      122       |          3.44 |        1599 |
| density              | 0.99007 |   1.00369 |  0.996747  |  0.99675 |  0.9972 |  0.00188733 |  0.002235 |      0.992248 |        1.00119 |          2.81 |        1599 |
| pH                   | 2.74    |   4.01    |  3.31111   |  3.31    |  3.3    |  0.154386   |  0.19     |      2.925    |        3.685   |          2.19 |        1599 |
| sulphates            | 0.33    |   2       |  0.658149  |  0.62    |  0.6    |  0.169507   |  0.18     |      0.28     |        1       |          3.69 |        1599 |

## Visualizations (saved files)

- output/unseen_inference_dataset/plots/hist_fixed acidity.png

- output/unseen_inference_dataset/plots/box_volatile acidity.png

- output/unseen_inference_dataset/plots/scatter_fixed acidity_vs_volatile acidity.png

- output/unseen_inference_dataset/plots/corr_heatmap.png

- output/unseen_inference_dataset/plots/missingness_top.png


## Insights + Limitations (Gemini)

**1) Data Insights**

*   The dataset consists of 1599 total rows and 12 columns, which were all inferred as `float64` or `int64` types.
*   The data appears complete, as all listed columns (including "fixed acidity," "volatile acidity," and "pH") show 0 missing values.
*   A significant number of exact duplicate entries are present, totaling 240 rows.
*   The "residual sugar" column exhibits the highest percentage of identified outliers, affecting 9.69% of the values.
*   The "citric acid" content spans from a minimum of 0.0 up to 1.0, and the most frequent value (mode) is 0.0.
*   "Total sulfur dioxide" shows a large variation, ranging up to a maximum of 289.0, with a standard deviation of 32.895...
*   The "density" column is extremely consistent, ranging narrowly between 0.99007 and 1.00369, corresponding to a very low standard deviation of 0.00188...
*   "Chlorides" shows a significant outlier presence, with 7.0% of the data points falling outside the defined inner fences.

**2) Limitations/Bias Note**

The presence of 240 duplicate rows suggests potential sampling redundancy, which could artificially bias statistical summaries and model training if the duplicates are not handled.