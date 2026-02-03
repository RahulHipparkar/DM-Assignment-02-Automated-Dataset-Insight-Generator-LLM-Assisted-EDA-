# Automated EDA Report — dev_training_dataset

## Dataset Overview

- Rows: **244**
- Columns: **7**
- Duplicates: **1**


### Inferred Types (first 15)

- total_bill: float64

- tip: float64

- sex: category

- smoker: category

- day: category

- time: category

- size: int64


### Missing Value Summary (Top 10)

| column     |   missing_count |   missing_pct |
|:-----------|----------------:|--------------:|
| total_bill |               0 |             0 |
| tip        |               0 |             0 |
| sex        |               0 |             0 |
| smoker     |               0 |             0 |
| day        |               0 |             0 |
| time       |               0 |             0 |
| size       |               0 |             0 |

## Basic Data Quality Checks

- Columns with one value: []

- High-missing columns (>40%): []


## Descriptive Statistics

### Categorical: `day` (Top values)

| day   |   count |   pct |
|:------|--------:|------:|
| Sat   |      87 | 35.66 |
| Sun   |      76 | 31.15 |
| Thur  |      62 | 25.41 |
| Fri   |      19 |  7.79 |

### Numeric (Top rows)

| column     |   min |   max |     mean |   median |   mode |     std |     iqr |   outlier_low |   outlier_high |   outlier_pct |   n_nonnull |
|:-----------|------:|------:|---------:|---------:|-------:|--------:|--------:|--------------:|---------------:|--------------:|------------:|
| total_bill |  3.07 | 50.81 | 19.7859  |   17.795 |  13.42 | 8.90241 | 10.78   |      -2.8225  |       40.2975  |          3.69 |         244 |
| tip        |  1    | 10    |  2.99828 |    2.9   |   2    | 1.38364 |  1.5625 |      -0.34375 |        5.90625 |          3.69 |         244 |
| size       |  1    |  6    |  2.56967 |    2     |   2    | 0.9511  |  1      |       0.5     |        4.5     |          3.69 |         244 |

## Visualizations (saved files)

- output/dev_training_dataset/plots/hist_total_bill.png

- output/dev_training_dataset/plots/box_tip.png

- output/dev_training_dataset/plots/bar_sex.png

- output/dev_training_dataset/plots/scatter_total_bill_vs_tip.png

- output/dev_training_dataset/plots/corr_heatmap.png


## Insights + Limitations (Gemini)

### EDA Insights

1.  The dataset is moderately sized, containing 244 rows and 7 columns.
2.  Data quality is high, as all 7 listed columns (e.g., 'total_bill', 'tip', 'sex', 'day') show a 0.0% missing percentage.
3.  Saturday ("Sat") is the busiest day in the observed sample, accounting for 87 counts, which represents 35.66% of the total observations.
4.  Friday ("Fri") is the least represented day, with only 19 recorded observations (7.79%).
5.  The minimum 'total_bill' observed is $3.07, while the maximum observed 'total_bill' is $50.81.
6.  The mean 'total_bill' ($19.785...) is slightly higher than the median 'total_bill' ($17.795).
7.  'tip' amounts range from a minimum of $1.0 to a maximum of $10.0, with the most frequent tip amount (mode) being $2.0.
8.  The most common group 'size' (median and mode) is 2.0, though party sizes range up to a maximum of 6.0.
9.  A small percentage (3.69%) of the values for 'total_bill', 'tip', and 'size' are flagged as high outliers by the IQR method.

---
### Limitations/Bias Note

The sample coverage is highly skewed toward weekend activity, as Saturday (87 counts) and Sunday (76 counts) dominate the data. This bias may limit generalizations about overall weekly dining habits. Additionally, there is 1 duplicate row recorded among the 244 total observations.