# Daily Exchange Rates

This is a small **educational / learning project** built to explore GitHub
Actions automation. A scheduled workflow runs once a day, fetches current
exchange rates, and updates this README and `rates.json` automatically —
no server, no manual work required.

## Current rates

<!-- KUR-BASLA -->
**Last updated:** 2026-07-22 10:28 (Turkey time)

### Top 5 Global Currencies (vs USD)

| Currency | Code | Rate (per 1 USD) |
|----------|------|-------------------|
| US Dollar | USD | 1.0000 (base) |
| Euro | EUR | 0.8741 |
| British Pound | GBP | 0.7444 |
| Japanese Yen | JPY | 162.6900 |
| Chinese Yuan | CNY | 6.7650 |

### Turkish Lira (TRY) Cross Rates

| From | To TRY |
|------|--------|
| 1 USD | 47.1740 |
| 1 EUR | 53.9656 |
| 1 GBP | 63.3727 |
| 1 JPY | 0.2900 |
| 1 CNY | 6.9732 |
<!-- KUR-BITIR -->

## What this is for

- A hands-on example of GitHub Actions scheduled (cron) jobs: fetch → compute
  → commit, fully automated.
- A lightweight, free data source other personal projects can read from
  (instead of calling a third-party API directly on every request).

## How it works

The job in `.github/workflows/test.yml` runs automatically every morning
(Turkey time), and can also be triggered manually from the **Actions** tab:

1. Fetches current rates from the [Frankfurter API](https://frankfurter.dev),
2. Writes the raw response to `rates.json`,
3. Updates the tables below,
4. Commits the change automatically.

## Source and disclaimer

Rate data comes from the [Frankfurter API](https://frankfurter.dev), which is
based on **European Central Bank (ECB)** reference rates. As the ECB states,
these rates are **for informational purposes only** and should not be used
for actual transactions. Cross rates (e.g. EUR→TRY, GBP→TRY) are not
published directly by the ECB — they are **derived** in this repo from
USD-based rates (`USD→X ÷ USD→Y`).

This project is not financial advice, a product, or a service — it exists
purely for learning and personal use.

## Using this from another project

Raw data is available at: https://raw.githubusercontent.com/omerrmanav/daily-exchange-rates/main/rates.json





