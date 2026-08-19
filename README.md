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
          │
          ▼
Data Preparation
          │
          ▼
Probability of Default (PD)
          │
          ▼
IFRS 9 Stage Classification
          │
          ├──────────────┐
          ▼              ▼
         LGD             EAD
          │              │
          └──────┬───────┘
                 ▼
          Expected Credit Loss
                 │
        ┌────────┴────────┐
        ▼                 ▼
Forward-Looking      Stress Testing
Scenarios                 │
        │                 │
        └────────┬────────┘
                 ▼
        Portfolio Risk Analysis
