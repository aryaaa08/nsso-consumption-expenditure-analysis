# NSSO Household Consumption & Nutritional Inequality Analysis (India 2023–24)

## Project Overview

This project analyzes household-level consumption data from the National Sample Survey Office (NSSO) Household Consumption Expenditure Survey (HCES) 2023–24 to examine patterns of economic welfare, consumption inequality, and nutritional adequacy in India.

Using R and statistical analysis techniques, the study investigates how household expenditure, calorie intake, education, and demographic characteristics influence living standards across rural and urban India.

The project combines expenditure-based and nutrition-based welfare indicators to provide evidence on inequality, consumption behavior, and food security.

---

## Research Questions

This study addresses the following questions:

### 1. Consumption Distribution
- How is Monthly Per Capita Consumption Expenditure (MPCE) distributed across households?
- How do food and non-food expenditures vary across expenditure deciles?

### 2. Rural–Urban Welfare Gap
- Do rural and urban households differ significantly in their average MPCE?
- Does the expenditure gap remain consistent across the distribution?

### 3. Nutritional Adequacy
- How does calorie intake vary across MPCE deciles?
- What proportion of households fall below calorie poverty thresholds?

### 4. Education and Consumption
- Is higher educational attainment associated with higher household consumption?

### 5. Social Group and Asset Ownership
- How does ownership of essential and non-essential assets differ across social groups?

---

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

## Key Findings

### Consumption Inequality

- MPCE rises sharply across expenditure deciles.
- Consumption inequality is driven largely by upper-tail expenditure concentration.
- Non-food expenditure grows substantially faster than food expenditure in higher deciles.

### Rural–Urban Gap

- Urban households exhibit significantly higher MPCE than rural households.
- The rural–urban expenditure gap remains relatively stable across deciles.

### Nutrition and Calorie Poverty

- Calorie poverty declines as household expenditure increases.
- Higher MPCE is strongly associated with improved nutritional adequacy.
- Poorer households rely more heavily on subsidized and self-produced food sources.

### Education and Welfare

- Higher educational attainment is associated with significantly higher household consumption levels.
- Education emerges as an important determinant of household welfare.

---

## Project Structure

```text
nsso-consumption-expenditure-analysis/

├── README.md
├── report/
│   └── NSSO_R_EPORT_FINAL.pdf
│
├── code/
│   └── analysis.R
│
├── outputs/
│   ├── mpce_dashboard.png
│   ├── rural_urban_gap.png
│   ├── calorie_poverty.png
│   └── calorie_sources.png
```

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

## Disclaimer

The NSSO unit-level data used in this project may be subject to access and usage restrictions. This repository is intended for educational, research, and portfolio purposes.
