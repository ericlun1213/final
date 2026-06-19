# final
## Student Information

**Name:** [許紹倫]

**Student ID:** [112370218]

## Project Repository

https://github.com/[Your-GitHub-Username]/[Your-Repository-Name]

## Presentation Video

https://youtube.com/[Your-Actual-Video-URL]

## 1. Project Overview & Research Question

This project examines the critical relationship between physical behavior and mental health trajectories in adolescents using the **Youth Risk Behavior Surveillance System (YRBS 2007)** big data repository. 

* **Research Question:** Does the frequency of weekly physical activity significantly affect or reduce the level of subjective depression (feelings of sadness or hopelessness) among adolescents?
* **Hypotheses:**
  * **Null Hypothesis ($H_0$):** There is no statistically significant difference in the mean depression level across adolescents with different weekly physical activity grouping frequencies.
  * **Alternative Hypothesis ($H_1$):** There is a statistically significant difference in the mean depression level across adolescents with different weekly physical activity grouping frequencies.

## 2. Variables & Data Preparation

To establish a solid statistical analytical workflow, the operational raw dataset features were carefully subsetted and handled:

* **Dependent Variable (DV):** `SadOrHopeless` (A structured binary outcome metric tracking whether a student felt continuously sad or hopeless for $\ge$ 2 weeks straight; coded as 1 = Yes, 2 = No).
* **Independent Variable (IV):** `PhysicalActivity5OrMoreDays` (Originally a continuous response measuring days active. Following professor guidelines for data restructuring, it was explicitly recoded into three discrete observational groups):
  * **`0 days`**: No localized physical exercise per week.
  * **`1-3 days`**: Occasional or moderate exercise per week.
  * **`4+ days`**: Routine or high-frequency exercise per week.

*All missing observations (NaN entries) were structurally dropped during data preparation to preserve computation validity, yielding a definitive functional sample size of **13,657** students.*

## 3. Statistical Methodology

Because the independent variable is partitioned into **three separate categorical treatment groups** and the dependent variable yields a numerical mean score, a **One-way Analysis of Variance (ANOVA)** was implemented. 

To determine where the exact statistical divergence lies without inflating Type I error rates, a downstream **Tukey HSD (Honestly Significant Difference)** Post-hoc comparison test was deployed at an alpha threshold of $\alpha = 0.05$.


## 4. Conclusion

The analytical workflow successfully confirms that regular physical activity is an effective behavioral mitigator against mental depression tendencies in adolescents. Education systems and public health initiatives should actively design programs helping youths achieve at least **4 days of active exercise per week** to enhance long-term psychological resilience.
