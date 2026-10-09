# fractional-quadratic-programming-agent
An iterative agent for solving fractional quadratic programming problems.

## Problem

Minimize:

    f(x) = (x^T A x + α) / (x^T B x + β)
    
over x ∈ {-1, 1}^n, where A, B are symmetric matrices.

This problem is NP-hard in general (contains Max-Cut as a special case).
Polynomially solvable when rank(A) ≤ r_a, rank(B) ≤ r_b, A has nonpositive
diagonal, and B has nonnegative diagonal.

## Agent Iteration Loop

The agent runs in rounds:

1. **Baseline** — Standard Dinkelbach algorithm, measure convergence.
2. **Strategy Search** — Try different subproblem solvers (spectral, SDP,
   gradient projection).
3. **Rank Exploration** — Construct instances with rank constraints, test
   polynomial solvability.
4. **Acceleration** — Improve update rules based on error patterns.

Each round records:
- Iteration count
- Objective value decrease
- Wall-clock time

## Results

## How to Run

## Reference
- Dinkelbach, W. (1967). On nonlinear fractional programming.
  
## Report
See [report.pdf](./report.pdf) for the full iteration summary.
