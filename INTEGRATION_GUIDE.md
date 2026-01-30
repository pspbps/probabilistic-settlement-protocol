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

---

## 3. Example Scenarios

This section illustrates how PSP may be applied in real-world systems.

### 3.1 E-commerce Probabilistic Settlement

In some e-commerce scenarios, the final settlement amount of an order
may intentionally vary according to predefined rules.

Examples include:
- Orders with a predefined probability of reduced settlement
- Promotional mechanisms where some transactions settle at zero cost
- Variable final charges determined at settlement time

Using PSP, the settlement outcome is:
- Predefined and transparent
- Verifiable by both merchant and buyer
- Non-manipulable after commitment

The merchant does not control individual outcomes, and the buyer does not
need to trust the merchant’s internal logic.

---

### 3.2 Discount and Cashback Programs

Traditional discount or cashback programs rely on centralized execution
and opaque logic.

PSP enables such programs to be expressed as settlement rules, where:
- Discounts are resolved probabilistically
- Cashback amounts are deterministically computed
- All outcomes can be independently verified

This reduces disputes and increases user trust without introducing
custodial or platform-level complexity.

---

### 3.3 Service-Level Guarantees

PSP may be used in service agreements where compensation depends on
probabilistic or conditional outcomes.

Examples include:
- Service credits triggered by predefined conditions
- Partial refunds resolved at settlement time
- Compensation rules that must be trusted by both parties

PSP ensures that settlement follows predefined rules and that outcomes
cannot be altered after the fact.
