# Gold Price Analysis & Prediction 2015–2024

> **Machine learning models to analyze and forecast gold prices using 9 years of weekly data.**  
> Combining statistical models, trend analysis, and market insights into one complete project.

---

## Overview

This project analyzes gold price movements from 2015 to 2024 using weekly historical data, trains multiple forecasting models, and generates 7 comprehensive market insights with professional visualizations.

**Key Result:** Ridge Regression achieved **0.90% MAPE** on the test set (2024), and SARIMAX forecasts gold at **$2,536.76** by end of 2026.

---

## Project Structure

```
gold-price-analysis-and-prediction/
│
├── data/
│   ├── Gold Futures Historical Data.csv
│   ├── Crude Oil WTI Futures Historical Data.csv
│   └── US Dollar Index Futures Historical Data.csv
│
├── Philip - Gold Price Prediction.ipynb   ← Main notebook
│
├── gold_part1_charts.png                  ← Market Dynamics
├── gold_part2_charts.png                  ← Investment Analysis
├── gold_part3_charts.png                  ← Portfolio Strategy
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Dataset

| File | Description | Source |
|------|-------------|--------|
| Gold Futures Historical Data.csv | Weekly gold prices (USD/oz) | Investing.com |
| Crude Oil WTI Futures Historical Data.csv | Weekly WTI oil prices | Investing.com |
| US Dollar Index Futures Historical Data.csv | Weekly USD index | Investing.com |

- **Period:** January 2016 – December 2024
- **Frequency:** Weekly (W-FRI)
- **Total Observations:** 470 weeks

---

## Models

| Rank | Model | Test MAPE | Test RMSE | Test MAE | Best Use |
|------|-------|-----------|-----------|----------|----------|
| 🥇 #1 | **Ridge Regression** | **0.90%** | $26.94 | $21.86 | Short-term (1–12 weeks) |
| #2 | Prophet | 12.77% | N/A | N/A | Not recommended |
| 🥉 #3 | **SARIMAX** | **14.89%** | $446.90 | $381.53 | Long-term (2026 forecast) |
| #4 | HistGradientBoosting | 15.24% | $438.90 | $379.13 | Not recommended |

**Key finding:** Ridge Regression wins because gold in 2024 was driven by **momentum and lag patterns**, not external macro variables (oil/USD). Simpler models beat complex ones when external features are noisy.

---

## 2026 Price Forecast

Based on **SARIMAX** (best for long-term structural trends):

| Quarter | Mean Forecast | Range |
|---------|--------------|-------|
| Q1 2026 | $2,580 | $2,541 – $2,626 |
| Q2 2026 | $2,570 | $2,543 – $2,599 |
| Q3 2026 | $2,564 | $2,537 – $2,592 |
| Q4 2026 | $2,537 | $2,516 – $2,563 |

> **Final Forecast (End-2026): $2,536.76**  
> Confidence: Medium (~14.89% MAPE) | Implied change vs 2024: -3.1%

---

## 7 Market Insights

### Part 1 — Market Dynamics
| Insight | Finding |
|---------|---------|
| **[A] 10-Year Journey** | Gold +147% over 9 years (10.6% annually). From $1,060 → $2,618. |
| **[B] 2024 Rally** | +27.7% in a single year, driven by central banks — NOT oil or USD. |
| **[D] Gold's Changing Role** | Evolved from inflation hedge → de-dollarization asset. Gold-USD correlation weakened from -0.44 → -0.20. |

### Part 2 — Investment Analysis
| Insight | Finding |
|---------|---------|
| **[F] Seasonal Patterns** | No consistent monthly pattern exists. "Buy in September" is statistically unsupported. |
| **[H] Real Returns** | +120% real gain after inflation. Beats Treasury bonds by 5x, destroys cash (-22% real). |
| **[I] Central Bank Buying** | 400+ tons purchased in 2024 (2x historical average). Structural shift, not cyclical. |

### Part 3 — Portfolio Strategy
| Insight | Finding |
|---------|---------|
| **[J] Portfolio Strategy** | Gold ranks 2nd in returns (after stocks). Optimal allocation: **10–20%** of diversified portfolio. |

---

## Visualizations

**Part 1 — Market Dynamics** (`gold_part1_charts.png`)
- Gold's 10-year price journey
- Yearly return bar chart
- 2024 rally detail
- Phase evolution analysis

**Part 2 — Investment Analysis** (`gold_part2_charts.png`)
- Monthly seasonality (debunked)
- Real return comparison vs other assets
- Annualized returns comparison
- Central bank buying trend

**Part 3 — Portfolio Strategy** (`gold_part3_charts.png`)
- Risk-return scatter (all assets)
- Total returns comparison
- Volatility comparison
- Portfolio allocation by investor type

---

## Portfolio Recommendations

| Profile | Gold | Bonds | Stocks | Other |
|---------|------|-------|--------|-------|
| Conservative | 30% | 50% | 20% | — |
| **Moderate** ⭐ | **20%** | **30%** | **40%** | **10%** |
| Aggressive | 10% | 15% | 70% | 5% |

> **Recommended for most investors: Moderate allocation.**  
> Balances growth (stocks), stability (bonds), and protection (gold).

---

## Installation

```bash
# Clone the repository
git clone https://github.com/matthewphilip-quantlab/Gold-Price-Analysis-and-Prediction.git
cd gold-price-analysis-and-prediction

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

---

## Requirements

```
numpy>=1.24.0
pandas>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
scikit-learn>=1.3.0
statsmodels>=0.14.0
prophet>=1.1.0
scipy>=1.10.0
jupyter>=1.0.0
ipython>=8.0.0
```

---

## Key Takeaways

1. **Gold is a proven long-term wealth creator** — +147% over 9 years, beating inflation by 120%+
2. **2024 was a structural shift** — central banks replaced speculators as the primary driver
3. **Old correlations are breaking down** — oil has zero predictive power; USD relationship weakening
4. **Seasonal trading is a myth** — no statistically significant monthly pattern exists
5. **Simple beats complex** — Ridge (0.90% MAPE) outperforms Prophet (12.77%) because momentum matters more than macro
6. **Gold belongs in every portfolio** — 10–20% allocation improves risk-adjusted returns for all investor types

---


## 👤 Author

**Philip Matthew**

- GitHub: [@matthewphilip-quantlab](https://github.com/matthewphilip-quantlab)
- LinkedIn: [Philip Matthew](https://www.linkedin.com/in/philip-matthew-514703341/)
- Email: matthewphilip788@gmail.com

---

*Data sourced from Investing.com. This project is for educational purposes only and does not constitute financial advice.*
