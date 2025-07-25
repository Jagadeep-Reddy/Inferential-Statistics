# Inferential-Statistics
# Dental Implant Hardness Analysis

## Project Overview

This project focuses on analyzing a dataset related to the hardness of dental implants, investigating how various factors such as the dentist, the implant method, and their interactions influence the final hardness of implants for different alloy types. The analysis utilizes statistical methods and data visualization to uncover significant relationships and provide actionable insights.

## Dataset

The primary dataset used for this analysis is `Dental Hardness data.xlsx - Data.csv`. It contains observations on:
-   `Dentist`: The dentist performing the implant procedure.
-   `Method`: The specific method used for the implant.
-   `Alloy`: The type of alloy used in the implant.
-   `Temp`: The temperature during the process (though not explicitly analyzed for its effect on hardness in the provided problems).
-   `Response` (renamed to `Hardness`): The measured hardness of the dental implant.

## Problem Statements Addressed

This analysis addresses the following key questions from Problem 4:

### 4.1 How does the hardness of implants vary depending on dentists?
   - Investigates the main effect of `Dentist` on `Hardness` for each `Alloy` type using One-Way ANOVA.

### 4.2 How does the hardness of implants vary depending on methods?
   - Examines the main effect of `Method` on `Hardness` for each `Alloy` type using One-Way ANOVA and post-hoc tests.

### 4.3 What is the interaction effect between the dentist and method on the hardness of dental implants for each type of alloy?
   - Explores the interaction between `Dentist` and `Method` on `Hardness` for each `Alloy` type using Two-Way ANOVA and visual interaction plots.

### 4.4 How does the hardness of implants vary depending on dentists and methods together?
   - A comprehensive analysis using Two-Way ANOVA to understand the combined and individual effects of `Dentist` and `Method`, as well as their interaction, on `Hardness` for each `Alloy`.

## Methodology

The analysis employs a robust statistical approach:

-   **One-Way ANOVA:** Used to assess the significant difference in mean hardness across different levels of a single factor (Dentist or Method).
-   **Two-Way ANOVA:** Employed to analyze the individual and combined (interaction) effects of `Dentist` and `Method` on `Hardness`.
-   **Tukey HSD Post-hoc Test:** Applied when ANOVA results indicate a significant difference, to identify which specific groups differ from each other.
-   **Assumption Checks:** Normality of residuals (Shapiro-Wilk Test) and homogeneity of variances (Levene's Test) were performed to validate ANOVA assumptions.
-   **Data Visualization:** Box plots and interaction plots are generated using Seaborn and Matplotlib to visually represent data distributions and potential interaction effects.
-   **Tools:** Python programming language with libraries such as `pandas` for data manipulation, `scipy.stats` for statistical tests, `statsmodels` for ANOVA, and `matplotlib.pyplot` and `seaborn` for plotting.

## Key Findings & Business Recommendations

### Summary of Results:

-   **Dentist Effect (Problem 4.1):** No statistically significant difference in implant hardness was found across different dentists for either Alloy 1 or Alloy 2. This suggests that the individual dentist does not, on average, significantly impact the implant hardness when considered alone.
-   **Method Effect (Problem 4.2):** A statistically significant difference in implant hardness was observed across different methods for **both Alloy 1 and Alloy 2**. Specifically, Method 3 consistently resulted in significantly lower hardness compared to Methods 1 and 2 for both alloy types.
-   **Interaction Effect (Problem 4.3 & 4.4):**
    -   For **Alloy 1**, a statistically significant interaction effect was found between Dentist and Method. This indicates that the effect of a specific method on implant hardness depends on the dentist performing it. Some dentists might perform better with certain methods, and vice-versa.
    -   For **Alloy 2**, no statistically significant interaction effect was detected. This implies that the effect of a specific method on hardness is consistent across all dentists; the methods perform predictably regardless of who performs them.
-   **Combined Effects (Problem 4.4):**
    -   For **Alloy 1**, all effects (Dentist, Method, and their Interaction) were found to be statistically significant, emphasizing a complex interplay.
    -   For **Alloy 2**, only the Method effect was significant, while the Dentist main effect and the Dentist-Method interaction were not.

### Business Recommendations:

1.  **Standardize Methods (Especially for Alloy 2):** Given that Method 3 consistently yields lower hardness for both alloys and that method effects are consistent across dentists for Alloy 2, standardizing to Methods 1 or 2 (which generally yield higher hardness) should be considered, particularly for Alloy 2.
2.  **Targeted Training & Best Practices (For Alloy 1):** The significant interaction for Alloy 1 suggests that a "one-size-fits-all" approach to methods may not be optimal. It is crucial to identify which dentists excel with which methods and potentially implement tailored training programs or best practices to optimize hardness outcomes specific to dentist-method combinations for Alloy 1.
3.  **Investigate Method 3:** The consistently lower hardness observed with Method 3 warrants further investigation. This could involve reviewing the process steps, materials, or equipment associated with Method 3 to understand and address the cause of reduced hardness.
4.  **Focus on Method Improvement (Overall):** Since methods have a significant impact on hardness for both alloys, continuous improvement and refinement of implant methods are vital to ensure high-quality dental implants.

---

Feel free to explore the code and the generated plots for a more detailed understanding of the analysis.
