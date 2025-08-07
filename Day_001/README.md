# Day 001 – Time Value of Money
- Learned: Discounting, Compounding
- Tool: Excel model
# 📅 Day 1 – Time Value of Money & Manual NPV Simulation

Welcome to Day 1 of the **Finance Ascension Protocol** — a 180-day intensive training built to master finance, investment logic, and financial modeling from first principles.

---

## 🎯 Objective

Understand and reconstruct the **Time Value of Money** and **Net Present Value (NPV)** logic **without using Excel shortcuts**.

> "Every ₹1 today has the potential to grow. Every ₹1 in the future is worth less because of inflation, risk, and opportunity cost."

---

## 📊 Case Study: Manual NPV Simulation

| Year | Cashflow |
|------|----------|
| 0    | -₹1000   |
| 1    | ₹300     |
| 2    | ₹400     |
| 3    | ₹500     |

### Discount Rate: `10%`

---

## 🧠 NPV Formula (from scratch)

\[
NPV = \sum_{t=0}^{n} \frac{CF_t}{(1 + r)^t}
\]

Where:  
- \( CF_t \) = Cashflow at time \( t \)  
- \( r \) = Discount rate  
- \( t \) = time period

---

## 🧱 Excel Simulation

| Year | Cashflow | Discount Factor | Present Value |
|------|----------|------------------|----------------|
| 0    | -1000    | =1.10^0          | =-1000/1       |
| 1    | 300      | =1.10^1          | =300/1.10      |
| 2    | 400      | =1.10^2          | =400/1.21      |
| 3    | 500      | =1.10^3          | =500/1.331     |

### ✅ NPV ≈ ₹29.19

---

## 🔍 Learnings

- 📉 Higher discount rate → lower present value  
- ⏳ Year 0 cashflow is not discounted  
- ✅ NPV > 0 → Accept investment  
- ❌ NPV < 0 → Reject (value-destroying)

---

## 📂 File Included

- `Manual_NPV_Simulation_Day1.xlsx` – fully built manual simulation  
- `Day_1_TVM_Notes_Adithiya.pdf` – handwritten & typed theory breakdown  
- `Day_1_LinkedIn_Post.txt` – ready-to-post caption for public proof

---

## 🔁 Bonus Challenge

> Change the rate to 15%  
> Redo the formulas  
> Re-analyze the result  
> Observe how NPV becomes more sensitive to risk

---

## 🚀 Next Steps

On Day 2, we’ll:
- Introduce **IRR logic**  
- Start timeline-based simulations  
- Translate formulas into business case reasoning

---

### 📌 Repository Purpose

This repo is a public ledger of my transformation from **student → analyst**, built on:

- 🔍 First principles finance  
- 📈 Excel-based decision models  
- 🧱 Manual logic → automation  
- 💼 Proof-of-work that recruiters and firms can verify

---

## 💬 Connect With Me

- LinkedIn: [www.linkedin.com/in/radithiyafinance]  
- GitHub: []  
- Email: [adithiyaroffice@gmail.com]  

---

#FinanceAscensionProtocol #NPV #ExcelFinance #InvestmentAnalysis #TimeValueOfMoney #StudentToStreet #ReverseEngineeringFinance
