# Escalation ticket

## Ticket 1 — ambiguous small pedestrian

- **Frame/object:** adasind_056040.jpg, L3+M4, box about (211,775)–(249,852), mid zone.
- **Evidence:** screenshots/056040_pedestrian_conflict.png; r1_craft/compare.html; r3_diag/model_compare.html.
- **Expected impact:** one apparent extra Pedestrian contributes FP=1 against the teaching reference. Deleting a real visible person merely to improve the score would violate R01/R03.
- **Owner:** qa; proposed recipient is Lab Coach/reference maintainer. This ticket is recorded in the repository, not sent externally.
- **Recommendation:** inspect the original crop and decide whether the light-shirted figure is a separate standing/walking person, a rider, or unreadable. Retain the current label pending adjudication; E5_unresolved, not a proven reference defect. Shared model provenance prevents treating two agreeing sources as two independent votes.

## Ticket 2 — shared review workflow

The coach allowed one leader repository (reported by team leader). Students reviewed collaboratively while seated together; no separate blind student review log was captured. The repository records this deviation and an assistant audit, without reconstructing a fictitious blind review. Ask the coach whether an additional rules-only review by a teammate is needed.
