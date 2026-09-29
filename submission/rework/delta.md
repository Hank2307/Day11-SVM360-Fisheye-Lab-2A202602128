# Rework delta

| zone | matched before | matched after | missing before | missing after | spurious before | spurious after |
|---|---:|---:|---:|---:|---:|---:|
| center | 10 | 10 | 0 | 0 | 0 | 0 |
| mid | 6 | 7 | 1 | 0 | 1 | 1 |
| edge | 3 | 3 | 0 | 0 | 0 | 0 |

## Findings action=rework
- adasind_006840.jpg R7 MISSING: đã sửa
- adasind_006840.jpg R7 MISSING: đã sửa

Added one Pedestrian box at (74,831)-(91,879) after inspecting the original image. Matched count increases 19 to 20; missing decreases 1 to 0; spurious remains 1. The unresolved 056040 pedestrian is retained. Original r1 lock is unchanged. The two rework lines above refer to the same object recorded in two rounds, not two fixes.
