# RiskLedger — Finance Risk & Comparison Analyzer

A single-file, browser-based tool for screening financial risk. Paste in numbers, get a ranked comparison with a risk score — no backend, no data leaves your browser.

**[Live demo](https://kanavvnegi.github.io/Finance-Risk-Analyzer/finance-risk-analyzer.html)**

## What it does

Three modules, each takes your inputs and gives a ranked comparison + 0–100 risk gauge:

- **Investments** — compare funds, stocks, FDs, ULIPs, bonds, etc. by expected return, cost, and volatility. Ranks by return-per-unit-of-risk.
- **Loans & Credit** — compare loan offers by EMI, total interest, total cost, and EMI-to-income strain.
- **Business Financials** — enter balance sheet / P&L figures and get current ratio, debt-to-equity, net margin, ROE, and interest coverage, rolled into a composite risk score.

## How to use it

1. Open `finance-risk-analyzer.html` in any browser (double-click the file, or visit the GitHub Pages link above).
2. Pick a tab (Investments / Loans / Business).
3. Fill in the form on the left and click "Add to comparison." Add two or more entries to see a ranked comparison.
4. The best-scoring entry is highlighted automatically.

No installation, no dependencies, no server required.

## How the risk scoring works

The tool uses simple, transparent rules-of-thumb rather than a black-box model:

| Module | Signals used | Example thresholds |
|---|---|---|
| Investments | volatility, expense ratio, lock-in | higher volatility/cost → higher risk score |
| Loans | EMI-to-income ratio | <30% low risk, 30–40% moderate, >40% high |
| Business | current ratio, debt/equity, net margin, ROE, interest coverage | e.g. current ratio >1.5 = healthy, <1 = high risk |

This is a first-pass screening tool, not financial advice. For high-stakes decisions, verify with a licensed advisor.

## Data & privacy

All calculations run client-side in JavaScript. Nothing is sent to a server, logged, or stored — the tool holds data in memory only for the current page session and resets on reload.

## Project structure

```
finance-risk-analyzer.html   # the entire app (HTML + CSS + JS, no build step)
README.md                    # this file
```

