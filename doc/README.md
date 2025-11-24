# Group Project – SMM270 Foundations of Econometrics

This repository contains material for the SMM270 *Foundations of Econometrics* group coursework.  
The official specification is the PDF in this directory:

- `Coursework_SMM270_2025-2026.pdf`  *(master document – always follow this if there is any discrepancy).*

This README summarises the brief and explains how this repo is organised for your work.

## Repository structure

- `doc/`
  - `Coursework_SMM270_2025-2026.pdf` – official coursework description.
  - `README.md` – this summary.
- `data/`
  - Excel files with the five core risk factors used throughout the coursework (daily frequency, around 2000–2025).
- `src/`
  - `question1.ipynb` – starting notebook for Question 1.
  - (Add further notebooks/scripts here for Questions 2–6 as you work.)

## Core dataset (five risk factors)

Across the questions you work with five key risk factors:

- An equity index in the **FTSE 100** or **S&P 500**.
- A **government bond yield** (U.S. or U.K.).
- A **corporate bond spread** (U.S. or U.K.).
- A **commodity price** (e.g. oil, gold, copper).
- A **major exchange rate** (e.g. GBP/USD, EUR/USD, USD/JPY).

Key features (see PDF for exact details):

- Main sample: **daily data** from *1 January 2000* to *30 August 2025* (approx.).
- Several questions require **aggregation to quarterly frequency**.
- All questions use (subsets of) the same five series.

## Software requirements

As stated in the coursework document:

- It is **compulsory** to use **OxMetrics 9** to execute the econometric applications.
- It is **advisable** to **replicate all empirical work in Python** (e.g. with `pandas`, `numpy`, `statsmodels`, `matplotlib`).
- Empirical results should be **reproducible** from your Excel data file and code (OxMetrics and/or Python).

AI-generated outputs that are not clearly grounded in your dataset are **not sufficient**; marks are awarded for:

- Data preparation and transformations.
- Correct numerical results.
- Contextual economic/financial analysis.
- Clear interpretation and professional reasoning as a quant.

## Coursework questions (summary)

Below is a high-level summary of each question.  
For exact wording, definitions, and any word limits, **always consult the PDF**.

### Question 1 – Descriptive analysis & stylised facts

Role: junior quant at a global asset management firm.

- Produce **diagnostic descriptive analysis** of the five core risk factors.
- Work mainly with **daily prices/levels and (log-)returns**.
- Conduct **exploratory analysis**: plots of levels and returns, basic checks for data issues.
- Compute **summary statistics** (mean, variance, skewness, kurtosis, correlations).
- Identify **stylised facts** in financial time series, such as:
  - Volatility clustering.
  - Fat tails / leptokurtosis.
  - Leverage/asymmetry effects.
  - Mean reversion in yields/spreads.
  - Persistence in volatility.
- Provide at least one **visual illustration** of stylised facts (e.g. returns vs squared returns, crisis-period volatility spikes).
- **Practitioner interpretation**: relate your evidence to major events (e.g. Global Financial Crisis, sovereign debt crisis, COVID‑19, commodity shocks) and explain why these properties matter for risk modelling and portfolio allocation.

### Question 2 – Unit roots in asset prices

Role: quant researcher checking whether key risk factors behave as random walks or are mean-reverting.

- **Aggregate each series to quarterly frequency.**
- Apply **unit root tests** (e.g. ADF) to:
  - Levels.
  - First differences/returns.
- Report **test statistics and conclusions** for each series.
- **Interpretation**:
  - Discuss implications for **market efficiency** (martingale/random walk vs mean reversion).
  - Highlight at least one asset whose behaviour is surprising, linking to economic/market events.
- **Decision-making**:
  - Advise whether each series should be modelled in **levels or returns** for forecasting and risk systems.
  - Discuss risks of **misclassifying stationarity** (e.g. treating a non-stationary process as stationary, or vice versa).
- **Professional communication**:
  - Draft a short **non‑technical executive summary** for the Chief Risk Officer explaining why stationarity matters and what the practical implications are for investment strategy (see PDF for the exact word limit).

### Question 3 – Cointegration in a multi‑asset portfolio

Role: quant analyst at a hedge fund trading multi‑asset portfolios.

