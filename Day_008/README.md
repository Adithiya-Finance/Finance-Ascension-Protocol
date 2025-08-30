1. Discounted Cash Flow (DCF)

Perpetuity Formula (Re-derived)

PV = CF1 / (r - g)


Derived from:

PV = Σ [CF0 * (1+g)^t / (1+r)^t],  t=1..∞


Constraint: g < r for convergence.
Proof: Convergence of a geometric series.

2. Weighted Average Cost of Capital (WACC)

Formula:

WACC = (E/V)*Re + (D/V)*Rd*(1-T)


Equity return via CAPM:

Re = Rf + β * (Rm - Rf)
β = Cov(Ri, Rm) / Var(Rm)


Leverage Effect:

βL = βU * [1 + (1-T)*(D/E)]

3. Sensitivity Analysis as Calculus

Instead of discrete tables, used gradients:

∂V/∂g, ∂V/∂r
J = [[∂V/∂g, ∂V/∂r]]


Produces continuous valuation sensitivity surfaces.

4. Accretion/Dilution Mechanics
EPS_new = (NI_old + NI_target - Interest*Debt) / (Shares_old + New_shares)


Mapped all boundary conditions explicitly (deal structure vs. shareholder impact).

5. Monte Carlo Valuation Simulation
V = f(r, g, margins, multiples)


Each parameter modeled as a stochastic variable.

Outputs full probability distribution of valuation outcomes with tail risk.
