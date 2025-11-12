Mutual Fund Performance Analysis and Ranking Project

Project Overview

This initiative establishes a robust, data-driven framework designed to move beyond traditional, return-centric evaluations of mutual funds. Conventional analysis often focuses narrowly on historical returns, failing to account for the level of risk incurred or the cost to the investor.

This project addresses that gap by creating a Composite Score—a singular, objective metric that holistically evaluates fund quality. By incorporating metrics spanning risk-adjusted returns (e.g., Sharpe, Sortino), volatility, and cost efficiency, the goal is to provide a clear, unbiased ranking. This enables investors to confidently identify truly high-performing schemes that demonstrate superior capital preservation and value creation over time.

Key Components and Files

The project follows a standard Extract, Transform, Load (ETL) structure, broken down into Analysis, Data Output, and Interactive Visualization.

File Name

Component

Description

Mutual Fund Analysis (1).ipynb

Analysis Engine (Python)

This Jupyter Notebook is the computational heart of the project. It handles data ingestion, cleaning, and the critical step of normalization. It uses the Pandas library to calculate the final Composite Score for each fund and generate the quantitative Rank.

top_30_mutual_funds.xlsx - Sheet1.csv

Processed Data Output

This file represents the final, actionable data. It contains the original fund metrics, augmented with the calculated composite_score and the resultant rank for the top 30 funds, ready for consumption by other systems or visualization tools.

Mutual Fund Dashboard.pbix

Interactive Visualization (Power BI)

This Power BI file offers an accessible, user-friendly interface for exploring the analytical results. It allows users to apply interactive filters, visualize performance trends, and compare the ranked mutual funds based on sub-category or fund manager.

Methodology: Composite Scoring and Normalization

The fund ranking is determined by the Composite Score, which is calculated through a critical two-step process: normalization and aggregation.

1. Metric Selection and Weighting

The analysis intentionally prioritizes metrics that indicate better risk-adjusted performance and lower costs.

Metric Type

Key Indicators Included

Weighting Logic

Risk-Adjusted Returns

Sharpe Ratio, Alpha, Sortino Ratio

Positively Weighted: Higher values indicate superior returns for the risk taken.

Absolute Performance

Returns (1-year, 3-year, 5-year)

Positively Weighted: Ensures funds with strong absolute growth are recognized.

Risk and Cost

Standard Deviation (SD), Beta, Expense Ratio

Negatively Weighted: Lower values are desired, indicating lower volatility and better cost efficiency.

2. Normalization Process

Due to the vastly different scales of the raw metrics (e.g., a 5-year return of 20% vs. an Expense Ratio of 0.5%), a Min-Max Normalization technique is applied to every indicator. This standardizes all values into a comparable range (typically 0 to 1). This crucial step ensures that the final Composite Score is an unbiased reflection of a fund's overall quality, rewarding it equally for high returns and efficient risk management without any single metric disproportionately dominating the result.

Technologies Used

Data Analysis & Processing: Python (Jupyter Notebook, Pandas)

Data Storage: CSV Format (for interoperability and lightweight data exchange)

Visualization: Microsoft Power BI (for rich, interactive reporting)
