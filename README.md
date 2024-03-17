# Python-AB_Testing-Hyperisland

---

## A/B Testing Explanation

## Introduction

A/B testing, also known as split testing, is a method used to compare two versions of a product or service to determine which one performs better. It is widely used in various fields, including marketing, web development, and user experience design, to make data-driven decisions and optimize outcomes.

## The Case

**Note**: The following case is fictive, and the data and visuals are borrowed from [GoodUI](https://goodui.org/patterns/126/tests/411/).

**Variant A (baseline)**

![Variant A](https://github.com/barisyukselcoding/Python-AB_Testing-Hyperisland/assets/135212402/19f80412-7584-43e7-a1ca-97276c390dba)

**Variant B**

![Variant B](https://github.com/barisyukselcoding/Python-AB_Testing-Hyperisland/assets/135212402/3c13b7db-907e-4b3a-9a3e-d4a1cca138ca)

## Dependencies

A/B testing has the following dependencies:

- **Pandas** (`import pandas as pd`): Used for data manipulation and analysis, including reading and handling structured data.
- **Seaborn** (`import seaborn as sns`): Used for data visualization, particularly for creating statistical graphics like histograms.
- **Matplotlib** (`import matplotlib.pyplot as plt`): Used for creating various types of plots, including histograms, scatter plots, and line plots.
- **Scipy** (`from scipy import stats`, `from scipy.stats import ttest_ind, anderson`): Used for statistical analysis, including hypothesis testing (t-tests), normality tests (Shapiro-Wilk, Anderson-Darling), and calculating statistical measures.

## Code Overview

The provided Python script performs an A/B testing analysis on a dataset containing user metrics for two variants, A and B. It includes steps for data loading, visualization, normality assessment, and statistical testing.

## Explanation of Steps

1. **Importing Libraries**: The script imports necessary libraries such as pandas for data manipulation, seaborn and matplotlib for visualization, and scipy for statistical testing.
   
2. **Loading Data**: Data is loaded from a CSV file named "user-data.csv" using pandas' `read_csv()` function.
   
3. **Data Exploration**: The first few rows of the dataset are displayed to understand its structure. The data is then separated into two groups based on the "Variant" column.
   
4. **Visualization**: Histograms are plotted to visualize the distributions of metrics between variant A and variant B.
   
5. **Normality Assessment**: Normality of metric distributions is assessed using skewness, kurtosis, and statistical tests such as Shapiro-Wilk and Anderson-Darling tests.
   
6. **Statistical Testing**: A two-sample t-test is performed to compare means between variant A and variant B for each metric.

## Interpretation of Results

- **Normality Assessment**: Skewness and kurtosis are used to assess the shape of distributions, while Shapiro-Wilk and Anderson-Darling tests are employed to evaluate normality statistically.
  
- **Statistical Testing**: The t-test results provide insights into whether there are significant differences between variant A and variant B for each metric.

## Findings and Conclusion

## Context

### Evaluation of Vertical vs. Horizontal Media Rail

We're conducting an A/B test to assess the efficacy of a vertical media rail compared to a horizontal one on a cooking equipment website's product page. The primary metric selected for this analysis is Clicks on media, with Time on Page (sec) serving as the secondary metric among the available data points.

### Justification for Primary and Secondary Metrics in A/B Test

**Primary Metric: Clicks on media**

- **Engagement Measurement:** Clicks directly gauge user interaction with the media rail, indicating higher engagement with the vertical format if the clicks increase.
- **Sales Potential:** While clicks do not directly translate to sales, they signify user interest in the media content, potentially leading to further exploration of product details and eventual purchase consideration.

**Secondary Metric: Time on Page (sec)**

- **Engagement Signal:** Time spent on the page reflects overall user interest beyond initial interaction with the media, providing insight into user engagement with the content.
- **Complement to Clicks on Media:** Time on page complements clicks on media by indicating how long users remain engaged with the content after interacting. Analyzing both metrics offers a comprehensive understanding, identifying scenarios where users might quickly leave the page despite initial engagement.

### Why not GMV or Page Views?

**GMV (in $):** GMV serves as a valuable long-term metric but may not be suitable for observing short-term design differences. External factors can influence sales, making it less indicative of the immediate impact of design changes.

**Page Views:** This metric reflects overall traffic to the page, unaffected by the media rail orientation. It does not directly measure interaction with the media rail itself. Prioritizing user engagement metrics allows for insights into whether the vertical media format effectively captures user attention and drives further product exploration. Subsequent long-term A/B tests can assess the translation of engagement into increased sales.

### Normality Assumption Check

Many statistical tests assume normally distributed datasets. In the following section, we'll demonstrate common methods for checking this assumption in Python.

**Results**: Insert the results obtained from the statistical tests, such as t-test statistics, p-values, means, and standard deviations, for each metric.

**Explanations**: Provide explanations for why specific tests were chosen, considering factors like assumptions, sample size, and distribution characteristics.

**Plot Interpretation**: Discuss insights gleaned from the histograms, such as differences in metric distributions between variants.

**Conclusion**: Summarize the findings and their implications, considering factors like statistical significance, practical significance, and potential actions based on the results.
