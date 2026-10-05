# Customer Segmentation and Prediction

An end-to-end statistical analysis and machine learning project on a dataset of 1,500 retail customers, covering exploratory data analysis, hypothesis testing, predictive modeling, and customer segmentation.

## Dataset

The dataset includes 1,500 customers with the following features:
`Customer_ID`, `Age`, `Gender`, `Annual_Income`, `Purchase_Amount`, `Purchase_Frequency`, `Customer_Rating`

## Methodology

**1. Data Cleaning & Outlier Detection**
- Checked for missing values and duplicates
- Detected outliers in `Annual_Income` and `Purchase_Amount` using both IQR and Z-score methods
- Evaluated skewness and kurtosis for all numeric variables

**2. Exploratory Data Analysis**
- Grouped customers by age brackets and compared purchasing behavior
- Built a correlation matrix to identify relationships between variables

**3. Hypothesis Testing**
- Compared purchase amounts between genders (Mann-Whitney U test)
- Compared customer ratings across income groups (Kruskal-Wallis test)
- Tested independence between gender and income group (Chi-square test)
- Computed effect sizes (rank-biserial correlation, epsilon-squared) and bootstrap confidence intervals

**4. Predictive Modeling**
- Linear Regression and Random Forest to predict `Purchase_Amount`
- Logistic Regression to classify customer satisfaction (`Customer_Rating` ≥ 4), evaluated with confusion matrix, precision, recall, and ROC-AUC

**5. Customer Segmentation**
- K-Means clustering (optimal k selected via the Elbow Method) to group customers into behavioral segments

## Key Findings

- No statistically significant relationship was found between gender, income group, and purchase behavior or satisfaction — effect sizes were consistently negligible.
- `Annual_Income` and `Purchase_Frequency` were the strongest predictors of `Purchase_Amount` (R² ≈ 0.72 with Linear Regression).
- None of the available features could reliably predict customer satisfaction, suggesting satisfaction depends on factors not captured in this dataset.
- K-Means identified 4 customer segments, including a high-income, high-spending group with only moderate satisfaction — a potential target for improved customer service.

## Tools & Libraries

Python, pandas, numpy, matplotlib, seaborn, scipy, scikit-learn

## Note

The dataset used in this project is synthetically generated for practice purposes.
