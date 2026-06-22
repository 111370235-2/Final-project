# Adolescent Emotional Health and Substance Use Analysis

## Student Information

**Name:** 林家昕

**Student ID:** 111370235

---

## Project Repository

https://github.com/111370235-2/Final-project.git
---

## Presentation Video

https://youtu.be/uc-VlgEfiAM?si=2BPGrxIV54CtRUu-

---

## Research Question

Does experiencing prolonged feelings of sadness or hopelessness increase the probability of current cigarette use among adolescents?

---

## Project Overview

This project investigates the relationship between emotional distress and cigarette smoking among adolescents using data from the 2007 Youth Risk Behavior Surveillance System (YRBS).

A Linear Probability Model (OLS Regression) was applied to evaluate whether students who reported prolonged feelings of sadness or hopelessness were more likely to be current cigarette smokers.

In addition to the primary analysis, exploratory analyses by biological sex and a sex-by-sadness interaction analysis were conducted to examine potential demographic patterns and explore whether biological sex may influence the observed relationship between emotional distress and smoking behavior.

---

## Dataset

- **Source:** Youth Risk Behavior Surveillance System (YRBS) 2007 Baseline Survey
- **Valid Sample Size:** 13,174 observations
- **Study Design:** Cross-sectional observational study

---

## Variables

### Dependent Variable (Y)

**Smoke_recoded**

- 1 = Current Smoker
- 0 = Non-Smoker

### Independent Variable (X)

**Sad_recoded**

- 1 = Felt Sad or Hopeless
- 0 = Did Not Feel Sad or Hopeless

### Exploratory Variable

**Sex_recoded**

- 1 = Male
- 0 = Female

This variable was used for exploratory subgroup and interaction analyses.

---

## Statistical Method

### Linear Probability Model (OLS Regression)

```text
Smoke_recoded = β₀ + β₁(Sad_recoded)
```

### Hypotheses

**Null Hypothesis (H₀)**

```text
β₁ = 0
```

There is no association between sadness and smoking probability.

**Alternative Hypothesis (H₁)**

```text
β₁ ≠ 0
```

There is an association between sadness and smoking probability.

---

## Project Structure

```text
project/
│
├── data/
│   ├── raw/
│   │   └── YRBS_2007.csv
│   │
│   └── processed/
│       └── cleaned_data.csv
│
├── notebooks/
│   └── final.ipynb
│
├── outputs/
│   └── figures/
│       ├── stacked_bar_perfect.png
│       ├── dumbbell_plot_perfect.png
│       ├── relative_risk_bar.png
│       ├── sex_exploration_bar.png
│       ├── interaction_sex_sad_bar.png
│       └── regression_ci_plot.png
│
└── README.md
```

---

## Key Findings

### Main Findings

| Group | Smoking Prevalence |
|---------|---------|
| Not Sad | 16.18% |
| Sad or Hopeless | 27.57% |

- Raw Difference: 11.39 percentage points
- Relative Risk: 1.70

Students who reported sadness or hopelessness exhibited approximately 1.70 times the smoking prevalence of students who did not report such feelings.

---

### Exploratory Analysis by Sex

| Sex | Smoking Prevalence |
|---------|---------|
| Female | 21.64% |
| Male | 17.43% |

Female students exhibited a higher overall smoking prevalence than male students.

---

### Interaction Analysis

| Emotional Status | Female | Male |
|---------|---------|---------|
| Not Sad | 19.2% | 12.6% |
| Sad | 30.5% | 25.9% |

The increase in smoking prevalence from the "Not Sad" group to the "Sad" group was observed among both female and male students.

This suggests that the positive association between emotional distress and smoking behavior is present across both sex groups.

---

### Regression Results

| Metric | Value |
|---------|---------|
| Intercept (β₀) | 0.1618 |
| Slope (β₁) | 0.1143 |
| p-value | < 0.001 |
| 95% Confidence Interval | [0.100, 0.129] |

Interpretation:

The regression model estimates that students reporting sadness or hopelessness have an 11.43 percentage-point higher probability of being current cigarette smokers compared with students who do not report such feelings.

Because the confidence interval does not include zero and the p-value is below 0.001, the null hypothesis is rejected.

---

## Generated Visualizations

### 100% Stacked Bar Chart of Smoking Status by Sadness

- File: `stacked_bar_perfect.png`

### Dumbbell Plot of Smoking Proportions

- File: `dumbbell_plot_perfect.png`

### Relative Risk Comparison

- File: `relative_risk_bar.png`

### Exploratory Analysis by Sex

- File: `sex_exploration_bar.png`

### Interaction Analysis (Sex × Sadness)

- File: `interaction_sex_sad_bar.png`

### 95% Confidence Interval Plot

- File: `regression_ci_plot.png`

---

## Limitations

- This study focuses on the association between sadness and smoking behavior and does not establish causality.
- Because the data are cross-sectional, temporal ordering between emotional distress and smoking behavior cannot be determined.
- Other variables such as age, grade, alcohol use, peer influence, and family environment were not included in the primary regression model.
- Potential confounding variables may partially explain the observed relationship.

---

## Future Research

Future studies may incorporate additional demographic, behavioral, and environmental variables into a multiple regression framework to determine whether the observed association remains significant after controlling for potential confounding factors.

Potential variables include:

- Age
- Grade level
- Alcohol use
- Drug use
- Peer influence
- Family environment
- Socioeconomic factors

---

## Conclusion

This study found a statistically significant positive association between sadness or hopelessness and current cigarette use among adolescents.

Students reporting sadness or hopelessness exhibited a smoking prevalence of 27.57%, compared with 16.18% among students who did not report such feelings.

The Linear Probability Model estimated an 11.43 percentage-point increase in smoking probability associated with emotional distress, with a 95% confidence interval of [0.100, 0.129] and a p-value below 0.001.

Exploratory analyses further showed that the positive association between sadness and smoking behavior was observed in both female and male students.

Although a significant association was identified, the results should be interpreted as correlational rather than causal. Additional studies incorporating more explanatory variables are recommended to better understand the mechanisms linking emotional health and adolescent smoking behavior.
