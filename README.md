# Probabilistic Settlement Protocol (PSP)

**Status:** Canonical Protocol Specification  
**Version:** v1.x (Whitepaper v1.0 · Spec v1.1 Draft)  
**License:** MIT (Specification)

---

## Overview

The **Probabilistic Settlement Protocol (PSP)** is a decentralized settlement protocol specification for **verifiable, non-manipulable probabilistic settlement**.

PSP defines how a fixed settlement amount can be deterministically resolved into **multiple possible outcomes**, according to predefined probability weights, while remaining:

- Fully on-chain verifiable
- Deterministically recomputable by third parties
- Non-manipulable after commitment
- Compatible with deterministic fee computation

This repository is the **canonical specification repository** of the PSP protocol.

---

## What PSP Is (and Is Not)

### PSP **Is**
- A **protocol**, not a platform
- A **settlement-layer primitive**
- A **probabilistic settlement standard**
- Designed to be embedded into:
  - E-commerce systems
  - Financial workflows
  - Service and fulfillment protocols

### PSP **Is Not**
- An application
- A UI or frontend product
- A custody system
- A gambling or betting protocol

---

## Core Properties

### 1. Commit–Reveal Verifiability
Settlement inputs are committed **before** outcome revelation, preventing after-the-fact manipulation.

### 2. Deterministic Recomputation
Any third party can recompute:
- The resolved outcome
- The charged protocol fee  
using only public inputs and on-chain data.

### 3. Non-Retroactive Governance
Protocol parameters may evolve **only via timelocked governance** and never affect finalized settlements.

### 4. Protocol-Level Fee Model
Fees are computed deterministically and bound to settlement finalization, not discretionary execution.

---

## Repository Structure

This repository contains **only protocol-level documentation and specifications**.

---

## Governance

The governance model and authorship declaration of PSP are defined in:

- [GOVERNANCE.md](./GOVERNANCE.md)

This document defines how the protocol may evolve without affecting finalized settlements.

---

## Citation & Usage

Guidelines for referencing and implementing PSP are defined in:

- [CITATION.md](./CITATION.md)

This document clarifies correct and incorrect usage of the PSP name and specification.

---

## Authorship & Governance

PSP is currently maintained as an author-stewarded protocol specification.

There is no foundation or governing entity at this stage.  
Governance applies only to specification evolution and never affects
finalized settlements.

Details are defined in [GOVERNANCE.md](./GOVERNANCE.md).




