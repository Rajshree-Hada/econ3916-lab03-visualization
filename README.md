# econ3916-lab03-visualization
Lab 03 submission

# Honest vs. Misleading Visualizations

## Objective
Demonstrate, using economic data, how chart design choices (axis truncation, time window, scale, and price basis) can change the story a dataset appears to tell, and how to test and correct for them.

## Methodology
- Recreated Anscombe's Quartet to show that four datasets with identical means, variances, and correlation can have very different underlying shapes.
- Computed a Lie Factor of [YOUR VALUE] for a truncated-axis revenue chart, then redesigned it with a zero-based axis.
- Deflated FRED average hourly earnings (AHETPI) to 2020 dollars using CPI, and plotted four versions of the same series: full-range zero-based, truncated y-axis, cherry-picked window, and log scale.
- Ran a four-step exploratory data analysis (structure, distributions, relationships, anomalies) on World Bank GDP data covering [YOUR VALUE] countries and [YOUR VALUE] years.
- Applied a log transform to correct GDP's right skew, and assessed missingness patterns (MCAR, MAR, MNAR) using a missing-data heatmap.
- Built an interactive dashboard (ipywidgets and matplotlib) with controls for nominal versus real series, y-axis floor, time window, and linear versus log scale, with a live Lie Factor readout.

## Key Findings
- Summary statistics alone can conceal structure. Plotting the data before modeling is necessary to detect nonlinearity, outliers, and influential points.
- Raising the y-axis floor inflates the Lie Factor. The truncated revenue chart scored [YOUR VALUE], against an ideal of about 1.
- The same real-wage series supports very different narratives depending on axis floor, time window, and scale. Cherry-picking the window and truncating the axis both distort the picture without changing the underlying data.
- Nominal and real series diverge because of inflation. Real earnings are the appropriate basis for comparing decades.
- GDP is heavily right-skewed across countries. A log transform makes its distribution and its decade-over-decade shift readable.
- Missing GDP values cluster at the start and end of the period, consistent with missingness that depends on year (MAR) rather than at-random gaps. A few isolated mid-period gaps may be MNAR.
