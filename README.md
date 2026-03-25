# Quantitative Market Regimes

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/status-70%25%20complete-yellow?style=for-the-badge"/>
</p>

Quantitative study of market regimes, streaks, and conditional probabilities applied to **GGAL** (Grupo Financiero Galicia) — using Hidden Markov Models (HMM) for regime detection and probabilistic analysis of price behavior across the last 10 years of Argentine market history.

> Although this project focuses on GGAL, the methodology is fully transferable to any financial asset.

---

## Overview

Financial markets alternate between distinct behavioral states — trending up, trending down, or moving sideways. Identifying which regime the market is currently in, and understanding the statistical properties of each regime, is fundamental to any quantitative trading or risk management strategy.

This project uses **Hidden Markov Models (HMM)** to detect and classify market regimes from price data alone, then builds a probabilistic framework around streaks, transitions, and conditional behavior within each regime — including the critical distinction between **trending markets** (where momentum strategies work) and **mean-reverting markets** (where contrarian strategies outperform).

---

## What this project does

**Regime detection**
- Applies HMM to classify market states: bull, bear, and lateral
- Extends the model to identify **trending vs. mean-reverting** regimes — enabling strategy calibration based on current market dynamics
- Visualizes regime states over time with annotated charts

**Streak analysis**
- Studies consecutive positive and negative return sequences under multiple criteria
- Calculates streak length distributions within each regime
- Identifies historically significant streak patterns

**Conditional probability analysis**
- Given the current regime, what is the probability of the next N days being positive?
- Given a streak of N days in one direction, what is the probability of continuation vs. reversal?
- State transition matrix — probability of moving from one regime to another

**Quantitative metrics**
- Duration statistics for each regime
- Return distributions by regime
- Volatility characteristics within each market state

---

## Roadmap

- **Volume integration** — incorporate volume data to validate and refine regime signals
- **Regime-conditional options analysis** — connect with [Options Expiration Analysis](https://github.com/JonatanSiracusa/options-expiration-analysis) to study how regime affects expiration behavior
- **Real-time regime classification** — adapt the model for live market monitoring
- **Multi-asset extension** — apply the same framework to other Argentine and international assets

---

## Key context: why GGAL over the last 10 years?

The dataset covers the last 10 years of Argentine market history — a period that includes the **2018 currency crisis**, the **2019 PASO election shock**, and subsequent macro instability episodes. Each of these events generated extreme regime transitions — making GGAL an exceptionally rich laboratory for regime detection under real-world stress conditions.

---

## Results & outputs

- 📊 **Interactive charts** (Plotly):
  - Price series with regime classification overlaid
  - Regime transition timeline
  - Streak length distributions by regime
  - Conditional probability heatmaps
- 📋 **Summary tables:**
  - Regime duration and frequency statistics
  - State transition probability matrix
  - Streak counts and conditional probabilities

---

## Tech stack

| Tool | Purpose |
|---|---|
| `Python` | Core language |
| `hmmlearn` | Hidden Markov Model estimation |
| `pandas` / `NumPy` | Data manipulation and numerical computation |
| `statsmodels` | Statistical analysis |
| `scipy` | Probability distributions |
| `yfinance` | Historical price data |
| `Plotly` | Interactive visualizations |
| `Jupyter Notebook` | Development and presentation environment |

---

## Project structure

```
quantitative-market-regimes/
│
├── notebooks/
│   └── market_regimes_streaks.ipynb  # Main analysis notebook
│
├── src/
│   └── (core Python modules and helper functions)
│
├── data/
│   └── (auto-downloaded via yfinance)
│
├── images/
│   └── (exported chart previews)
│
└── README.md
```

---

## How to run

```bash
# Clone the repository
git clone https://github.com/JonatanSiracusa/quantitative-market-regimes.git
cd quantitative-market-regimes

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook notebooks/market_regimes_streaks.ipynb
```

---

## Related projects

This project is part of a broader quantitative analysis suite on GGAL:

- [Market Risk — VaR & GARCH](https://github.com/JonatanSiracusa/market-risk-var-garch)
- [Options Expiration Analysis](https://github.com/JonatanSiracusa/options-expiration-analysis)

---

## Status

🟡 **70% complete** — core HMM regime detection and streak analysis functional. Volume integration and extended regime classification in progress.

---

## Author

**Jonatan Siracusa**
[LinkedIn](https://www.linkedin.com/in/ajsiracusa) · [GitHub](https://github.com/JonatanSiracusa) · [Medium](https://jonatansiracusa.medium.com)
