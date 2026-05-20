# zillmer-hull-white-reserve
# Term Life Insurance Premium Reserve Calculation using Zillmer Method & Hull-White Interest Rate Model

## 1. Project Overview
This repository contains the Python implementation of my undergraduate thesis project. The project focuses on determining the premium reserves for term life insurance by integrating stochastic interest rates with modified reserve calculations. 

Traditional actuarial models often assume a constant interest rate. To achieve a more realistic valuation, this project applies the **Hull-White One-Factor Model** to capture interest rate volatility. Additionally, the **Zillmer Method** is implemented to calculate the premium reserves, which allows for the amortization of initial acquisition costs over the policy term, preventing large negative reserves in the early years of the policy.

## 2. Methodology
The computational logic in this repository is built upon two main mathematical frameworks:

* **Stochastic Interest Rate (Hull-White Model):** The interest rate paths are simulated using the Hull-White model. The model parameters (mean reversion speed and volatility) are calibrated using **Ordinary Least Squares (OLS) estimation** based on historical monthly interest rate data from Bank Indonesia (BI).
* **Actuarial Valuation (Zillmer Method):** Premium reserves are calculated by incorporating a Zillmer quota. The algorithm utilizes mortality tables (integrated via CSV) to calculate survival probabilities and expected present values, adjusting the net premium reserve for acquisition expenses.
