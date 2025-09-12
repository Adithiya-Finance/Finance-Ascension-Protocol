"""
Day 13 — DCF / FCFF Model 



Purpose: A single-file, self-contained implementation of a 5-year FCFF projection
and enterprise value calculation from first principles. 




Key formulas encoded here (comments reference first principles):

  Revenue_t = Revenue_{t-1} * (1 + growth_rate)         # multiplicative compounding
  
  COGS = Revenue * cogs_pct                              # proportional direct costs
  
  Gross = Revenue - COGS                                 # subtraction gives residual
  
  EBIT = Gross - Total_Opex                              # operating profitability
  
  NOPAT = EBIT * (1 - tax_rate)                          # tax reduces operating returns
  
  FCFF = NOPAT + Depreciation - Delta_WC - CapEx        # cash available to providers
  
  PV(FCFF) = FCFF / (1 + WACC)^t                         # time-value discounting
  
  TV = FCFF_last * (1+g) / (WACC - g)                    # Gordon growth terminal

"""

