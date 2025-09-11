# Day 12: DCF + CAPM + Ratios Financial Model

import numpy as np

# -------------------------------
# 1. Inputs 
# -------------------------------
revenue_yr1 = 100000       # Revenue Year 1
growth_rate = 0.10         # Revenue growth rate
ebit_margin = 0.15         # EBIT margin
dep_amort = 5000           # Depreciation & Amortization
capex = 8000               # Capital Expenditures
wc_change = 2000           # Change in Working Capital
tax_rate = 0.30            # Tax Rate
equity = 70000             # Equity for WACC
debt = 30000               # Debt for WACC
Rd = 0.06                  # Cost of Debt
Rf = 0.05                  # Risk-free rate
Rm = 0.11                  # Market return
beta = 1.2                 # Beta for CAPM
g = 0.03                   # Terminal growth rate
forecast_years = 5

# -------------------------------
# 2. Revenue and EBIT Forecast
# -------------------------------
revenues = [revenue_yr1 * (1 + growth_rate)**i for i in range(forecast_years)]
ebit = [rev * ebit_margin for rev in revenues]
tax = [e * tax_rate for e in ebit]
nopat = [e - t for e, t in zip(ebit, tax)]

# -------------------------------
# 3. Free Cash Flow
# -------------------------------
fcf = [n + dep_amort - capex - wc_change for n in nopat]

# -------------------------------
# 4. WACC Calculation
# -------------------------------
weight_e = equity / (equity + debt)
weight_d = debt / (equity + debt)
Re = Rf + beta * (Rm - Rf)    # CAPM cost of equity
wacc = weight_e * Re + weight_d * Rd * (1 - tax_rate)

# -------------------------------
# 5. Discount Factors and PV of FCF
# -------------------------------
discount_factors = [(1 / (1 + wacc) ** (i+1)) for i in range(forecast_years)]
pv_fcf = [fcf[i] * discount_factors[i] for i in range(forecast_years)]

# -------------------------------
# 6. Terminal Value
# -------------------------------
fcf_next = fcf[-1] * (1 + g)
terminal_value = fcf_next / (wacc - g)
pv_terminal = terminal_value / (1 + wacc)**forecast_years

# -------------------------------
# 7. Enterprise Value
# -------------------------------
enterprise_value = sum(pv_fcf) + pv_terminal

# -------------------------------
# 8. Leverage & ROE Sensitivity
# -------------------------------
ROA = nopat[-1] / (equity + debt)   # Approx ROA
ROE = ROA + (ROA - Rd) * (debt / equity)

# -------------------------------
# 9. Output
# -------------------------------
print("Revenue Forecast:", revenues)
print("EBIT:", ebit)
print("NOPAT:", nopat)
print("FCF:", fcf)
print("Discount Factors:", discount_factors)
print("PV of FCF:", pv_fcf)
print("Terminal Value:", terminal_value)
print("PV Terminal Value:", pv_terminal)
print("Enterprise Value:", enterprise_value)
print("Cost of Equity (Re):", Re)
print("WACC:", wacc)
print("ROE:", ROE)
