# Statistical Hypothesis Testing Using Python

## 📌 Project Overview

This project demonstrates statistical hypothesis testing using the real-world Iris dataset. The objective is to determine whether there is a statistically significant difference in the average sepal length of Iris Setosa and Iris Versicolor flowers.

The project includes exploratory data analysis, assumption validation, hypothesis testing, p-value interpretation, confidence interval estimation, and practical significance analysis.

## 🎯 Objectives

- Understand and implement statistical hypothesis testing.
- Formulate clear null and alternative hypotheses.
- Select an appropriate statistical test.
- Validate statistical test assumptions.
- Calculate the test statistic and p-value.
- Understand statistical versus practical significance.
- Present findings through visualizations and a detailed report.

## 📂 Dataset

- **Dataset:** Iris Dataset
- **Source:** UCI Machine Learning Repository
- **Total records:** 150
- **Records used for analysis:** 100
- **Groups:** Iris Setosa and Iris Versicolor
- **Target measurement:** Sepal length (cm)

Dataset link: https://archive.ics.uci.edu/dataset/53/iris

## ❓ Research Question

Is there a statistically significant difference in the average sepal length between Iris Setosa and Iris Versicolor flowers?

## 📝 Hypothesis Formulation

### Null Hypothesis (H₀)

There is no difference in the population mean sepal length between Iris Setosa and Iris Versicolor flowers.

### Alternative Hypothesis (H₁)

There is a difference in the population mean sepal length between Iris Setosa and Iris Versicolor flowers.

**Significance Level:** α = 0.05

**Test Type:** Two-tailed hypothesis test.

## 🛠️ Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Scikit-learn

## ⚙️ Project Methodology

1. Import the required Python libraries.
2. Load the real-world Iris dataset.
3. Perform exploratory data analysis.
4. Check missing values and repeated measurements.
5. Detect potential outliers using the IQR method.
6. Calculate descriptive statistics.
7. Visualize data distributions using histograms and box plots.
8. Check normality using the Shapiro–Wilk test.
9. Check variance equality using Levene's test.
10. Perform Welch's independent two-sample t-test.
11. Calculate the test statistic and p-value.
12. Calculate the confidence interval and effect size.
13. Interpret statistical and practical significance.
14. Document the final findings.

## 🔬 Statistical Test Selection

Welch's independent two-sample t-test was selected because:

- The analysis compares two separate groups.
- Sepal length is a continuous numerical variable.
- The objective is to compare population means.
- The two groups show evidence of unequal variances.
- Welch's t-test does not require equal population variances.

## ✅ Assumption Validation

| Assumption | Method | Result |
|---|---|---|
| Normality of Setosa | Shapiro–Wilk test | p = 0.459513 |
| Normality of Versicolor | Shapiro–Wilk test | p = 0.464737 |
| Equality of variances | Levene's test | p = 0.005196 |
| Independence | Sampling assumption | Assumed, not fully verified |
| Outlier detection | IQR and box plots | Observations retained |
| Missing values | Data quality check | No missing analysis values |

The normality tests do not provide sufficient evidence to reject normality. However, Levene's test indicates unequal variances, supporting the selection of Welch's t-test.

## 📊 Experimental Results

| Parameter | Result |
|---|---:|
| Setosa sample size | 50 |
| Versicolor sample size | 50 |
| Setosa mean sepal length | 5.006 cm |
| Versicolor mean sepal length | 5.936 cm |
| Mean difference (Versicolor − Setosa) | 0.930 cm |
| t-statistic (Setosa − Versicolor) | -10.520986 |
| Degrees of freedom | 86.5380 |
| p-value | 3.74674261 × 10⁻¹⁷ |
| Significance level | 0.05 |
| 95% confidence interval for mean difference | 0.754 to 1.106 cm |
| Cohen's d (magnitude) | 2.104 |
| Hypothesis decision | Reject H₀ |

## 📈 Data Visualizations

The notebook includes the following visualizations:

- Species-wise sepal length distribution
- Histogram with density curve
- Box plot for outlier detection
- Q-Q plots for normality assessment
- Mean comparison bar chart
- Statistical distribution comparison

These visualizations help identify differences between the two groups and understand their distributions.

## 📉 Statistical Significance

The calculated p-value is approximately 3.747 × 10⁻¹⁷, which is considerably smaller than the significance level of 0.05.

Since p-value < 0.05, the null hypothesis is rejected.

Therefore, there is strong statistical evidence that the population mean sepal lengths of Iris Setosa and Iris Versicolor flowers differ.

The p-value represents the probability of obtaining a test statistic at least as extreme as the observed result, assuming the null hypothesis and statistical test assumptions are true. It does not represent the probability that the null hypothesis is true.

## 💡 Practical Significance

Statistical significance indicates whether the observed difference is supported by statistical evidence, whereas practical significance determines whether the difference is meaningful in a real-world application.

In this analysis:

- Versicolor flowers have an average sepal length 0.93 cm greater than Setosa flowers.
- Cohen's d magnitude of 2.104 indicates a large standardized difference.
- The confidence interval suggests that the population mean difference is between 0.754 cm and 1.106 cm.
- The difference exceeds an illustrative practical threshold of 0.5 cm.

These findings suggest that sepal length may be useful as a feature in botanical classification and machine learning applications. However, the practical threshold is illustrative rather than a validated botanical standard, and classification accuracy requires further evaluation.

## 📋 Key Findings

- The Iris dataset contains sufficient observations for comparing the selected groups.
- Neither normality test rejects the normality assumption.
- The two groups exhibit evidence of unequal variances.
- Welch's t-test is appropriate for the selected research question.
- The difference between the average sepal lengths is statistically significant.
- The effect size indicates a large standardized difference.
- Sepal length may be a useful feature for distinguishing the two species.

## ⚠️ Limitations

- Only two of the three Iris species were considered.
- Only sepal length was selected for hypothesis testing.
- Sampling independence and population representativeness cannot be completely verified.
- Statistical significance does not establish causation.
- Additional research is required to validate classification performance.

## 📁 Repository Structure

    Statistical-Hypothesis-Testing/
    ├── Hypothesis_Testing.ipynb
    └── README.md

## 🚀 How to Run the Project

1. Clone or download this GitHub repository.
2. Open Google Colab.
3. Upload the `Hypothesis_Testing.ipynb` file.
4. Select Runtime → Run all.
5. Explore the visualizations, statistical results, and final findings.

## 🎓 Learning Outcomes

- Understanding statistical hypothesis testing.
- Formulating null and alternative hypotheses.
- Selecting appropriate statistical tests.
- Validating statistical assumptions.
- Performing statistical analysis using SciPy.
- Interpreting p-values and confidence intervals.
- Differentiating statistical and practical significance.
- Communicating statistical findings effectively.

## 🏁 Conclusion

This project successfully demonstrates statistical hypothesis testing using a real-world dataset. Welch's independent two-sample t-test provides strong evidence that the average sepal lengths of Iris Setosa and Iris Versicolor flowers differ.

Versicolor flowers have an average sepal length approximately 0.93 cm greater than Setosa flowers. The small p-value and large effect size indicate a statistically significant and potentially practically meaningful difference.

The project highlights the importance of selecting appropriate statistical methods, validating assumptions, and interpreting results correctly before making data-driven decisions.

## 📚 References

- UCI Iris Dataset: https://archive.ics.uci.edu/dataset/53/iris
- SciPy Statistical Functions: https://docs.scipy.org/doc/scipy/reference/stats.html
- Scikit-learn Documentation: https://scikit-learn.org/
- Google Colab: https://colab.research.google.com/
