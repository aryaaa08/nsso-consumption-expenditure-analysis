# 📊 NSSO HCES 2023–24: Household Welfare & Consumption Inequality in India

<div align="center">

![R](https://img.shields.io/badge/Language-R%204.2%2B-276DC3?style=flat-square\&logo=r\&logoColor=white)
![Data](https://img.shields.io/badge/Data-NSSO%20HCES%202023--24-orange?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Quarto](https://img.shields.io/badge/Report-Quarto-blueviolet?style=flat-square)

### 📈 Household Consumption, Nutrition, Education & Social Inequality Analysis using NSSO HCES 2023–24

**Tech Stack:** R • Quarto • dplyr • ggplot2 • Statistical Testing • Data Visualization

</div>

---

# 🔍 Overview

Household consumption expenditure is one of the most reliable indicators of economic well-being in India, where income data is often incomplete or underreported. This project uses **unit-level microdata** from the **National Sample Survey Office (NSSO) Household Consumer Expenditure Survey (HCES) 2023–24** to examine five interconnected dimensions of household welfare.

The study investigates:

* How unequal consumption is across the expenditure distribution.
* The magnitude and persistence of the rural–urban consumption gap.
* Nutritional adequacy and calorie poverty across expenditure groups.
* The relationship between education and household welfare.
* Differences in asset ownership across social groups.

The analysis covers **over 3.47 crore household observations** across rural and urban India and integrates food expenditure, non-food expenditure, calorie conversion, education, demographic characteristics, and social group information from multiple NSSO survey levels.

---

# ❓ Research Questions

| # | Question                                                                                                                                    | Method                                                       |
| - | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| 1 | How is Monthly Per Capita Consumption Expenditure (MPCE) distributed, and how do food vs. non-food spending patterns differ across deciles? | Decile analysis, histograms, boxplots                        |
| 2 | Is there a statistically significant rural–urban gap in MPCE, and does it persist across the expenditure distribution?                      | Welch Two-Sample t-test, decile analysis                     |
| 3 | What proportion of households falls below calorie norms, and how do food-sourcing strategies change with expenditure?                       | Calorie conversion, poverty thresholds, source decomposition |
| 4 | Does the education level of the household head significantly influence household consumption (MPCE)?                                        | One-Way ANOVA, Tukey HSD                                     |
| 5 | Do social groups differ in ownership of essential and non-essential household assets?                                                       | Chi-Square Test of Independence                              |

---

# 🔑 Key Findings

## Q1 — Consumption Inequality

* Mean MPCE rises from **₹9,427** in the bottom decile to **₹84,412** in the top decile — a nearly **9× disparity**.
* MPCE distribution is heavily **right-skewed**, with extreme expenditure concentration among top-consuming households.
* **Non-food expenditure grows substantially faster** than food expenditure across deciles, supporting **Engel's Law**.
* In higher deciles, non-food spending becomes the dominant component of total household consumption.

---

## Q2 — Rural–Urban Divide

* Mean MPCE equals **₹23,186 for Rural households** and **₹37,431 for Urban households**.
* The average monthly per-capita gap is approximately **₹14,250**.
* Welch Two-Sample t-test confirms that the difference is **statistically significant**.
* Decile curves remain largely parallel, suggesting a persistent level difference rather than structural divergence.

---

## Q3 — Nutritional Adequacy

* A substantial share of households falls below both the **Indian calorie norms (2400/2100 kcal)** and the **international threshold (2100 kcal)**.
* Calorie poverty declines steadily as MPCE increases.
* Lower-income households depend more heavily on **Public Distribution System (PDS)** support and **home-produced food**.
* Higher-income households increasingly rely on **market purchases** for calorie consumption.

---

## Q4 — Education & Consumption

* Education level is strongly associated with household consumption expenditure.
* ANOVA results indicate statistically significant differences in MPCE across education categories.
* Graduate-led households exhibit substantially higher MPCE than households headed by individuals with low educational attainment.
* Returns to education become increasingly pronounced from secondary education onward.

---

## Q5 — Social Group & Asset Ownership

* Essential asset ownership is widespread but remains lower among historically disadvantaged groups.
* Ownership of non-essential assets exhibits a strong social gradient.
* Significant differences in ownership patterns are observed across social groups.
* Social stratification continues to influence access to household resources and economic resilience.

---

# 📁 Repository Structure

```text
nsso-consumption-expenditure-analysis/
│
├── README.md
│
├── quarto/
│   └── NSSO_Analysis.qmd
│
├── report/
│   └── NSSO_R_EPORT_FINAL.pdf
│
└── outputs/
    ├── mpce_dashboard.png
    ├── rural_urban_gap.png
    ├── calorie_poverty.png
    └── calorie_sources.png
```

---

# 🗃️ Dataset

### Source

**National Sample Survey Office (NSSO)**
**Household Consumer Expenditure Survey (HCES) 2023–24**

### Unit of Analysis

Household

### Data Components

The project combines multiple NSSO survey levels containing:

* Household demographics
* Consumption expenditure
* Food quantities
* Education information
* Social group characteristics
* Asset ownership data
* Food acquisition sources

---

# ⚙️ Methodology

## Data Preparation

* Constructed unique household identifiers (HHID)
* Merged multiple NSSO survey modules
* Standardized 7-day and 365-day recall periods
* Aggregated household-level expenditure measures
* Computed Monthly Per Capita Consumption Expenditure (MPCE)

## Statistical Analysis

### 📊 Consumption Analysis

* MPCE Decile Distribution
* Mean and Median Expenditure Analysis
* Food vs Non-Food Expenditure Decomposition

### 🌆 Rural–Urban Comparison

* Welch Two-Sample t-Test
* Decile-wise Expenditure Comparison
* Confidence Interval Estimation

### 🍽️ Nutritional Analysis

* Calorie Conversion using Standard Food Factors
* Daily Per-Capita Calorie Estimation
* Calorie Poverty Assessment
* Nutritional Adequacy Evaluation

### 🎓 Education Analysis

* One-Way ANOVA
* Tukey HSD Post-Hoc Testing

### 🏠 Asset Ownership Analysis

* Cross-Tabulations
* Social Group Comparisons
* Statistical Significance Testing

---

# 🛠️ Tools & Technologies

* R
* Quarto
* dplyr
* tidyr
* ggplot2
* haven
* patchwork
* gridExtra

---

# 📈 Visual Outputs

The project includes:

* MPCE Distribution Dashboard
* Rural–Urban Consumption Gap Analysis
* Calorie Poverty Assessment
* Calorie Source Composition Analysis
* Education and Consumption Analysis
* Asset Ownership Comparison

---

# 📂 Data Availability

The raw NSSO HCES 2023–24 microdata is **not included** in this repository due to access restrictions and file size limitations.

Researchers interested in reproducing the analysis should obtain the data independently from the **Ministry of Statistics and Programme Implementation (MoSPI)** and update the local file paths within the Quarto workflow.

---

# 🔄 Reproducibility

To reproduce the analysis:

1. Obtain NSSO HCES 2023–24 unit-level microdata.
2. Install the required R packages.
3. Open `quarto/NSSO_Analysis.qmd`.
4. Update local data paths.
5. Render the Quarto document to generate all outputs and analyses.

---

# 📄 Report

The complete analytical report is available in:

```text
report/NSSO_R_EPORT_FINAL.pdf
```

The report contains:

* Data preparation workflow
* Statistical analysis
* Hypothesis testing
* Visualizations
* Interpretation of results
* Policy-oriented discussion

---

# 👩‍💻 Author

**Anjali Arya**

**B.S. in Analytics and Sustainability Studies**

---

<div align="center">

### ⭐ If you found this project interesting, consider giving the repository a star.

</div>