- Use **quarterly data** to investigate **long‑run equilibrium (cointegrating) relationships** among the five series, typically with the **stock index as the dependent variable**.
- Perform **cointegration tests** (e.g. Engle–Granger and/or Johansen, as specified in the PDF).
- Identify any **cointegrating vectors** and interpret them economically.
- Assess whether the long‑run relations are **stable** over time (e.g. think about crises, regime changes).
- Link the findings to a potential **pairs/relative‑value trading strategy**:
  - Would you recommend the strategy based on your cointegration results?
  - Discuss risks such as structural breaks, transaction costs, model misspecification, regulatory changes.
- **Professional communication**:
  - Summarise your results in a short **“trader’s note”** (with a strict word limit, see PDF) that could be used to brief the trading desk.

### Question 4 – Spurious regression in multi‑asset analysis

Role: quant analyst assessing a questionable trading signal linking equity prices and bond yields.

- Select a **pair of trending series** from the five assets.
- Estimate a **naïve regression in levels** of one series on the other:
  - Include a constant and, if needed, a deterministic trend.
  - Report **R², t‑statistics**, and the **Durbin–Watson** statistic.
- Perform **diagnostics**:
  - Test regression residuals for a **unit root**.
  - Show how an apparently “significant” regression with a high R² can still be misleading.
- **Re‑specification**:
  - Re‑estimate the relationship in **first differences/returns** and compare results with the levels regression.
  - Comment on differences and why the original specification is problematic.
- **Practitioner reflection**:
  - Explain to the portfolio manager why the original regression is **spurious** and the risks of basing trading strategies on such relationships (false predictability, mis‑estimated hedge ratios, mispriced risk).
  - Emphasise the importance of **pre‑testing for unit roots and cointegration** in empirical research.
- **Professional communication**:
  - Write a short explanation (with a word limit given in the PDF) on why spurious regressions can generate false signals in cross‑asset trading.

### Question 5 – Granger causality & price discovery

Role: quantitative analyst on a multi‑asset trading desk.

- Investigate **Granger causality** and **price discovery** across the five assets.
- Use appropriate **VAR / Granger causality tests** (as specified in the PDF) to assess which markets **lead or lag** others in processing information.
- Interpret the direction of information flows and discuss implications for:
  - Forecasting accuracy.
  - Hedging and portfolio construction.
  - Intraday or high‑frequency trading strategies (where relevant).
- **Professional communication**:
  - Draft a one‑paragraph briefing for the **Head of Trading** summarising your main findings and their implications for price discovery across the five assets (see PDF for the exact word limit).

### Question 6 – Volatility modelling with GARCH (TBC)

Role: quantitative analyst on the risk management team of a global investment bank.

- Question 6 concerns **volatility dynamics and GARCH modelling** for the same set of assets.
- The PDF currently labels this question as **“TBC”** (to be confirmed): treat the PDF as the authoritative source for whether and how this part is assessed.
- Indicatively, you should expect to:
  - Work with **daily returns** for the five assets.
  - Specify and estimate appropriate **GARCH‑type models**.
  - Compare volatility dynamics across asset classes and relate them to risk management / VaR and stress‑testing frameworks.

## Deliverables & submission (summary)

The PDF contains the full submission instructions. Key points extracted from it:

- **Deadline**: a specific date and time in early November (see PDF for the exact deadline, which takes precedence over anything written here).
- **Submission platform**: upload via **Moodle**.
- Your submission must include:
  - **PDF report** containing your answers to the coursework questions, with a **maximum length of 8 pages**, including references and appendices.
  - A **zipped folder** containing:
    - An **Excel file** with the downloaded dataset and any transformations applied (sufficient to replicate your empirical results in OxMetrics).
    - Any supporting code (OxMetrics project/output files and Python notebooks/scripts) necessary to **replicate all reported results**.

## Working in this repository

- Keep all **data files** in `data/` (do not commit raw data downloaded from other sources unless permitted).
- Put your OxMetrics projects and Python code under `src/`, ideally one notebook/script per question (e.g. `question2.ipynb`, `question3.ipynb`, etc.).
- When the coursework is complete:
  - Generate the **PDF report** from your written answers and figures.
  - Export/prepare the **Excel file** summarising the dataset and transformations.
  - Zip the Excel file together with relevant OxMetrics and Python files for submission.

If you are unsure about any requirement, always **refer back to `Coursework_SMM270_2025-2026.pdf`** or ask the module leader/teaching team. This README is only a convenience summary and does **not** override the official coursework document.
