# 📊 Day 11 — DCF & WACC Model  

A fully functional **Discounted Cash Flow (DCF) model with Weighted Average Cost of Capital (WACC)** built in Excel. This project is part of my **Finance Ascension Protocol (Day 11)**, where I reverse-engineer valuation formulas from first principles instead of just applying them.  

---

## 🚀 Project Highlights  
- **Dynamic Inputs Sheet** → Risk-free rate, Beta, Market premium, Debt/Equity, Tax rate.  
- **CAPM-based Cost of Equity** →  
r_e = r_f + β (E[R_m] - r_f)
- **Weighted Average Cost of Capital (WACC)** →  
WACC = (E/(E+D+P)) * r_e + (D/(E+D+P)) * r_d * (1-T) + (P/(E+D+P)) * r_p
- **FCFF Projection Engine** → 5-year EBIT, NOPAT, CapEx, Depreciation, Working Capital.  
- **Terminal Value via Perpetuity Growth** →  
TV = FCFF_(n+1) / (WACC - g)
- **Enterprise Value** = PV(FCFF) + PV(Terminal Value).  
- **Sensitivity-ready structure** → Easily extend to WACC vs g tables.  

----
