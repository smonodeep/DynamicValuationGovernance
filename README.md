Dynamic Valuation Governance

Uncertainty → Governance → Decision in Property Lending

---

1. Overview

This project studies how uncertainty is generated, transformed, and transmitted within property lending systems, ultimately influencing credit and valuation decisions.

The research is anchored in a unifying framework:

«Uncertainty → Governance → Decision»

- Uncertainty arises from valuation dispersion, market dynamics, and data inconsistencies
- Governance acts as a transformation layer (models, controls, policy transmission)
- Decision reflects final outputs such as pricing, lending, and risk assessment

---

2. Domain Focus

The empirical setting is property lending, with a specific focus on:

- Multifamily apartments
- Intersection of:
  - Urban Economics
  - Commercial Real Estate (CRE)
  - Residential Real Estate (RRE)

This segment is chosen because it naturally embeds:

- Rental income dynamics (CRE-like)
- Asset price appreciation (RRE-like)
- Strong sensitivity to macro policy (interest rates)

---

3. Research Objective

The project aims to:

1. Quantify valuation uncertainty using divergence between price and rent dynamics
2. Examine how monetary policy (Repo Rate) propagates into real estate markets
3. Model how governance layers (statistical + econometric frameworks)
   transform uncertainty into actionable signals
4. Understand heterogeneity across cities and regimes

---

4. Data Architecture

4.1 Data Sources

The dataset is constructed from three primary sources:

A. House Price Index (HPI)

- Source: Reserve Bank of India (RBI)
- Issue: Multiple base years across series
- Treatment:
  - Base normalization
  - Cross-linking across rebased indices
  - Creation of a continuous HPI time series

---

B. Rental Data

- Source: CREMatrix (city-level extraction)
- Nature:
  - Manually compiled
  - City-specific rental indices
- Cities covered:
  - Bangalore
  - Chennai
  - Delhi
  - Mumbai

---

C. Monetary Policy (Repo Rate)

- Source: FRED database
- Transformation:
  - Repo growth
  - Lag structures
  - Moving averages (MA2 primarily used)

---

4.2 Final Dataset

- Time Period: 2015 Q1 – 2024 Q4
- Frequency: Quarterly
- Geography: 4 major Indian cities
- Observations: Panel + aggregated formats

---

5. Key Variable Construction

Core Variables

- HPI Growth → Price dynamics
- Rent Growth → Income dynamics
- Valuation Gap →
  HPI Growth − Rent Growth
  → Proxy for mispricing / disequilibrium

---

Policy Variables

- Repo Rate
- Repo Growth
- Repo Growth MA(2) → captures smoothed policy transmission

---

Lag Structure

- HPI Lag
- Rent Lag
- Repo Lag

These capture temporal propagation of shocks

---

6. Methodological Framework

The modeling strategy is layered to reflect the core thesis:

---

A. Layer 1: Structural Modeling (HPI Dynamics)

- HAC-robust OLS
- Panel regression (city fixed effects)
- Quantile regression

Captures:

- Average effects
- Distributional asymmetry
- Cross-city heterogeneity

---

B. Layer 2: Valuation Gap Dynamics

- ARIMAX models
- Exogenous driver: Repo Growth (MA2)
- Objective:
  - Model policy transmission into valuation misalignment

---

C. Layer 3: Uncertainty Modeling

- GARCH / EGARCH (where statistically valid)
- Applied primarily to:
  - Larger pooled datasets

 Insight:

- Volatility is not always intrinsic
- It emerges under aggregation and regime interaction

---

7. Key Insights (Emerging)

- Monetary policy has a statistically significant impact on valuation gap
- Rental and price dynamics are not perfectly synchronized
- Valuation uncertainty is:
  - Weak at aggregate levels (short series)
  - Strong when cross-sectional heterogeneity is preserved
- City-level dynamics exhibit heterogeneous policy transmission

---

8. Conceptual Contribution

This work reframes real estate modeling as:

Data → Uncertainty → Governance → Decision

Where:

- Data inconsistencies create uncertainty
- Governance (models, transformations, smoothing) shapes interpretation
- Decisions emerge as a function of both structure and uncertainty

---

9. Repository Structure (Indicative)

- "0.DBA_data_prep.ipynb" → Data ingestion and preprocessing
- Modeling notebooks → HPI, valuation gap, volatility
- Visualizations → Trend, regime, and diagnostic plots

---

10. Future Extensions

- Regime-switching models
- City-level policy transmission heterogeneity
- Integration with credit risk (PD / LGD frameworks)
- Linking valuation uncertainty to lending decisions

---

11. Summary

This project demonstrates that:

«Valuation is not just a function of fundamentals,
but of how uncertainty is governed before decisions are made.»

---
