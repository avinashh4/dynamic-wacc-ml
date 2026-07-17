# dynamic-wacc-ml
a random forest and synthetic control framework to dynamically optimize wacc and model sovereign policy insulation for fixed peg infrastructure ppp's (ieo '26)

# Dynamic WACC ML Engine & Sovereign PPP Shield

This repository contains the quantitative financial engineering framework and econometric modeling developed for the International Economics Olympiad (IEO) 2026, designed to insulate large-scale public-private partnerships (PPPs) in fixed-exchange-rate economies from global macroeconomic shocks.

## Overview

Traditional infrastructure models rely on static discount rates ($6.0\%$), exposing long-term projects to massive capital destruction during global monetary tightening cycles. This project introduces a two-tier quantitative solution:
1. **Dynamic WACC Predictor:** A **Random Forest Regressor** trained to predict the project's Weighted Average Cost of Capital ($\text{WACC}$) under 10,000 simulated global interest rate environments.
2. **Econometric Appraisal:** A **Lasso-Regularized Synthetic Control Method (SCM)** evaluating macroeconomic policy impact against a weighted counterfactual baseline.

### Key Quantitative Discoveries
* **Fed Dominance:** The US Federal Funds Rate dictates **67.3%** of the project's WACC risk due to the domestic currency peg.
* **Risk Insulation:** Re-engineering the capital stack (40% Green Bonds, 35% Sovereign Equity, 25% Private Equity) combined with an automated sovereign debt-swap trigger permanently lowered the baseline hurdle rate to **7.40%** and achieved a **100% simulated project survival rate**.

## Repository Structure

* `notebooks/01_wacc_random_forest.ipynb`: Contains data preprocessing, Random Forest training ($R^2 = 0.965$), feature importance mapping, and Monte Carlo dynamic cash flow simulations.
* `notebooks/02_synthetic_control.ipynb`: Employs the Lasso-Regularized Synthetic Control approach (Doudchenko & Imbens, 2016) to establish the counterfactual macroeconomic baseline trend against donor economies.

## Execution in Google Colab

1. Open Google Colab.
2. Select the **GitHub** tab.
3. Paste this repository's URL into the search bar.
4. Click on either notebook file inside the `notebooks/` directory to review the pre-run execution blocks, compiled charts, and performance metrics instantly.

## 📊 Core Models & Equations

### Synthetic Control Objective Function
$$\min_{\mu, W} \sum_{t=1}^{T_0} \left( Y_{1t} - \mu - \sum_{j=2}^{J+1} w_j Y_{jt} \right)^2 + \lambda \sum_{j=2}^{J+1} \vert{}w_j\vert{}$$

### Automated Sovereign Debt-Swap Policy Rule
$$\text{If } \text{WACC}_{\text{ML}} \ge 8.5\% \Longrightarrow \text{Execute Automated Sovereign Debt-Swap}$$

## Team
* Developed by **Avinash** for the International Economics Olympiad (IEO) 2026.
