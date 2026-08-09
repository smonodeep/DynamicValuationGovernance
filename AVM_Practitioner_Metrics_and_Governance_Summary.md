# AVM Practitioner Metrics and Governance Notes

## 1. Core AVM Performance Metrics

  -----------------------------------------------------------------------
  Metric            Definition        Formula           Interpretation
  ----------------- ----------------- ----------------- -----------------
  Hit Rate          Proportion of     Hit Rate = AVM    Higher values
                    valuation         Estimates / Total indicate broader
                    requests for      Requests          model coverage.
                    which the AVM                       
                    produces an                         
                    estimate.                           

  Percentage Error  Relative          (AVM Estimate −   Positive =
  (PE)              deviation of the  Benchmark Value)  overvaluation;
                    AVM estimate from / Benchmark Value negative =
                    the benchmark                       undervaluation.
                    sale price.                         

  Absolute Error    Absolute value of \|PE\|            Measures error
  (AE)              Percentage Error.                   magnitude
                                                        irrespective of
                                                        direction.

  Mean Error (ME)   Average           ΣPE / N           Measures
                    Percentage Error.                   systematic
                                                        valuation bias.

  Mean Absolute     Average Absolute  (1/N)Σ\|PE\|      Measures average
  Error (MAE)       Error.                              prediction error
                                                        magnitude.

  Root Mean Square  Square root of    √\[(ΣPE²)/N\]     Penalizes large
  Error (RMSE)      average squared                     errors more
                    Percentage                          heavily than MAE.
                    Errors.                             

  PPE10             Percentage of     (AE ≤ 10%) / N ×  Overall model
                    valuations with   100%              success rate
                    Absolute Error ≤                    within ±10% error
                    10%.                                band.

  PPE \> +20%       Percentage of     (PE \> +20%) / N  Measures
                    valuations with   × 100%            frequency of
                    Percentage Error                    extreme
                    \> +20%.                            overvaluation
                                                        outliers.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 2. Practitioner Performance Thresholds

  -------------------------------------------------------------------------
  Metric                     Threshold     Acceptable Range Purpose
  --------------- -------------------- -------------------- ---------------
  Mean Error (ME)         \|ME\| ≤ 10%           −8% to +8% Controls
                                                            systematic
                                                            bias.

  PPE10                           ≥55%       ≥65% preferred Indicates
                                                            satisfactory
                                                            valuation
                                                            accuracy.

  PPE \> +20%                     ≤10%                 ≤10% Limits
                                                            high-side
                                                            valuation
                                                            outliers.
  -------------------------------------------------------------------------

------------------------------------------------------------------------

## 3. Relationship Between Metric Values and Model Performance

  -------------------------------------------------------------------------
  Metric                   Optimal Value Performance      Comments
                                         Trend as Metric  
                                         Increases        
  ---------------- --------------------- ---------------- -----------------
  Hit Rate                          100% Increasing       Higher Hit Rate
                                                          indicates better
                                                          performance.

  Mean Error                          0% Closest to 0% is Lower systematic
                                         best             bias.

  MAE                                 0% Decreasing       Lower MAE
                                                          indicates higher
                                                          accuracy.

  RMSE                                0% Decreasing       Lower RMSE
                                                          indicates fewer
                                                          large errors.

  PPE10                             100% Increasing       Higher PPE10
                                                          indicates better
                                                          accuracy.

  PPE \> +20%                         0% Decreasing       Lower values
                                                          indicate fewer
                                                          extreme
                                                          overvaluations.
  -------------------------------------------------------------------------

------------------------------------------------------------------------

## 4. Market Valuation Classification

  ------------------------------------------------------------------------
  Classification             Overvaluation Threshold Interpretation
  --------------------- ---------------------------- ---------------------
  Overvalued Market                          \> +20% Significant
                                                     overvaluation;
                                                     elevated correction
                                                     risk.

  Moderately Valued                       0% to +20% Moderate
  Market                                             overvaluation within
                                                     acceptable range.

  Undervalued Market                           \< 0% Prices below
                                                     estimated fundamental
                                                     value.
  ------------------------------------------------------------------------

> Overvaluation is typically evaluated at a regional level (e.g., MSA,
> state, municipality) using the previous quarter's estimates.

------------------------------------------------------------------------

## 5. Disclosure vs. Non-disclosure States

  -----------------------------------------------------------------------
  Regime                  Sale Price Availability AVM Implications
  ----------------------- ----------------------- -----------------------
  Disclosure States       Sale prices publicly    Rich transaction data
                          recorded.               improves AVM
                                                  calibration and
                                                  validation.

  Non-disclosure States   Sale prices not         Reduced data
                          publicly disclosed;     availability increases
                          alternative proprietary modeling uncertainty
                          sources required.       and reliance on
                                                  governance controls.
  -----------------------------------------------------------------------

Examples of non-disclosure states include Alaska, Idaho, Indiana,
Kansas, Louisiana, Maine, Mississippi, Missouri, Montana, New Mexico,
North Dakota, Texas, Utah, and Wyoming (subject to changes in state
legislation).

------------------------------------------------------------------------

## Key Research Takeaways

-   Practitioner AVM evaluation relies on **coverage (Hit Rate)**,
    **accuracy (MAE, RMSE, PPE10)**, **bias (ME)**, and **tail risk (PPE
    \> +20%)**.
-   Acceptance thresholds provide operational criteria for model
    validation.
-   Overvaluation classifications support regional market surveillance
    and portfolio risk assessment.
-   Disclosure regimes directly affect transaction data availability
    and, consequently, AVM development, validation, and governance.
-   Non-disclosure states illustrate how data-constrained environments
    necessitate stronger valuation governance, aligning with the broader
    governance challenges observed in emerging markets such as India.
