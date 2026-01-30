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

---

## 2. Where PSP Fits in Your Architecture

PSP is designed to operate strictly at the **settlement rule layer**.

It does not replace existing systems, but integrates between them.

A typical architecture may include:

- Product or service definition layer
- Pricing and inventory logic
- Payment initiation and asset transfer
- **Settlement rule resolution (PSP)**
- Fulfillment, delivery, or service execution

PSP is invoked **after a transaction intent exists**, but **before final settlement is considered complete**.

### What PSP Handles

PSP is responsible for:

- Resolving probabilistic settlement outcomes
- Deterministically computing final payable amounts
- Providing verifiable outcome proofs
- Enforcing non-retroactive settlement finalization

### What PSP Does Not Handle

PSP does **not** manage:

- User accounts or identity
- Product listings or inventories
- Payment custody or fund transfers
- Refund logistics or dispute resolution
- Frontend or user experience

PSP should be treated as a **pure settlement primitive**, similar to
how cryptographic hash functions or signature schemes are used as primitives
within larger systems.
