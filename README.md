# Project Cycle 3: Gender and Sad or Hopeless Feeling
### Two-Sample Inference on Gender Difference in Sad or Hopeless Feelings

## Group & Members
* **Group Number**: 4
* **Members**:
    * 111370229 李尚諭
    * 113370238 鍾訓弘

## Dataset
raw data:
* `YRBS_2007.csv`

processed data:
* `cycle3_selected_variables.csv`

## Research Question
**Is the proportion of students who felt sad or hopeless different between male and female students?**

This project compares the proportion of students who felt sad or hopeless between female and male students using the YRBS 2007 dataset.

## Selected Variables
* **Group Variable**: `WhatIsYourSex`
    * Original coding:
        * 1 = Female
        * 2 = Male
    * Recoded coding:
        * 1 = Female
        * 0 = Male

* **Response Variable**: `SadOrHopeless`
    * Original coding:
        * 1 = Yes
        * 2 = No
    * Recoded coding:
        * 1 = Yes, felt sad or hopeless
        * 0 = No, did not feel sad or hopeless

## Hypotheses
Let:

* \(p_{female}\) = the population proportion of female students who felt sad or hopeless.
* \(p_{male}\) = the population proportion of male students who felt sad or hopeless.

The hypotheses are:

* **Null Hypothesis \(H_0\)**: \(p_{female} = p_{male}\)
* **Alternative Hypothesis \(H_1\)**: \(p_{female} \ne p_{male}\)

This is a two-sided test because the research question asks whether the two proportions are different.

## Statistical Method
Because the response variable `SadOrHopeless` is binary, this project uses a **two-proportion z-test** to compare the two population proportions.

The estimated difference is calculated as:

\[
\hat{p}_{female} - \hat{p}_{male}
\]

A 95% confidence interval is also calculated for the difference in proportions.

## Project Workflow
1. Select the research question and variables.
2. Load the raw YRBS 2007 dataset.
3. Select `WhatIsYourSex` and `SadOrHopeless`.
4. Check missing values for the two selected variables.
5. Remove rows with missing or invalid values.
6. Recode both variables into binary form.
7. Create descriptive summaries and visualizations.
8. Conduct the two-proportion z-test.
9. Calculate the 95% confidence interval for the difference in proportions.
10. Interpret the result in context.

## Main Results
The female sample proportion of students who felt sad or hopeless was higher than the male sample proportion.

* Female sample proportion: approximately **0.372**
* Male sample proportion: approximately **0.227**
* Estimated difference \(\hat{p}_{female} - \hat{p}_{male}\): approximately **0.145**
* Group with higher sample proportion: **Female**
* Decision at \(\alpha = 0.05\): **Reject \(H_0\)**

## Final Conclusion
At a 5% significance level, the two-proportion z-test rejected the null hypothesis. There is statistically significant evidence that the proportion of students who felt sad or hopeless is different between female and male students.

The female group had the higher sample proportion. The estimated difference was about **14.5 percentage points**, meaning that the proportion of female students who felt sad or hopeless was higher than the proportion of male students who felt sad or hopeless.

Because the YRBS dataset is observational survey data, this result should be interpreted as a difference in proportions between groups, not as a causal relationship.

## Project Structure
```text
project-cycle-3/
  README.md
  data/
    raw/
      YRBS_2007.csv
    processed/
      cycle3_selected_variables.csv
  notebooks/
    01_Cycle3_Data_Cleaning.ipynb
    02_Cycle3_EDA_and_Summary.ipynb
    03_Cycle3_Inference.ipynb
  outputs/
    figures/
    tables/
    summary/
  report/
  references/
```

## Output Files
figures:
* `cycle3_missing_value_pie_chart.png`
* `cycle3_four_group_proportion_bar_chart.png`
* `cycle3_within_gender_proportion_bar_chart.png`

tables:
* `cycle3_missing_value_summary.csv`
* `cycle3_four_group_proportion_summary.csv`
* `cycle3_within_gender_proportion_summary.csv`
* `cycle3_inference_group_summary.csv`
* `cycle3_main_inference_result.csv`
* `cycle3_compact_inference_result.csv`
* `cycle3_assumption_check.csv`

summary:
* `cycle3_final_interpretation.txt`
