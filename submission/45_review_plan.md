# Review plan from observed errors

| Slice / frame | Cases and types | Priority reason | Evidence |
|---|---|---|---|
| B1-center / 006840 | One missing small pedestrian R7; model rider splits and wrong ThreeWheeler classes | A visible person above H=40 was missed; inspect occluded small people and rider composition before trusting prelabels | Original crop, rework XML, delta, findings |
| B1-center / 056040 | One unmatched Pedestrian L3+M4; model Truck/ThreeWheeler confusion and rider fragments | Separate a possible reference omission from a learner error; avoid score-driven deletion | Pedestrian conflict crop, R03, escalation ticket |

Only three frames and four represented classes contribute to these metrics. No Bus/Truck performance estimate can be inferred from their absence. Repeated frames from one camera are not independent fleet samples. The labels were initialized from the same frozen model, so L/M agreement is dependent.

## Hypothetical four-camera coverage

Use the eight strata in 45_sampling_plan.csv. Split by drive/scene before sampling; avoid counting adjacent frames of the same event as independent cases. Select candidates with a reproducible seed, then audit coverage by lighting, weather, occlusion, parking context and seam participation. Reserve 20 normal + 30 hard per camera: equal camera coverage is a planning assumption because no real four-camera error frequencies are supplied. Hard-case enrichment finds failures but does not estimate natural-population error rates; keep sampling probabilities if later weighting is required.
