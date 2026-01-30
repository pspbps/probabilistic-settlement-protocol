# PSP Integration Guide

This guide explains how to integrate the Probabilistic Settlement Protocol (PSP)
into real-world systems.

---

## 1. When You Should Use PSP

You should consider using PSP when **the settlement outcome of a transaction
is intentionally non-deterministic**, but must remain:

- Verifiable
- Non-manipulable
- Deterministically recomputable after finalization

Typical indicators include:

- The final payable amount may vary according to predefined probabilities
- The outcome must be trusted by all parties without a central operator
- Post-hoc manipulation must be impossible

PSP is particularly suitable when traditional centralized logic such as
randomized discounts, lotteries, or refunds would otherwise require
blind trust in the operator.

PSP replaces trust in the operator with **trust in verifiable settlement rules**.
