# Machine Learning and Policy Shocks: Predicting Stock Market Reactions to the 2025 U.S. Steel and Aluminum Tariffs

This repository contains my Computational Finance thesis submitted at **LUISS Guido Carli University** for the **Management and Computer Science** degree program. The project studies whether historical market reactions to the **2018 U.S. steel and aluminum tariffs** can help predict stock return behavior around the **2025 tariff reintroduction**. fileciteturn0file0

## Project Overview

The research combines **event-study logic**, **CAPM-based abnormal return analysis**, and a **pooled OLS panel regression framework** with a **train-test split** approach. The training set is built on stock reactions to the 2018 tariff shock, while the test set evaluates model performance on 2025 data. fileciteturn0file0

The objective is not to forecast long-term stock prices, but rather to assess how selected firms reacted in the days surrounding a major policy shock and whether similar historical patterns provide predictive value for later events. fileciteturn0file0

## Research Question

Can historical stock market reactions to the 2018 U.S. steel and aluminum tariffs help predict short-term stock return behavior following the 2025 reintroduction of those tariffs?

## Methodology

The workflow in this project includes:

- Collection of historical stock price data, market index data, and risk-free rate data
- Computation of daily log returns and cumulative returns
- Visual analysis of stock performance around key tariff-related dates
- CAPM beta estimation for each selected stock
- Calculation of abnormal returns and cumulative abnormal returns around event windows
- One-sample t-tests to assess whether the 2018 tariff events produced statistically significant abnormal returns
- Construction of a pooled OLS panel regression model using market return, rolling volatility, and an event dummy as predictors
- Application of a train-test split framework, using 2018 data for training and 2025 data for out-of-sample testing fileciteturn0file0

## Selected Companies

The thesis focuses on a set of firms exposed to tariffs either directly or through input-cost sensitivity, including:

- Alcoa (`AA`)
- Caterpillar (`CAT`)
- Campbell Soup (`CPB`)
- Ford (`F`)
- General Motors (`GM`)
- Hammond Power Solutions (`HPS-A.TO`)
- Grupo Simec (`SIM`)
- Tesla (`TSLA`) fileciteturn0file0

## Key Findings

- The **March 1, 2018 tariff announcement** was the only one of the five major event dates that produced statistically significant abnormal returns in the sample. fileciteturn0file0
- In the training set, the pooled OLS model achieved an **R-squared of 0.118**, with **market return** and the **event dummy** emerging as statistically significant predictors. fileciteturn0file0
- In the 2025 test period, the model captured some directional patterns in returns, but predictive performance remained modest, which is consistent with the noisy nature of daily equity returns. The test-period **R-squared was approximately 0.052**. fileciteturn0file0
- The main contribution of the project is not precise short-term price forecasting, but rather a structured finance and econometrics framework for analyzing how policy shocks transmit into market reactions. fileciteturn0file0

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

## Files Included

- **Thesis PDF**: final submitted thesis document
- **Notebook**: research workflow used for data analysis, modeling, and visualization
- **Raw CSV files**: supporting data snapshots used in the project

## Tools and Libraries

- Python
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- statsmodels
- scipy
- scikit-learn
- yfinance
- linearmodels
- CAPM / event-study methods
- panel regression
- machine learning train-test split

## Reproducibility Note

This repository is intended as an **academic and portfolio project**.

The notebook reflects the workflow used in the thesis and includes rendered outputs and visualizations. Some sections rely on live downloads from Yahoo Finance through `yfinance`. Because Yahoo Finance may occasionally impose temporary rate limits, rerunning the notebook from top to bottom may not always succeed immediately without adjustment.

For that reason, this repository should be interpreted as:

- a transparent record of the analytical workflow
- a portfolio example of finance, econometrics, and Python-based market analysis
- a thesis project with included data snapshots and rendered notebook outputs

## Why This Project Matters

This project sits at the intersection of **finance**, **econometrics**, and **machine learning-style validation**. It shows how historical policy shocks can be used to build structured frameworks for analyzing market sensitivity, with practical relevance for:

- investors
- policymakers
- corporates exposed to trade policy changes
- finance professionals interested in event-driven market behavior fileciteturn0file0

## Author

**Santiago Cuesta**  
LUISS Guido Carli University  
Degree Program in Management and Computer Science  
Course: Computational Finance  
Supervisor: Prof. Nicola Borri  
Academic Year: 2024/2025 fileciteturn0file0

## License

This repository is shared for academic and portfolio purposes.
