# Market Risk: VaR, Expected Shortfall & Stress Testing

End-to-end market risk project analysing a multi-asset portfolio using Value at Risk (VaR), Expected Shortfall (ES), Monte Carlo simulation, dynamic volatility modelling, formal model backtesting and portfolio stress testing.

## Project Overview

The analysis constructs an equally weighted $1 million portfolio across:

- SPY — S&P 500
- QQQ — Nasdaq-100
- TLT — Long-duration US Treasuries
- LQD — Investment-grade corporate bonds
- GLD — Gold

The project examines portfolio risk using both statistical tail-risk models and scenario-based stress testing.

## Methodology

The framework covers:

- Portfolio return and volatility analysis
- Correlation and drawdown analysis
- Historical VaR and Expected Shortfall
- Gaussian parametric VaR and Expected Shortfall
- Monte Carlo simulation
- Rolling VaR backtesting
- Kupiec unconditional-coverage testing
- Christoffersen independence and conditional-coverage testing
- EWMA volatility modelling
- Student-t tail modelling
- Rolling no-look-ahead Student-t EWMA VaR
- Historical stress testing
- Hypothetical stress scenarios
- Asset-level stress P&L attribution

## Key Findings

- Portfolio returns exhibit heavy tails and volatility clustering, limiting the reliability of Gaussian risk assumptions.
- Historical 99% VaR provides the strongest unconditional calibration among the tested models.
- Gaussian specifications materially underestimate extreme tail risk.
- EWMA improves volatility responsiveness but does not eliminate clustered VaR exceptions.
- Rolling Student-t EWMA improves tail modelling relative to Gaussian EWMA, but still fails conditional-coverage testing.
- Stress testing shows that diversification benefits can weaken materially when equities and fixed income decline simultaneously.

## Model Validation

VaR models are evaluated using:

- Kupiec unconditional-coverage test
- Christoffersen independence test
- Conditional-coverage test

No tested specification satisfies all conditional-coverage requirements, illustrating the limitations of relying on a single VaR model for portfolio risk management.

## Stress Testing

The project evaluates both historical and hypothetical market shocks.

Historical scenarios include:

- 2018 Q4 selloff
- COVID-19 market crash
- 2022 cross-asset selloff

Hypothetical scenarios examine equity crashes, interest-rate shocks, risk-off environments and simultaneous cross-asset declines.

## Tools

Python, pandas, NumPy, SciPy, Matplotlib, yfinance and Jupyter Notebook.

## Disclaimer

This project is for educational and portfolio demonstration purposes only and does not constitute investment advice.

