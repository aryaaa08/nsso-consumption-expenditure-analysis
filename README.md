📊 NSSO HCES 2023–24: Household Welfare & Consumption Inequality in India

🔍 Overview
Household consumption expenditure is one of the most reliable indicators of economic well-being in India, where income data is often incomplete or underreported. This project uses unit-level microdata from the NSSO's 2023–24 Household Consumer Expenditure Survey (HCES) to examine five interconnected dimensions of household welfare:

How unequal is consumption across the expenditure distribution?
How large is the rural–urban divide, and is it consistent across income groups?
Are Indian households calorically adequate, and how does this vary with spending?
Does the household head's education level predict consumption outcomes?
Does caste-based social group membership shape access to household assets?

The analysis covers over 3.47 crore household observations across all states and union territories of India, combining food expenditure, non-food expenditure, nutritional conversion, and socio-demographic data from multiple NSSO survey levels.

❓ Research Questions
#QuestionMethod1How is Monthly Per Capita Consumption Expenditure (MPCE) distributed, and how do food vs. non-food spending patterns differ across deciles?Decile analysis, histogram, boxplots2Is there a statistically significant rural–urban gap in MPCE, and does it persist across the expenditure distribution?Welch two-sample t-test, decile curves3What share of households falls below calorie norms, and how do food-sourcing strategies shift with expenditure?Calorie conversion, poverty thresholds, source decomposition4Does household head's education level significantly predict household consumption (MPCE)?One-way ANOVA, Tukey HSD post-hoc test5Do social groups (ST, SC, OBC, Others) differ in ownership of essential vs. non-essential household assets?Chi-square test of independence

🔑 Key Findings
Q1 — Consumption Inequality

Mean MPCE rises from ₹9,427 (bottom decile) to ₹84,412 (top decile) — a ~9x disparity
MPCE distribution is heavily right-skewed; top-decile mean far exceeds median, indicating extreme upper-tail concentration
Non-food MPCE grows far faster than food MPCE across deciles — consistent with Engel's Law
By the top deciles, non-food expenditure dominates total consumption, reflecting discretionary spending

Q2 — Rural–Urban Divide

Mean MPCE: ₹23,186 (Rural) vs. ₹37,431 (Urban) — a monthly gap of ~₹14,250
Gap is statistically significant (t = −1333, p < 0.001)
Decile curves are nearly parallel, indicating the gap is a level difference, not a structural divergence

Q3 — Nutritional Adequacy

A significant share of the population falls below both the Indian norm (2400/2100 kcal) and the international threshold (2100 kcal)
Calorie poverty rates decline sharply with rising MPCE, but persist even in middle deciles
Poorer households rely more on PDS and home production; richer households shift toward market purchases

Q4 — Education & Consumption

ANOVA: F = 1335, p < 0.001 — education level is strongly associated with MPCE
Mean MPCE for graduate-led households is ₹21,481 higher than illiterate-led households
No significant difference between "Literate (no school)" and "Primary" — basic literacy alone provides limited returns
Large returns emerge from secondary education onward; diploma and graduate levels yield the highest gains

Q5 — Social Group & Asset Ownership

Essential asset ownership is near-universal, but ST and SC households lag even at this baseline
Non-essential asset ownership shows a sharp social gradient: ST/SC < OBC < Others
Chi-square results: Essential (χ² = 250.89, p < 0.001), Non-Essential (χ² = 71.41, p < 0.001)
Caste-based stratification shapes not just wealth, but access to comfort and economic resilience
---

## 📁 Repository Structure

```text
nsso-consumption-expenditure-analysis/
│
├── README.md
│   └── Project documentation, methodology, findings, and usage guide
│
├── quarto/
│   └── NSSO_Analysis.qmd
│       └── Complete Quarto workflow containing data preparation,
│           statistical analysis, visualisations, and report generation
│
├── report/
│   └── NSSO_R_EPORT_FINAL.pdf
│       └── Final project report with methodology, code,
│           outputs, statistical tests, and interpretation
│
└── outputs/
    ├── mpce_dashboard.png
    ├── rural_urban_gap.png
    ├── calorie_poverty.png
    └── calorie_sources.png
        └── Key visualisations generated from the analysis
```


## Dataset

**Source:** NSSO Household Consumption Expenditure Survey (HCES) 2023–24

**Unit of Analysis:** Household

The project combines multiple NSSO survey levels containing:

- Household demographics
- Consumption expenditure
- Food quantities
- Education information
- Social group characteristics
- Asset ownership data
- Food acquisition sources

---

## Methodology

### Data Preparation

- Constructed unique household identifiers (HHID)
- Merged multiple NSSO survey modules
- Standardized 7-day and 365-day recall periods
- Aggregated household-level expenditure measures
- Computed Monthly Per Capita Consumption Expenditure (MPCE)

### Statistical Analysis

#### Consumption Analysis
- MPCE Decile Distribution
- Mean and Median Expenditure Analysis
- Food vs Non-Food Expenditure Decomposition

#### Rural–Urban Comparison
- Welch Two-Sample t-Test
- Decile-wise expenditure comparisons
- Confidence interval estimation

#### Nutritional Analysis
- Calorie conversion using standard food calorie factors
- Daily per-capita calorie estimation
- Calorie poverty assessment
- Nutritional adequacy evaluation

#### Education Analysis
- One-Way ANOVA
- Tukey HSD Post-Hoc Testing

#### Asset Ownership Analysis
- Cross-tabulations
- Social group comparisons
- Statistical significance testing

---

## Tools & Technologies

- R
- dplyr
- tidyr
- ggplot2
- patchwork
- haven
- gridExtra

---

## Visual Outputs

The project includes:

- MPCE Distribution Dashboard
- Rural–Urban Consumption Gap Analysis
- Calorie Poverty Assessment
- Calorie Source Composition Analysis
- Education vs Consumption Analysis
- Asset Ownership Comparisons

---

## Reproducibility

To reproduce the analysis:

1. Obtain NSSO HCES 2023–24 unit-level data.
2. Install required R packages.
3. Run the analysis scripts in the `code/` directory.
4. Generate outputs and visualizations.

---

## Author

**Anjali Arya**

BS in Analytics and Sustainability Studies

---

📜 License
This project is licensed under the MIT License. The underlying NSSO data is the property of the Government of India / MoSPI and is subject to their own terms of use.

The NSSO unit-level data used in this project may be subject to access and usage restrictions. This repository is intended for educational, research, and portfolio purposes.
