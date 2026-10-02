# Education Investment & Adult Literacy — ANOVA Analysis

## 📌 Project Overview

This project investigates whether **government education spending levels are associated with differences in adult literacy rates**.

Using an education dataset, countries are categorized into **Low, Medium, and High government education-spending tiers**. Statistical analysis is then performed to determine whether the mean adult literacy rates differ significantly across these groups.

The project demonstrates an end-to-end statistical analysis workflow, including:

* Data acquisition and cleaning
* Feature grouping using quantiles
* Descriptive statistics
* Statistical assumption testing
* One-way ANOVA
* Tukey HSD post-hoc analysis
* Effect-size calculation using Eta-Squared (η²)
* Data visualization

---

## 🔗 Google Colab

**Run the complete analysis in Google Colab:**

[Open Project in Google Colab](https://colab.research.google.com/drive/1Y0n5NNHERATZB-46beclfbgNuPEj8XrR?usp=sharing)

The original analysis notebook is available through the Colab link included in the project source file.

---

## 🎯 Research Question

> **Do countries with different levels of government education spending have significantly different adult literacy rates?**

### Hypotheses

**H₀ (Null Hypothesis):**

Mean adult literacy rates are equal across the Low, Medium, and High spending groups.

**H₁ (Alternative Hypothesis):**

At least one spending group has a different mean adult literacy rate.

---

## 📊 Methodology

### 1. Data Acquisition

The project uses the **World Education Dataset** obtained through KaggleHub.

The analysis focuses on:

* `gov_exp_pct_gdp` — Government education expenditure as a percentage of GDP
* `lit_rate_adult_pct` — Adult literacy rate
* `country`
* `year`

---

### 2. Data Cleaning

Rows containing missing values in the primary analysis variables are removed.

Countries are then divided into three approximately equal-sized spending groups using quantile-based binning:

| Group           | Description                                  |
| --------------- | -------------------------------------------- |
| Low Spending    | Lower third of government education spending |
| Medium Spending | Middle third                                 |
| High Spending   | Upper third                                  |

A cleaned dataset is also exported as:

`clean_project_data.csv`

---

### 3. Descriptive Statistics

For each spending tier, the analysis calculates:

* Number of observations
* Mean adult literacy rate
* Standard deviation

This provides an initial comparison of literacy-rate distributions across spending groups.

---

### 4. Statistical Assumption Testing

Before performing the group comparison, statistical assumptions are examined using:

**Shapiro-Wilk Test**

Used to assess the normality of literacy-rate distributions within each spending group.

**Levene's Test**

Used to assess whether the variance of literacy rates is approximately equal across the three spending groups.

---

### 5. ANOVA

A one-way ANOVA framework is used to test whether mean adult literacy rates differ across:

```text
Low Spending
      ↓
Medium Spending
      ↓
High Spending
```

The analysis uses:

* Significance level: **α = 0.05**
* F-statistic
* Between-group degrees of freedom
* Within-group degrees of freedom
* p-value

---

### 6. Post-Hoc Analysis

When the overall ANOVA indicates a statistically significant difference, **Tukey's HSD** is used to identify which pairs of spending groups differ.

The pairwise comparisons include:

* Low vs Medium
* Low vs High
* Medium vs High

This provides more detailed insight than the overall ANOVA alone.

---

### 7. Effect Size

The project calculates **Eta-Squared (η²)** to estimate the proportion of variability in adult literacy rates associated with the spending-tier grouping.

The analysis reports:

```text
η²
Percentage of variance explained
Effect-size category
```

This complements statistical significance by describing the magnitude of the observed group effect.

---

## 📈 Visualization

A violin plot is generated to visualize the distribution of adult literacy rates across the three government-spending tiers.

Output:

`literacy_distribution.png`

The visualization helps compare the distribution, spread, and central tendency of literacy rates between spending groups.

---

## 🛠️ Technologies & Libraries

**Language**

* Python

**Libraries**

* Pandas
* NumPy
* SciPy
* Statsmodels
* Matplotlib
* Seaborn
* KaggleHub

**Environment**

* Google Colab
* Jupyter/Python

---

## 📂 Project Structure

```text
├── README.md
├── education_investment_literacy_ANOVA.ipynb
```

---

## 💡 Key Skills Demonstrated

This project demonstrates practical experience with:

* Data cleaning and preprocessing
* Exploratory data analysis
* Quantile-based feature engineering
* Descriptive statistics
* Statistical hypothesis testing
* ANOVA
* Assumption testing
* Tukey HSD post-hoc analysis
* Effect-size interpretation
* Data visualization
* Python-based statistical analysis
* Reproducible analytical workflows

---

## ⚠️ Reproducibility Note

The analysis downloads the World Education Dataset through KaggleHub. Therefore, internet access and the required dataset availability are necessary when running the analysis from scratch.

---

## 👩‍💻 Project Focus

**Domain:** Data Analytics / Statistics / Education

**Analysis Type:** Inferential Statistical Analysis

**Primary Technique:** One-Way ANOVA

**Additional Techniques:** Shapiro-Wilk, Levene's Test, Tukey HSD, Eta-Squared

**Output:** Statistical comparison and visualization of adult literacy rates across government education-spending tiers.
