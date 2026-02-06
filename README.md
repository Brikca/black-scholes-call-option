# Black–Scholes Call Option Pricing

This project applies the **Black–Scholes model** to estimate **European call option prices** using **historical volatility** derived from daily stock prices obtained via Yahoo Finance.

The implementation is written in Python and evaluates multiple stocks under the same maturity period and risk-free rate for comparison.

---

## Assets Analyzed

- Apple Inc. (AAPL)
- Microsoft Corp. (MSFT)
- Tesla Inc. (TSLA)
- Amazon.com Inc. (AMZN)
- Alphabet Inc. (GOOGL)

---

## Model Parameters

| Parameter | Description |
|----------|------------|
| \(S_0\) | Latest closing stock price (Yahoo Finance) |
| \(K\) | Strike price |
| \(T\) | Time to maturity (90 days = 0.2466 years) |
| \(\sigma\) | Annualized historical volatility |
| \(r\) | Risk-free interest rate (BI7DRR = 4.75%) |
| \(C\) | Black–Scholes call option price |

---

## Method Summary

- Historical volatility is calculated from **1-year daily log returns**.
- Volatility is annualized using \(\sqrt{252}\).
- Call option prices are computed using the **Black–Scholes formula** (no dividend assumption).
- All stocks share the same \(r\) and \(T\) to ensure comparability.

---

## Key Results

| Stock | Volatility (σ) | Call Price (USD) |
|------|---------------|------------------|
| AAPL | 0.3241 | 14.5449 |
| MSFT | 0.2402 | 21.8720 |
| TSLA | 0.6756 | 53.4850 |
| AMZN | 0.3472 | 15.4792 |
| GOOGL | 0.3263 | 11.9797 |

---

## Insights

- All options are **out-of-the-money (S₀ < K)** at valuation time.
- Higher volatility leads to higher call option prices.
- TSLA shows the highest risk and option premium due to elevated volatility.
- Differences in option prices are driven mainly by **volatility and moneyness**, as \(r\) and \(T\) are constant.

---

## Tools & Libraries

- Python
- NumPy
- Pandas
- SciPy
- yFinance

---

## Author

**Brikca Kristal**  
Undergraduate Statistics Student – Universitas Gadjah Mada  
