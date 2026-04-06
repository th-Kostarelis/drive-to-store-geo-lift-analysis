# drive-to-store-geo-lift-analysis
Geo-lift analysis for a 'Drive to Store' campaign for a Scandinavian fashion brand.

This repository contains a comprehensive evaluation of a "Drive to Store" online advertising campaign for a Scandinavian fashion brand. The objective was to determine if additional online ad spend generated incremental in-store revenue across physical locations in Sweden.

# Project Overview
The initial stakeholder analysis suggested the campaign was a failure, showing a negative result in revenue growth. This investigation uncovers why those initial results were misleading and provides a corrected assessment using causal inference methods.

# Key Challenge: The "Mid-Season Sale" Anomaly
While treatment and control cities showed near-perfect parallel trends during the baseline period (Weeks 1–26), the test was contaminated in Week 31.
  1. Data Pollution: Control cities received a disproportionate influx of Mid-Season Sale ad spend (686,465 SEK vs. 376,800 SEK in treatment cities).
  2. Impact: This artificially inflated the control group's revenue, creating a flawed baseline that made the "Drive to Store" campaign appear to lose money.

# Methodology
To provide an honest assessment, I applied the following technical approach:
  1. Parallel Trends Validation: Confirmed group comparability using Weekly Revenue and Average Order Value (AOV) trends.
  2. Difference-in-Differences (DiD): Used both manual calculations and OLS Regression to estimate the treatment effect.
  3. Clean Window Isolation: Restricted the analysis to Weeks 27–30 to measure the campaign impact before the promotional "noise" began.
  4. ROAS Calculation: Estimated the incremental Return on Ad Spend for the clean window.

# Final Results
  1. Flawed Initial Lift: −325,346 SEK / week.
  2. Corrected Incremental Lift: +104,686 SEK / week.
  3. Implied ROAS: 0.73x.
  4. On a 4-week clean sample, the results are directional but inconclusive.

# Repository Structure
  1. analysis.ipynb: The complete Python technical workflow
  2. presentation.pdf: Stakeholder-ready slides (Technical and Non-Technical).
  3. ai_transcript.md: Full log of interactions with the AI assistant during the analysis.
  4. data/: Contains revenue.csv and spend.csv.

# Data Privacy & Security
To respect the confidentiality of the [Fashion Brand] business data and adhere to data security best practices, the raw revenue.csv and spend.csv files are not included in this public repository.

    Reproducibility: If you are a recruiter with access to the original source files, please place them in a folder named /data in the root directory to run the analysis.ipynb notebook without path errors.

    Security: A .gitignore file has been implemented to ensure sensitive datasets are not inadvertently committed to version control.
