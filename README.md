# 6-Lens Market Analysis & Investment Decision Studio

An interactive, multi-lens quantitative decision studio for testing sector rotation, equity factor weighting, event-driven volatility sizing, options payoff structuring, housing/macro forecasts, and portfolio correlation networks in real time.

## Live Market & Macro Calibration (As of November 25, 2026)

All built-in baseline datasets and default model levers reflect late-November 2026 market and macroeconomic readings:

| Domain | Source / Series | Nov 2026 Baseline Value |
| :--- | :--- | :--- |
| **Equities Universe** | 20 S&P 500 Leaders (`AAPL`, `MSFT`, `GOOGL`, `AMZN`, `TSLA`, `NFLX`, `JPM`, `BAC`, `JNJ`, `PFE`, `KO`, `PEP`, `WMT`, `HD`, `NKE`, `MCD`, `SBUX`, `DIS`, `XOM`, `CVX`) | Live spot prices (e.g., `AAPL` `$355.10`, `MSFT` `$494.20`, `JPM` `$322.40`, `XOM` `$158.08`), TTM P/E, dividend yields, 5Y betas, and annualized volatility |
| **Risk-Free Benchmark** | 3-Month U.S. Treasury Yield | **4.30%** |
| **30Y Fixed Mortgage Rate** | FRED `MORTGAGE30US` (Week ending Nov 25, 2026) | **7.21%** |
| **New Housing Supply** | FRED `MSACSR` (Oct 2026; Sep 2026 = 8.4 mos.) | **8.0 months** |
| **Real Disposable Income / Cap** | FRED `A229RX0` (Q3 2026 SAAR, chained 2017 $) | **$53,639** |
| **Unemployment Rate** | FRED `UNRATE` (Oct 2026 BLS release) | **4.1%** |
| **Consumer Sentiment** | FRED `UMCSENT` (Nov 2026 UMich index) | **51.5** |
| **Case-Shiller Home Price Index** | FRED `CSUSHPISA` (Sep 2026 index `334.82`) | **+0.20% SA MoM** (`+2.1%` YoY) |
| **Volatility Regime** | Trailing vs 30D Volatility (`XLK`, `XLE`, `SPY`, `XLU`) | Tech-led volatility spike (`XLK` `2.24%` daily shock vol; elevated VIX environment) |

## The 6 Analytical Lenses + Core Capabilities

1. **Lens 1 — Macro & Sector Rotation:** Adjust cycle regime (`Bull` / `Neutral` / `Bear`), 30Y rate, sentiment, unemployment, and defensive low-beta overlay to re-rank all 8 sectors dynamically.
2. **Lens 2 — Multi-Factor Stock Screener:** Tune Momentum, Value, Low-Volatility, and Growth/ROE weights plus risk-free hurdle rate and beta/volatility filters with a live Risk-Return Frontier scatter chart.
3. **Lens 3 — Event Volatility Shock Sizer:** Model Pre-Event, Initial Shock, and Recovery windows with shock stress multipliers and daily risk budgets to compute inverse-volatility Risk-Parity weights and position caps.
4. **Lens 4 — Black-Scholes Options Lab:** Model 7 multi-leg structures (`Bull Call Spread`, `Bear Put Spread`, `Iron Condor`, `Butterfly Spread`, `Collar`, `Long Straddle`, `Long Strangle`) with **IV Skew**, **Probability of Profit (`PoP`)**, **T+0 Black-Scholes curve**, Net Greeks, and a **7d / 30d / 90d Term Structure Comparison**.
5. **Lens 5 — FRED Macro & Housing Regression:** Test supply, mortgage, income, unemployment, and sentiment scenarios against 44 historical monthly periods with **95% Newey-West confidence intervals** and optional **AR(1) persistence (`rho = 0.83`)**.
6. **Lens 6 — Network Correlation, Structural Defectors & Custom Portfolio Basket:** Inspect empirical correlation clusters vs official GICS classifications, highlight structural defectors, and assemble custom equal-weight baskets to evaluate **Portfolio Volatility**, **Diversification Ratio**, **Average Pairwise Correlation**, and **Sharpe Ratio**.

### Cross-Lens Workflow Features
- **Investment Conviction Scorecard:** Always-visible top bar summarizing the winning sector, #1 stock pick, options PoP & shock P&L, FRED HPI forecast, and custom basket Sharpe—click any pill to jump straight to that lens.
- **Zero-Backend CSV Uploader:** Load your own wide/long daily equity price CSVs (computes empirical volatility, RSI, beta, and pairwise correlation matrix) or custom FRED monthly CSVs in-browser.
- **Scenario A vs B Snapshots & 1-Click Markdown Memo:** Pin a baseline scenario (`Pin Snapshot A`), adjust sliders to test a stress case, review live metric deltas, and export a formatted Markdown Investment Decision Memo (`Copy Markdown` or `Download .md`).

## Running Locally & Deploying for Submission

The standalone application (`index.html`) is **100% self-contained** with zero external network dependencies.

- **Run locally:** Open `index.html` directly in any modern browser, or serve locally:
  ```powershell
  npx --yes http-server . -p 8080
  ```
- **Shareable URL (Static Hosting):** Upload `index.html` cleanly to **GitHub Pages**, **Netlify Drop**, **Cloudflare Pages**, or **Vercel** to generate a public HTTPS submission link.

## Profile Submission Kit (Ready to Paste)

- **Project Title:** `6-Lens Market Analysis & Investment Decision Studio`
- **Cover Preview Image:** `cover-preview.png` (`1500x1000`, exact 3:2 ratio)
- **Description (468 / 500 chars):**
> Built a 6-lens Market Analysis Studio calibrated to late-Nov 2026 data (20 equities, 4.30% Rf, 7.21% mortgage, 51.5 sentiment) with live sliders, CSV uploads, and A-vs-B snapshots. Tinkering revealed cross-cluster diversification (MSFT, JPM, KO, XOM) sharply cuts correlation vs naive growth baskets, while XLK vol spikes shift Risk Parity toward SPY/XLU. Proud of unifying Black-Scholes PoP, FRED confidence bands, and instant Markdown memos in a zero-backend studio.

## Ready-to-Use Submission Summary

> **Scenario & Goal:** Evaluating sector allocation, single-stock selection, hedging structures, and portfolio diversification tradeoffs in late-November 2026 amid high 30-year mortgage rates (`7.21%`), depressed consumer sentiment (`51.5`), and a tech-led volatility spike.
>
> **Interactive Levers:** Dynamic cycle toggles, macro sliders (yields, sentiment, unemployment, housing supply), factor weights, IV & IV-skew sliders, correlation thresholds (`r > tau`), and custom portfolio basket builders.
>
> **Outcome:** Every slider, preset, CSV upload, and toggle updates all 6 charts, tables, the Cross-Lens Conviction Scorecard, Scenario A-vs-B deltas, and the exportable Investment Decision Memo immediately in real time.
