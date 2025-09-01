📊 Day 9 – Discounted Cash Flow (DCF) Model Rebuild

🔹 Key Components

Revenue Forecasting

Base year revenue (2025E)

Growth assumption per year → Forecast revenue for 5 years

EBIT & NOPAT

EBIT = Revenue × Operating Margin  
NOPAT = EBIT × (1 - Tax Rate)


Free Cash Flow to Firm (FCFF)

FCFF = NOPAT + Depreciation - Capex - ΔWorking Capital


Discount Factor

Discount Factor (Year n) = 1 / (1 + WACC)^n
PV of FCFF = FCFF × Discount Factor


Terminal Value

TV (End of Year n) = FCFF(n+1) × (1 + g) / (WACC - g)
PV(TV) = TV × Discount Factor (Year n)


Enterprise Value

EV = Σ PV(FCFF) + PV(Terminal Value)

🔹 Excel Cell Map (Sample Layout)
Cell	Formula	Description
B3	2025 Revenue	Base year revenue input
C3	=B3*(1+Growth%)	Revenue forecast
B6	=C3*OPM%	EBIT
B7	=B6*(1-Tax%)	NOPAT
B10	=B7+Depreciation-Capex-ΔWC	FCFF
B13	=1/(1+WACC)^Year	Discount Factor
B14	=B10*B13	PV of FCFF
B17	=(FCFF_next*(1+g))/(WACC-g)	Terminal Value
B18	=B17*B13	PV of Terminal Value
B20	=SUM(PV_FCFF_range)+B18	Enterprise Value
🔹 Why This Matters

Discounting: Captures risk and opportunity cost.

Terminal Growth: Reflects going-concern valuation.

FCFF vs. FCFE: FCFF avoids leverage distortions, making EV comparisons cleaner.

Dynamic Design: Change assumptions → Model updates instantly.


This DCF model is structured for sensitivity analysis (Growth vs. WACC matrix) and clean audit trails. 


🔹 Deliverable

This DCF model is structured for sensitivity analysis (Growth vs. WACC matrix) and clean audit trails. Next step: Automate a two-variable data table to see how EV reacts to growth/WACC changes.
