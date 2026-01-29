# PSP Governance & Authorship

## Authorship

The Probabilistic Settlement Protocol (PSP) specification was originally authored and published by the PSP author(s).

This repository represents the **canonical definition** of the PSP protocol specification.

Authorship refers to:
- The original protocol design
- The semantic definition of probabilistic settlement
- The invariants and constraints defined in the whitepaper and specifications

---

## Governance Model

PSP follows a **non-custodial, specification-first governance model**.

- The protocol itself does not assume on-chain governance.
- Governance applies to the **evolution of the specification**, not to finalized settlements.
- All finalized settlements are immutable and non-retroactive.

---

## Upgrade Principles

Protocol evolution must satisfy the following principles:

1. **Explicit Versioning**  
   All changes must be versioned and documented.

2. **Non-Retroactivity**  
   Changes must never affect already finalized settlements.

3. **Timelocked Adoption**  
   Any parameter or semantic change must include a clear adoption delay.

4. **Public Verifiability**  
   All changes must be publicly reviewable.

---

## Implementations

Implementations of PSP:
- May be open-source or closed-source
- Are not authoritative unless explicitly declared
- Must not claim protocol-level authority unless referencing this repository

---

## Trademark & Naming

The name “Probabilistic Settlement Protocol (PSP)” refers to the protocol specification defined in this repository.

Use of the name must not imply:
- Exclusive ownership of implementations
- Custodial control
- Centralized authority over settlement outcomes

---

## Disclaimer

This repository defines a protocol specification, not a financial product or service.

Use of the protocol is at the discretion and risk of implementers.
