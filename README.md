#Inferential-statistics
# Comprehensive Data Analysis Project

## Project Overview

This project encompasses a series of data analysis tasks focusing on different datasets to extract insights, answer specific questions, and provide actionable recommendations. It covers topics ranging from probability calculations and normal distribution analysis to hypothesis testing and ANOVA for understanding factor relationships.

## Datasets

This project utilizes data from various contexts:

1.  **Football Team Injury Data:** A contingency table detailing foot injuries among football players across different positions. (Problem 1)
2.  **Gunny Bags Breaking Strength Data:** Information on the breaking strength of gunny bags, assumed to follow a normal distribution. (Problem 2)
3.  **Zingaro Stone Hardness Data:** Contains Brinell's hardness index for polished and unpolished stones. (`Zingaro_Company.csv`) (Problem 3)
4.  **Dental Implant Hardness Data:** Details on the hardness of metal implants, influenced by dentists, implant methods, and alloy types. (`Dental Hardness data.xlsx - Data.csv`) (Problem 4)

## Problem Statements Addressed

This project addresses the following questions:

### Problem 1: Football Team Injury Analysis

A physiotherapist is studying the relationship between foot injuries and player positions.

1.1 What is the probability that a randomly chosen player would suffer an injury?
1.2 What is the probability that a player is a forward or a winger?
1.3 What is the probability that a randomly chosen player plays in a striker position and has a foot injury?
1.4 What is the probability that a randomly chosen injured player is a striker?

### Problem 2: Gunny Bags Breaking Strength Analysis

The breaking strength of gunny bags is normally distributed with a mean of 5 kg/sq. cm and a standard deviation of 1.5 kg/sq. cm.

2.1 What proportion of the gunny bags have a breaking strength of less than 3.17 kg per sq cm?
2.2 What proportion of the gunny bags have a breaking strength of at least 3.6 kg per sq cm.?
2.3 What proportion of the gunny bags have a breaking strength between 5 and 5.5 kg per sq cm.?
2.4 What proportion of the gunny bags have a breaking strength NOT between 3 and 7.5 kg per sq cm.?

### Problem 3: Zingaro Stone Printing Hardness Analysis

Zingaro needs stones with a Brinell's hardness index of at least 150 for optimum printing.

3.1 Zingaro has reason to believe that the unpolished stones may not be suitable for printing. Do you think Zingaro is justified in thinking so?
3.2 Is the mean hardness of the polished and unpolished stones the same?

### Problem 4: Dental Implant Hardness Analysis

The hardness of metal implants depends on multiple factors such as method, temperature, alloy, and dentist.

4.1 How does the hardness of implants vary depending on dentists?
4.2 How does the hardness of implants vary depending on methods?
4.3 What is the interaction effect between the dentist and method on the hardness of dental implants for each type of alloy?
4.4 How does the hardness of implants vary depending on dentists and methods together?

## Methodology

This project employs a range of statistical and analytical techniques:

-   **Probability Theory:** For calculating various probabilities from contingency tables (Problem 1).
-   **Normal Distribution & Z-scores:** For determining proportions within a normally distributed dataset (Problem 2).
-   **Hypothesis Testing:**
    -   **One-Sample t-test:** To compare a sample mean against a known population mean (Problem 3.1).
    -   **Two-Sample Independent t-test:** To compare means of two independent groups (Problem 3.2).
    -   **One-Way ANOVA:** To assess significant differences in means across multiple groups for a single factor (Problems 4.1, 4.2).
    -   **Two-Way ANOVA:** To analyze main effects and interaction effects of two independent variables on a dependent variable (Problems 4.3, 4.4).
