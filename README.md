# Machine Learning and Policy Shocks: Predicting Stock Market Reactions to the 2025 U.S. Steel and Aluminum Tariffs

Undergraduate thesis completed at **LUISS Guido Carli University** for the **Computational Finance** course in the **Management and Computer Science** degree program.

## Overview

This project studies whether historical market reactions to major trade-policy shocks can help predict the short-term stock return impact of similar future events.

The thesis uses the 2018 U.S. steel and aluminum tariff announcements as the training context and applies the learned framework to evaluate stock return reactions around the 2025 reintroduction of those tariffs.

The objective was not to forecast long-term stock prices, but to model how selected companies exposed to steel, aluminum, and related supply-chain effects responded to a policy shock.

## Research Question

Can historical stock market reactions to the 2018 U.S. steel and aluminum tariffs help predict the direction and short-term return impact of the 2025 tariff reintroduction?

## Methodology

The workflow combines finance and econometrics techniques with a machine-learning-style validation structure:

- CAPM-based event analysis
- cumulative abnormal return (CAR) testing
- one-sample t-tests for event significance
- pooled OLS panel regression
- train-test split using 2018 data as training context and 2025 data as test context

### Main variables used in the panel model

- stock return
- market return
- rolling 20-day volatility
- event dummy for the tariff announcement window

## Companies Included

The analysis focuses on a selected set of companies chosen for their exposure to steel, aluminum, manufacturing inputs, or related supply-chain effects:

- Alcoa (`AA`)
- Caterpillar (`CAT`)
- Campbell Soup (`CPB`)
- Ford (`F`)
- General Motors (`GM`)
- Hammond Power Solutions (`HPS-A.TO`)
- Grupo Simec (`SIM`)
- Tesla (`TSLA`)

## Main Findings

- The initial 2018 tariff announcement behaved like a statistically meaningful market shock in the selected sample.
- The panel regression captured part of the return variation during the training period.
- Out-of-sample performance for 2025 was modest in exact value prediction, which is expected given the noise and volatility of daily stock returns.
- Even with limited explanatory power, the framework was useful for identifying directional patterns and illustrating how policy shocks can affect different firms in different ways.

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── .gitignore
├── thesis/
│   └── Santiago_Cuesta_Thesis_CompFi.pdf
├── notebooks/
│   └── predictive_stock_price_us_tariff.ipynb
└── data/
    └── raw/
        ├── stock_prices_2018_2019.csv
        ├── price_data_2025.csv
        └── market_data_2025.csv
```

## Files

### `thesis/`
Contains the final submitted thesis PDF.

### `notebooks/`
Contains the main Jupyter notebook used for the analysis and visualizations.

### `data/raw/`
Contains the CSV snapshots used in the workflow.

## Tech Stack

- Python
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- scipy
- statsmodels
- scikit-learn
- yfinance
- linearmodels

## Reproducibility Note

This repository is intended primarily as an academic and portfolio project.

The notebook reflects the research workflow and includes the main visual outputs. Some steps rely on live Yahoo Finance downloads through `yfinance`, which may occasionally fail because of temporary rate limits or API-side restrictions.

Included CSV snapshots support the core workflow, but a full rerun may still require refreshing or adjusting some data download steps.

## Why this project matters

This work sits at the intersection of:

- computational finance
- econometrics
- market reaction analysis
- policy-event modeling
- applied machine learning in finance

It was designed to show how historical financial data can be used to study the market impact of major policy shocks in a structured, interpretable way.

## Author

**Santiago Cuesta**

LUISS Guido Carli University  
BSc in Management and Computer Science

## Thesis Title

**Machine Learning and Policy Shocks: Predicting Stock Market Reactions to the 2025 U.S. Steel and Aluminum Tariffs**
