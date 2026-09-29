# Proposed gold set — hypothetical four-camera scenario

Choose 200 frames from a hypothetical 50,000-frame pool using 45_sampling_plan.csv. No such pool is present in this repository; these are proposed procedures, not completed data collection.

| camera_id | Normal / hard examples | Likely difficulty | Space and calibration retained | Independent review |
|---|---|---|---|---|
| front | Clear traffic / crossing people and front-side seams | Small people, rider grouping | Raw frame, camera ID, timestamp, intrinsics, distortion model, extrinsics, calibration version | Anh labels, Hải reviews without prelabels/reference, Mạnh adjudicates |
| rear | Clear parking / reversing scene, low obstacles and rear-side seams | Occlusion, sparse visible extent | Same raw/calibration metadata; retain any BEV transform separately | Hải labels, Mạnh reviews, Anh adjudicates |
| left | Clear side traffic / close riders at distorted edge | Truncation and occlusion confusion | Same metadata and original image dimensions | Mạnh labels, Anh reviews, Hải adjudicates |
| right | Clear curb / pedestrians behind parked vehicles | Missed people, class ambiguity | Same metadata and native annotation space | Anh labels, Mạnh reviews, Hải adjudicates |

Sampling: deduplicate adjacent timestamps and scenes; select normal frames randomly within each camera and hard frames by declared criteria. Record seed, source drive, inclusion reason and exclusion decisions. Preserve 20 normal and 30 hard per camera, all eight cells positive, total 200.

Before calling the set gold, two people independently annotate every selected frame, inspect disagreements on originals, record decisions with rule versions, and ask the coach to resolve disagreements the third reviewer cannot settle. Agreement alone is insufficient: sample agreements for shared bias and check missing objects. This describes a future process; the present collaborative labels are not certified gold.

Seam example: one pedestrian appears in front and right cameras simultaneously. Keep both valid per-camera boxes. Link identity only after synchronized timestamps, calibration/overlap geometry and output policy support it; do not delete one as a duplicate. BEV/fused-object annotations need a separately declared coordinate space and policy.

Refresh after camera replacement, moved mount, calibration drift, resolution/crop changes, new environment distribution, or revised rider/ignore policy. Version old and new sets; re-review affected examples and keep a stable regression subset. Current single-camera teaching reference and peer agreement cannot establish four-camera coverage or correctness.
