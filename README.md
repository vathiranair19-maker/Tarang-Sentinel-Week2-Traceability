# Week 2 · Exercise 2 · Sentinel Disconnection: Traceability Trace Report

**Candidate ID:** 280222
**Case:** Tarang Power Distribution Ltd, Sentinel revenue-protection system (Phase 2, domestic customers)
**Decision traced:** disconnection of supply, account 4471-0098-22 (Mrs. Lalitha Pillai, Ward 14, Coastal Zone), work order WO-88217, 5 March 2027
**Prepared:** 15 March 2027, for Sandra D'Souza (Head of Internal Audit)
**Due:** 19 March 2027. The Energy Ombudsman's reply is due 31 March 2027.

---

## Purpose

This repository holds a traceability report on one automated decision. It traces the decision back from the notice and disconnection to the intent behind the system, and answers the Energy Ombudsman's six questions (Q1 to Q6).

The report separates three things at every step:

- **Shown:** a record supports it.
- **Shown false:** a record contradicts it.
- **Cannot be shown:** the record that would settle it does not exist.

Every factual claim cites an evidence ID (E1 to E21, from the case pack). Every time is converted to UTC.

## Contents

| File | What it is |
|---|---|
| `UST_AITPM_Week2_Ex2_280222.docx` | The completed Part D answer sheet, sections D1 to D9 |
| `README.md` | This file |

## How to read the report

Read in this order:

1. **D2, The answer, first.** One paragraph with the conclusion, what is shown, what is false, what cannot be shown, and confidence.
2. **D8, Answers to the Ombudsman.** Q1 to Q6, each answered directly with evidence IDs.
3. **D4, Hop-by-hop trace.** Each hop from the notice (H0) back to the intent (H7), with a verdict: Linked, Partial or Broken.
4. **D7, Silent breaks.** Nine breaks, each with an owner for the missing evidence and the control that would prevent recurrence.
5. **D9, Statements not relied on, links that hold, assumptions.** What was excluded and why, what was checked, and what was assumed.

D1 (header), D3 (timeline), D5 (runtime controls) and D6 (traceability matrix) are the supporting detail.

## Summary of findings

- **The disconnection followed a remote desk review, not an on-site verification.** Verification VER-77310 took 33 seconds on 2 March. It was remote, used a photo from 14 November 2026, and recorded no GPS (E14). REV-5 requires on-site verification with a GPS-stamped photo at the premises.
- **The remote route came from an unapproved rule change.** Rule R-22 was added to the rules engine at 02:50 UTC on 2 March, through the console, with no Model Risk approval and no risk-owner review (E4, E5, E6).
- **The medical-priority check never matched.** The customer key from the VoltIQ connector does not match the register's CRM keys, so the default
