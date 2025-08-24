# Discounted Cash Flow (DCF) from First Principles

This repository rebuilds the **Discounted Cash Flow (DCF)** valuation method 
from its mathematical foundations, proving every step without templates or memorization.

---

## 🔍 Structure of Proof

1. **Layer 1: Time Value of Money**
   \[
   FV = PV(1+r)^n \Rightarrow PV = \frac{FV}{(1+r)^n}
   \]
   - Division is **inverse compounding**.

2. **Layer 2: Multi-Year Cash Flows**
   \[
   PV = \sum_{t=1}^N \frac{C_t}{(1+r)^t}
   \]
   - Linear summation of claims; exponential discounting.

3. **Layer 3: Perpetual Growth (Gordon Model)**
   \[
   PV = \frac{C_1}{r-g}, \quad r > g
   \]
   - Derived using a **geometric series** proof.

4. **Layer 4: Enterprise DCF**
   \[
   EV = \sum_{t=1}^{n} \frac{FCF_t}{(1+WACC)^t} + \frac{TV}{(1+WACC)^n}
   \]
   - WACC formula included; TV derived from Layer 3.


---

## 📄 Artifacts
- Scanned handwritten proofs (`proofs/`)
- Equation images for LinkedIn/Portfolio (`images/`)

---

## 🎯 Goal
Turn DCF into a **transparent valuation model** you can derive in any interview or case study.

---

**Tags:** `Finance`, `DCF`, `Mathematical Finance`, `Valuation`, `Investment Banking`

