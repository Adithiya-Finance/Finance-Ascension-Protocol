# Day 13 — DCF / FCFF Model (Finance Ascension Protocol)

This repository documents **Day 13 of my Finance Ascension Protocol**, where I built a full **Discounted Cash Flow (DCF) model** using **Free Cash Flow to Firm (FCFF)** from first principles. The focus is on breaking down *why* each formula exists — not just plugging numbers.

---

## 📌 Key Steps in the Model

1️⃣ **Revenue Projection**  
Revenue grows recursively:
```
Revenue_t = Revenue_{t-1} × (1 + GrowthRate)
```

2️⃣ **COGS & Gross Profit**  
```
COGS = Revenue × COGS%
Gross Profit = Revenue - COGS
```

3️⃣ **Operating Expenses & EBIT**  
```
Opex = SG&A + R&D (both % of Revenue)
EBIT = Gross Profit - Opex
```

4️⃣ **NOPAT (After-Tax Profit)**  
```
NOPAT = EBIT × (1 - TaxRate)
```

5️⃣ **Free Cash Flow to Firm (FCFF)**  
```
FCFF = NOPAT + Depreciation - ΔWorkingCapital - CapEx
```

6️⃣ **Discounting Future Cash Flows**  
```
PV(FCFF_t) = FCFF_t / (1 + WACC)^t
```

7️⃣ **Terminal Value (Gordon Growth)**  
```
TV = FCFF_last × (1 + g) / (WACC - g)
```

8️⃣ **Enterprise Value (EV)**  
```
EV = Σ PV(FCFF) + PV(Terminal Value)
```

---

## 🖥️ Excel Layout
| Year | Revenue | COGS | Gross Profit | Opex | EBIT | Tax | NOPAT | ΔWC | CapEx | Depreciation | FCFF | Discount Factor | PV_FCFF |
|------|---------|------|--------------|------|------|-----|-------|-----|-------|--------------|------|----------------|---------|

Each row flows logically: **Revenue → Costs → EBIT → NOPAT → FCFF → EV**.

---

## 🧠 Reverse-Engineering Mindset
- Multiplication → Compounding or scaling (growth, % of revenue)
- Subtraction → Residuals (profit after cost layers)
- Addition → Non-cash adjustments (depreciation back to cash)
- ΔWorking Capital, CapEx → Real drains on cash
- Discounting → Converting future promises into today’s value

---

## 🔖 Next Steps
- Add scenario/sensitivity analysis (WACC vs growth)
- Layer in debt/equity adjustments for Equity Value per share
- Stress-test assumptions (CapEx, margins, working capital)

---

