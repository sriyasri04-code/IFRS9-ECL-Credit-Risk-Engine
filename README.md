# IFRS 9 Expected Credit Loss (ECL) Credit Risk Engine

Python-based quantitative credit-risk modelling project implementing a simplified IFRS 9 Expected Credit Loss framework.

## Overview

This project develops an end-to-end credit-risk modelling pipeline for a synthetic loan portfolio of 6,000 exposures.

The model covers:

- Probability of Default (PD)
- IFRS 9 Stage 1, Stage 2 and Stage 3 classification
- Loss Given Default (LGD)
- Exposure at Default (EAD)
- Expected Credit Loss (ECL)
- Forward-looking scenarios
- Portfolio stress testing
- Sector-level credit-risk analysis
- Model validation and risk reporting

The core ECL framework is:

**ECL = PD × LGD × EAD**

---

## Objective

The objective is to demonstrate how quantitative credit-risk concepts can be implemented in Python to estimate expected credit losses and assess portfolio risk under different credit conditions.

The project is designed as an educational credit-risk modelling prototype using synthetic data.

---

## Project Workflow

```text
Synthetic Loan Portfolio
          ↓
Data Preparation
          ↓
Probability of Default (PD)
          ↓
IFRS 9 Stage Classification
          ↓
      ┌───┴───┐
      ↓       ↓
     LGD     EAD
      └───┬───┘
          ↓
Expected Credit Loss
          ↓
Stress Testing
          ↓
Portfolio Risk Analysis
```

## Methodology
1. Probability of Default (PD)

A logistic regression-based credit-risk model is used to estimate borrower default probability.

Model performance is evaluated using:

ROC-AUC
Gini coefficient
KS statistic
Brier score
Precision
Recall
F1 score
2. IFRS 9 Staging

The project implements a simplified IFRS 9 staging framework.

Stage 1: 12-month ECL

Stage 2: Lifetime ECL following significant credit deterioration

Stage 3: Credit-impaired exposures with lifetime ECL treatment

3. Loss Given Default (LGD)

LGD is estimated using collateral and recovery-related assumptions.

The analysis examines LGD across loan characteristics and IFRS 9 stages.

4. Exposure at Default (EAD)

EAD represents expected exposure at the point of default.

The framework incorporates current exposure and expected utilization of undrawn credit.

EAD = Current Exposure + CCF × Undrawn Commitment

5. Expected Credit Loss (ECL)

The core calculation is:

ECL = PD × LGD × EAD

## Forward-Looking Scenarios

The model incorporates forward-looking scenarios to evaluate how changes in credit-risk assumptions affect expected losses.

## Stress Testing

The portfolio is evaluated under:

Scenario	ECL	Increase vs Base
Base	₹2,293,504	—
Mild Stress	₹3,053,544	+33.14%
Severe Stress	₹3,951,579	+72.29%
Extreme Stress	₹5,964,913	+160.08%

## Final Portfolio Results
Metric	Result
Portfolio Size	6,000 loans
Current Exposure	₹231.91M
Exposure at Default	₹243.51M
Expected Credit Loss	₹2.29M
Portfolio ECL Rate	0.94%
Default Rate	3.88%

## IFRS 9 Stage Analysis

The model evaluates:

Stage distribution
ECL by stage
Stage 3 credit-impaired exposures
Portfolio risk concentration

## Key Outputs

The outputs/ directory contains:

Final portfolio ECL summary
Stress-test summary
Stress-test results by IFRS 9 stage
Stress-test results by sector

## Technologies
Python
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn
Google Colab

## Repository Structure
IFRS9-ECL-Credit-Risk-Engine/
│
├── README.md
│
├── notebooks/
│   └── IFRS9_ECL_Credit_Risk_Engine.ipynb
│
└── outputs/
    ├── README.md
    ├── IFRS9_ECL_Final_Portfolio_Summary.csv
    ├── credit_stress_test_summary.csv
    ├── credit_stress_test_by_stage.csv
    └── credit_stress_test_by_sector.csv
    
## Model Limitations

This is an educational quantitative credit-risk prototype using synthetic data.

Key limitations include:

Synthetic loan portfolio
Simplified SICR assessment
Simplified LGD methodology
Synthetic EAD and CCF assumptions
Simplified Stage 3 treatment
Scenario-based rather than fully econometric macroeconomic modelling

Therefore, the results should not be interpreted as production banking or regulatory IFRS 9 provisions.

## Author

V.Sriyasri

B.Com | ACCA Student

Areas of interest:

Credit Risk
Quantitative Finance
Financial Modelling
Risk Analytics
Python for Finance
