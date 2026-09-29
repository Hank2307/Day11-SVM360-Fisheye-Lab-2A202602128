# Parking observations

Source: team CVAT export, corrected with assistant help and leader authorization. The original export is preserved locally. The submitted version is parking/annotations.xml.

- Selected dividers: six visible painted segments across the middle row. For example, the left divider runs approximately (59,521) to (49,569), and the next diagonal runs (175,522) to (245,564). Both divide adjacent parking bays. The remaining four follow the visible receding bay dividers.
- Excluded marking: the original seventh polyline connected (0,542) to (960,506). It did not trace a continuous visible painted bay divider and was removed; the fact that it crossed a parking lot was insufficient. The fence/vegetation boundary was also excluded.
- Free-space: a conservative visible section of the aisle between the middle row of parking bays and the foreground row, bounded by (110,585), (545,560), (665,603), (270,628). Its endpoints intentionally stop short of the marked bays, foreground paint, and image boundaries. This is a partial region, not an exhaustive aisle segmentation; the straight polygon edges are selection boundaries, not claimed physical curbs.
- Occlusion: no car, vegetation, curb or hidden ground lies inside the selected region. The distant red car is outside it. Free-space here is an image observation, not a drivable-area or safety certification.
- Remaining uncertainty: perspective does not uniquely identify the full aisle boundary. The selected patch is deliberately interior; no inferred continuation beyond the visible patch is labeled. Geometric acceptance remains a human grading decision.

See screenshots/parking_corrected_preview.jpg. Six polylines and one polygon meet the minimum counts; counts alone do not establish quality.
