# QA review · B2-center

Snapshot code: A45D-8B75. Source: Hai.zip, reviewed team export, extracted without changing shapes.

The team reports collaborative cross-checking during annotation. The following additional observations were made by the assistant against original-image overlays before opening the teaching reference. This is not a claim of independent blind student QA: the assistant also prepared the original model-assisted draft.

| frame | object_ref | rule_id | observation |
|---|---|---|---|
| adasind_062370.jpg | L4 | R04 | Passenger van is correctly Car; retain this mapping rather than Bus. |
| adasind_086220.jpg | unboxed vehicle near x225 y995 | R01 | A dark three-wheeler around x200–250 y950–1040 appears unboxed and taller than 40 px; needs correction. |
| adasind_086220.jpg | L1 | R03 | Small center object labeled Car appears to be a rider/two-wheeler; request a zoomed human check before changing class. |
| adasind_117120.jpg | L5 | R03 | Person adjacent to the three-wheeler has a separate Pedestrian box; check standing outside versus seated inside before retaining. |

Response: retain van mapping; send the three uncertain/missing-object observations to the team. These are supporting peer-slice issues; they do not alter the leader B1-center metrics.
