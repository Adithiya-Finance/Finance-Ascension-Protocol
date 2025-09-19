# Day 15 — DCF Sensitivity Analysis

## 🔹 What I Built
Today I took the core Discounted Cash Flow (DCF) framework and added a **sensitivity table** that shows how firm valuation shifts when the discount rate (r) changes.  

## 🔹 Why This Matters
Valuation isn’t a single number. It’s a range that flexes with assumptions:  
- If r is higher → future cash flows are penalized more → valuation drops.  
- If r is lower → future cash flows retain more weight → valuation rises.  

This sensitivity analysis reveals the **fragility of assumptions**: a 1–2% swing in r can change enterprise value by millions.  

## 🔹 Core Formula Reverse Engineered
\[
PV = \frac{CF_t}{(1+r)^t}
\]  
- **1** = the 100% baseline of your money today.  
- **+r** = opportunity cost of capital (what else your money could earn).  
- **t** = time exponent, showing compounding drag across years.  

## 🔹 Takeaway
DCF is not about “finding the true value.”  
It’s about **testing the story**: if assumptions shift, does the company still make sense?  

---
