# Soybean Agricultural Dataset Analysis Report

## Dataset Overview
The analysis utilizes the Advanced Soybean Agricultural Dataset, containing various attributes related to soybean agriculture. The dataset includes both numerical and categorical features relevant to agricultural production, environmental conditions, and soybean characteristics.

---

## Data Cleaning Procedures

### Missing Values
- Checked for missing values using `df.info()`.
- Identified columns with missing data.
- **Numerical Columns:** Filled missing values with median values.
- **Categorical Columns:** Filled missing values with mode (most frequent category).

### Duplicate Records
- Checked and removed duplicate entries to ensure data integrity.

### Categorical Standardization
- Ensured consistency in categorical variables by standardizing text formats (e.g., title case).

### Outlier Detection and Treatment
- Applied Z-score method (values beyond ±3 standard deviations identified as outliers).
- Utilized Interquartile Range (IQR) method to detect extreme values.
- Employed capping technique to limit outlier impact without deleting observations.

---

## Exploratory Data Analysis

### Univariate Analysis

**Numerical Variables:**
- Histograms revealed distribution shapes, skewness, and kurtosis of numeric variables.
- Boxplots identified outliers clearly.
- Variables examined include yield, moisture content, plant height, seed weight, and soil nutrients.

**Categorical Variables:**
- Frequency distributions visualized through bar charts.
- Identified dominant categories and imbalances in categorical features such as soybean variety, soil type, and farming method.

---

### Bivariate Analysis

**Correlation Analysis:**
- Correlation heatmap identified strong positive or negative relationships.
  - Yield positively correlated with soil nutrient levels.
  - Yield negatively correlated with moisture extremes.
- Scatter plots visualized pairwise relationships clearly.

**Categorical vs. Numerical:**
- Boxplots and violin plots created for categorical variables against numerical target variables.
- ANOVA tests confirmed significant differences in yield across different soybean varieties and farming methods.

---

### Multivariate Analysis

**Principal Component Analysis (PCA):**
- PCA applied to reduce dimensionality and identify major patterns.
- First two principal components explained significant variance.
  - Component loadings showed high contributions from environmental conditions and soil nutrients.
- Pairplots visualized multivariate relationships clearly.

---

## Key Findings and Inferences

### Yield Influencing Factors
- Soil nutrient levels strongly influence soybean yield.
- Optimal moisture content significantly enhances productivity; extremes negatively impact yields.

### Variety and Farming Method Impact
- Soybean variety significantly affects yield outcomes (confirmed by ANOVA).
- Different farming methods cluster distinctly in PCA space; indicating clear differences in productivity based on farming practices.

### Environmental Conditions
- Environmental factors such as rainfall patterns, temperature, and humidity significantly correlate with yield variations.
- Geographic location influences agricultural outcomes due to varying environmental conditions.

### Statistical Distributions
- Yield distribution is positively skewed; log transformations may normalize the distribution for modeling purposes.
- Several numeric features exhibit non-normal distributions requiring transformations for certain analyses.

---

### Dimensional Analysis
- PCA demonstrates environmental and soil-related features explain the majority of variance.
- Multivariate analysis provides deeper insights compared to univariate methods alone.
