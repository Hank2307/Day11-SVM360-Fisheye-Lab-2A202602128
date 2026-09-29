# Guideline patch

- **Proposed rule:** add an explicit decision sequence for a small partially hidden person near a rider: inspect the native-resolution crop; decide seated rider versus separate standing/walking person; measure visible height against H=40; if identity/extent remains unclear, preserve the case for adjudication with crop coordinates and competing interpretations.
- **Applies to:** Pedestrian/Bike, R01/R03/R06, especially overlapping mid-zone objects.
- **Gap:** R03 states the class mapping but does not specify evidence required for ambiguous partly hidden people. In 056040 L3+M4, a light-shirted person appears behind a rider while the reference has no matching box. Agreement of L and M is not independent evidence because the draft came from M.
- **Proposed rules_version:** v1.1.0, pending Lab Coach approval. Current labels remain evaluated under v1.0.0.
- **Effective from:** a future annotation round after approval and a small two-reviewer calibration exercise; do not apply retroactively to inflate metrics.
