# Probabilistic Settlement Protocol (PSP)
## Whitepaper v1.0.1

---

## Version & Scope Declaration

This document defines **Probabilistic Settlement Protocol (PSP) v1.x**.

This whitepaper is a **protocol-level specification**, not a business offering,
financial product, or application-layer implementation.

### Scope

PSP defines:

- Deterministic and verifiable probabilistic settlement rules
- Commit–reveal based randomness verification
- Protocol-level fee computation
- Non-retroactive governance constraints

PSP does **not** define:

- User interfaces or frontends
- Business logic or merchant policies
- Asset custody or fund transfers
- Compliance, consumer protection, or dispute resolution
- Application-specific workflows

Any application, platform, or service integrating PSP is solely responsible
for its own legal, regulatory, and operational compliance.

### Non-Endorsement

Use of PSP does not imply endorsement, approval, or partnership
by the PSP authors or contributors.

### Immutability of Finalized Outcomes

Once a settlement outcome is finalized under PSP rules,
it must not be altered retroactively by governance, operators, or integrators.

---

## Abstract

The **Probabilistic Settlement Protocol (PSP)** is a decentralized protocol
specification for **verifiable, non-manipulable probabilistic settlement**.

PSP defines a deterministic settlement primitive where the final settlement
outcome is selected from a predefined distribution using publicly verifiable
randomness derived via commit–reveal mechanisms.

Once finalized, settlement results are immutable and recomputable by any
third party.

PSP is designed as a **settlement-layer primitive**, not an application,
and is intended to be embedded into diverse systems including digital
commerce, financial workflows, and service settlement processes.

---

## 1. What PSP Is

PSP is:

- A **protocol**, not a platform
- A **settlement-layer primitive**, not a product
- A **verifiable probabilistic settlement standard**
- Designed to be embedded into external systems

PSP does **not** define:

- User interfaces
- Business logic
- Asset custody
- Application-specific workflows

PSP defines **how settlement outcomes are selected, finalized, and verified**.

---

## 2. Core Design Principles

### 2.1 Deterministic Recomputability

Given the same public inputs:

- Rule definition
- Committed randomness
- Declared settlement amount
- Protocol parameters

Any observer can deterministically recompute:

- Outcome index
- Final settlement metadata
- Protocol fee obligation

No trusted party is required.

---

### 2.2 Commit–Reveal Verifiability

Settlement randomness follows a commit–reveal flow:

1. A commitment hash is submitted on-chain
2. Inputs are revealed later
3. The revealed data must match the prior commitment

This prevents:

- After-the-fact manipulation
- Selective outcome bias
- Hidden randomness sources

---

### 2.3 Non-Retroactive Finality

Once a settlement is finalized:

- Outcomes cannot be changed
- Fees cannot be recalculated
- Rules cannot be retroactively modified

Protocol evolution is allowed **only for future settlements**.

> **The protocol may evolve, but it must never change past commitments.**

---

### 2.4 Minimal Trust Assumptions

PSP assumes:

- Public blockchain execution
- Transparent contract code
- Publicly verifiable data availability

PSP explicitly avoids reliance on:

- Trusted oracles
- Proprietary randomness providers
- Off-chain adjudication

---

## 3. Settlement Model

### 3.1 Rule Definition

A **Rule** defines a settlement distribution consisting of multiple **Outcomes**.

Each Outcome includes:

- A settlement behavior identifier
- A probability weight (basis points)
- A parameter field interpreted externally

All outcome weights must sum to **10,000 bps**.

---

### 3.2 Outcome Selection

Given:

- A finalized random value
- A rule's outcome distribution

The protocol deterministically maps the random value
to a single outcome index using cumulative probability traversal.

This process is:

- Deterministic
- Recomputable
- Non-interactive

---

### 3.3 Amount Binding and Outputs

Settlement finalization binds:

- Declared settlement amount
- Selected outcome index
- Protocol fee parameters

PSP does **not** transfer assets.

PSP outputs **verifiable settlement metadata**
that external systems may use to execute settlement
within their own execution context.

---

## 4. Randomness Model

### 4.1 Commit–Reveal Rationale

PSP intentionally adopts a **commit–reveal** mechanism
as its default randomness model.

This choice is motivated by:

- No dependency on third-party oracle networks
- Deterministic replay without oracle availability
- Reduced systemic and governance risk
- Suitability for protocol-layer primitives

Commit–reveal ensures:

- Commitments are immutable
- Reveals are publicly verifiable
- Manipulation attempts are detectable

PSP prioritizes **verifiability and auditability**
over perfect entropy.

---

### 4.2 Trust Properties

Commit–reveal provides:

- **Unpredictability before reveal**
- **Verifiability after reveal**
- **Non-repudiation of committed inputs**

It does not attempt to guarantee:

- Perfect cryptographic randomness
- Entropy beyond adversarial detectability

This tradeoff is intentional.

---

## 5. Fee Model

### 5.1 Protocol-Level Fee Principle

PSP defines a protocol-level fee that is:

- Deterministically computable
- Bound to settlement finalization
- Independent of asset transfer execution

The protocol does not charge for:

- Randomness generation
- Probability evaluation
- Rule definition

Fees are assessed **only when a settlement outcome is finalized**.

---

### 5.2 Deterministic Fee Computation

For each finalized invocation, the protocol computes a fee obligation:
feeCharged = min(amount * feeBps / 10,000, feeCap)

Where:

- `amount` is the declared settlement amount
- `feeBps` is the protocol fee rate in basis points
- `feeCap` is the maximum fee per invocation

All parameters are public and apply **only to future settlements**.

---

### 5.3 Fee Responsibility Separation

PSP separates:

- **Fee computation** (protocol responsibility)
- **Fee settlement** (integrator responsibility)

The protocol does **not** enforce asset transfers.
Custody, escrow, and payment execution are explicitly out of scope.

---

### 5.4 Verifiability and Non-Retroactivity

The computed fee is:

- Public
- Deterministic
- Bound to a specific invocation

No governance action may retroactively alter:

- Finalized settlement outcomes
- Previously computed fees

---

## 6. Governance and Upgradability

PSP governance applies **only to future protocol behavior**.

It may evolve through:

- Parameter updates
- Interface extensions
- Modular execution components

It must never explain or modify finalized settlements.

---

## 7. Integration Model

PSP is intended to be embedded by external systems.

PSP provides **settlement correctness guarantees**, not business logic,
randomized promotions, or application workflows.

Integrators remain responsible for:

- Asset custody
- Business logic
- User interaction
- Regulatory compliance

---

## 8. Security Considerations

PSP defends against:

- After-the-fact manipulation
- Selective outcome bias
- Hidden settlement logic

PSP does not defend against:

- Malicious frontends
- Incorrect integration
- Off-chain fraud

---

## 9. Conclusion

The Probabilistic Settlement Protocol (PSP) defines
a new class of decentralized settlement primitive that is:

- Probabilistic
- Verifiable
- Non-manipulable
- Deterministically auditable

PSP is not an application.  
PSP is not a business model.  

PSP is a **settlement rule protocol**.

---

**End of Document**  
Probabilistic Settlement Protocol (PSP)  
Whitepaper v1.0.1

