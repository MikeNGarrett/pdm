<!--
  Title: RAID Log Template
  Purpose: Track Risks, Assumptions, Issues, Dependencies in one table.
  Inputs: {RAID_Rows}
  Usage: copy, paste, add new rows during project life-cycle.
-->
h1. RAID Log Template  

Version: 1.0.0

---

|| Status          || {status:DRAFT} ||
|| Audience        || Project / Program Team ||
|| Confidentiality || [Public \| Internal \| Restricted] ||

---

h2. 1. Purpose  

Track **R**isks, **A**ssumptions, **I**ssues, and **D**ependencies in one continuously updated table.  
Update *Status* and *Action / Mitigation* as items evolve.

---

h2. 2. RAID Table  

| # | Date | Type<br>(*Risk / Assumption / Issue / Dependency*) | Item / Description | Owner | Status<br>(*Open / Active / Resolved / Closed*) | Impact<br>(*High / Medium / Low*) | Action / Mitigation | Target / Review Date |
|---|------|----------------------------------------------------|--------------------|-------|-----------------------------------------------|-----------------------|---------------------|-----------------------|
| 1 | [YYYY-MM-DD] | Risk | *e.g., Third-party API rate limits may delay launch* | [Owner] | Open | High | Draft fallback caching strategy | [YYYY-MM-DD] |
| 2 | [YYYY-MM-DD] | Assumption | *e.g., Users will have modern browsers (ES6+)* | [Owner] | Active | Medium | Validate via analytics; update requirement if false | [YYYY-MM-DD] |
| 3 | [YYYY-MM-DD] | Dependency | *e.g., Upstream data feed v2 required* | [Owner] | Open | High | Confirm delivery timeline with provider | [YYYY-MM-DD] |
| 4 | [YYYY-MM-DD] | Issue | *e.g., Sprint 4 velocity dropped 30 %* | [Owner] | Resolved | Low | Adjust capacity planning next sprint | [YYYY-MM-DD] |

_Add rows as needed. Sort or filter by Type, Status, or Impact during reviews._

---

h2. 3. Status & Impact Definitions  

| Field   | Definition |
|---------|------------|
| **Status** | *Open* — logged, no action yet · *Active* — mitigation in progress · *Resolved* — addressed, awaiting confirmation · *Closed* — no further action |
| **Impact** | *High* — threatens scope, timeline, or budget · *Medium* — manageable with careful oversight · *Low* — minor; monitor only |

---

h2. 4. Review Cadence  

- Review the RAID log at each weekly status or sprint review.  
- Escalate any **High-impact** items without an owner or overdue target date.

---

h2. 5. Sources / References  

Link to discovery docs, risk assessments, or dependency agreements that inform this log.