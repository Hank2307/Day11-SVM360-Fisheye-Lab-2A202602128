# Error analysis card

## Zone × block

| zone | block | what | count |
|---|---|---|---:|
| center | B1 | IGNORE_SCOPE | 1 |
| center | B1 | MISSING | 5 |
| center | B1 | SPURIOUS | 6 |
| center | B2 | ATTRIBUTE | 1 |
| center | B2 | WRONG_CLASS | 1 |
| center | C0 | MISSING | 1 |
| center | C0 | SPURIOUS | 1 |
| edge | B1 | MISSING | 2 |
| edge | B1 | SPURIOUS | 5 |
| mid | B1 | MISSING | 4 |
| mid | B1 | SPURIOUS | 7 |
| mid | B2 | WRONG_CLASS | 1 |
| mid | C0 | WRONG_CLASS | 1 |
| unknown | B2 | MISSING | 1 |

## Top defects
- SPURIOUS: 19 (ví dụ frame adasind_019560.jpg)
- MISSING: 13 (ví dụ frame adasind_086220.jpg)
- WRONG_CLASS: 3 (ví dụ frame adasind_062370.jpg)

## Phân tích của bạn

The counts above are finding rows, not unique confirmed defects: a case may appear in craft and diagnosis, and a model class mismatch can create both missing and spurious cells. They must not be interpreted as independent failure rates.

The missing small pedestrian in 006840 R7 was confirmed on the original crop and added in rework by the annotator role with assistant help. Small visible extent beside a rider made it easy to miss during prelabel review; this is an evidence-supported annotator omission, not proof of a model-domain cause. See screenshots/006840_missing_pedestrian.png and R01.

For 056040 L3+M4, retain E5_unresolved: a light-shirted figure is visible, but blur and overlap make identity uncertain. QA/coach should adjudicate the crop under R03; see screenshots/056040_pedestrian_conflict.png. Do not treat L/M agreement as independent because both share model provenance.

The team specifically reports confusion over ThreeWheeler versus Truck, lens-border placement and small protruding ego parts such as a foot. A separate class/rider pass and full-contour ego pass are proposed improvements.
