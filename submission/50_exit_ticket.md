# Exit ticket

1. Two boxes for the same object in overlapping cameras can both be valid per-camera annotations. They are not automatically DUPLICATE. Declare whether output is per-camera, BEV or fused objects, then define overlap/identity policy before evaluation.

2. Within one camera, retain track identity while evidence supports the same physical object; add keyframes at significant shape/position changes. Use Outside when the object leaves the field of view according to task policy. Do not equate temporary occlusion with a new identity. Cross-camera association additionally needs synchronized timestamps, calibrated overlap geometry and an agreed identity/output policy.

3. The team reports learning from confusion between ThreeWheeler and Truck, checking the lens border, and including small visible ego parts such as a protruding foot. A more explicit pass for vehicle class and the complete ego outline would improve the next review. Assistant-documented case for discussion: 056040 L3+M4 remains a possible separate pedestrian although the teaching reference has no match. The label is retained with an escalation rather than deleted to improve the score.

Answers 1–2 and the case summary were drafted with AI assistance; they are not a claim of an independently written student reflection.