-   **Assumption Checks:** For ANOVA and t-tests, assumptions like normality of residuals (Shapiro-Wilk Test) and homogeneity of variances (Levene's Test) were considered.
-   **Post-hoc Tests:** Tukey HSD for pairwise comparisons following significant ANOVA results.
-   **Data Visualization:** Box plots and interaction plots to visually represent data distributions and relationships.
-   **Tools:** Python programming language with libraries such as `pandas` for data manipulation, `scipy.stats` for statistical tests, `statsmodels.formula.api` for ANOVA, and `matplotlib.pyplot` and `seaborn` for plotting.

## Key Findings & Business Recommendations

### Problem 1: Football Team Injury Analysis

-   **1.1 Probability of Injury:** P(Injured) = 145 / 235 ≈ 0.617 (61.7%)
-   **1.2 Probability of Forward or Winger:** P(Forward or Winger) = (94 + 29) / 235 = 123 / 235 ≈ 0.523 (52.3%)
-   **1.3 Probability of Striker and Injury:** P(Striker AND Injured) = 45 / 235 ≈ 0.191 (19.1%)
-   **1.4 Probability of Injured Player being a Striker:** P(Striker | Injured) = 45 / 145 ≈ 0.310 (31.0%)

### Problem 2: Gunny Bags Breaking Strength Analysis

*(Visual representations would typically accompany these in a full report)*
-   **2.1 Proportion < 3.17 kg/sq cm:** Approximately 10.93% of gunny bags have a breaking strength less than 3.17 kg/sq cm (Z-score = -1.22).
-   **2.2 Proportion at least 3.6 kg/sq cm:** Approximately 82.26% of gunny bags have a breaking strength of at least 3.6 kg/sq cm (Z-score = -0.93).
-   **2.3 Proportion between 5 and 5.5 kg/sq cm:** Approximately 13.06% of gunny bags have a breaking strength between 5 and 5.5 kg/sq cm (Z-scores = 0.0, 0.33).
-   **2.4 Proportion NOT between 3 and 7.5 kg/sq cm:** Approximately 11.43% of gunny bags have a breaking strength not between 3 and 7.5 kg/sq cm (Z-scores = -1.33, 1.67).

### Problem 3: Zingaro Stone Printing Hardness Analysis

-   **3.1 Justification for Unsuitable Unpolished Stones:**
    -   The mean hardness of unpolished stones is 121.44.
    -   One-Sample t-test comparing unpolished stone hardness to 150: T-statistic = -4.909, P-value = 0.000.
    -   **Conclusion:** With a p-value < 0.05, we reject the null hypothesis. Zingaro is **justified** in thinking that unpolished stones may not be suitable for printing, as their mean hardness (121.44) is significantly less than the required 150.
-   **3.2 Equality of Mean Hardness (Polished vs. Unpolished):**
    -   Mean hardness of unpolished stones: 121.44
    -   Mean hardness of polished stones: 147.47
    -   Levene's Test for equality of variances: P-value = 0.000 (< 0.05), indicating variances are **not equal**.
    -   Independent Two-Sample t-test (unequal variances): T-statistic = -4.135, P-value = 0.000.
    -   **Conclusion:** With a p-value < 0.05, we reject the null hypothesis. The mean hardness of unpolished and polished stones is **statistically different**. Polished stones generally have significantly higher hardness.

### Problem 4: Dental Implant Hardness Analysis

-   **4.1 Dentist Effect:** No statistically significant difference in implant hardness was found across different dentists for either Alloy 1 or Alloy 2 when considered as a sole factor.
-   **4.2 Method Effect:** A statistically significant difference in implant hardness was observed across different methods for **both Alloy 1 and Alloy 2**. Method 3 consistently resulted in significantly lower hardness compared to Methods 1 and 2 for both alloy types.
-   **4.3 & 4.4 Interaction and Combined Effects:**
    -   For **Alloy 1**, a statistically significant interaction effect was found between Dentist and Method (p-value = 0.0068). This means the effect of a specific method on implant hardness depends on the dentist performing it, implying that optimal method usage might vary by dentist.
    -   For **Alloy 2**, no statistically significant interaction effect was detected (p-value = 0.0932). This indicates that the effect of a method on hardness is consistent across all dentists for this alloy type, allowing for more standardized method protocols.
    -   For Alloy 1, all main effects (Dentist, Method) and their interaction were significant. For Alloy 2, only the Method main effect was significant.

### Business Recommendations (Across All Problems Where Applicable):

1.  **Dental Implants - Method Optimization:** Prioritize Methods 1 and 2 over Method 3 for dental implants across all alloys, as Method 3 consistently yields lower hardness. Further investigation into Method 3's process is recommended.
2.  **Dental Implants - Tailored Training for Alloy 1:** Given the significant interaction for Alloy 1, implement tailored training or best practice guidelines for dentists. Identify which dentist-method combinations yield optimal results and disseminate this knowledge.
3.  **Dental Implants - Standardization for Alloy 2:** For Alloy 2, methods can be more universally standardized as their effectiveness on hardness is consistent regardless of the dentist.
4.  **Zingaro Stones - Material Selection:** Zingaro is justified in its concern about unpolished stones. Polished stones show significantly higher and potentially suitable hardness. Prioritize polished stones for printing to ensure optimal image quality based on hardness requirements. If unpolished stones must be used, a pre-treatment to increase hardness would be advisable.
5.  **Gunny Bags - Quality Control:** Implement quality checks to identify gunny bags with breaking strengths below critical thresholds (e.g., 3.17 kg/sq cm) to minimize wastage and pilferage within the supply chain. This insight can help in setting acceptance criteria for new batches.
6.  **Football Team Injuries - Positional Risk Assessment:** The probability analysis highlights positions with higher injury rates (e.g., Forwards and Strikers). This can inform targeted injury prevention programs, specific strength and conditioning for high-risk positions, and closer monitoring by physiotherapists for players in these roles.

---
