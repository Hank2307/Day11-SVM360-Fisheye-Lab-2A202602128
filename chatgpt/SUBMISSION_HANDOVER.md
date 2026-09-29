# Team lab handover

Team: Phạm Hoàng Anh 02128 (leader), Đỗ Lý Minh Hải 02073, Lê Đức Mạnh 02122. The leader reports coach authorization for one shared repository with all three contributors.

## Evidence and provenance

- Original dataset and lab tooling are unchanged.
- AI drafts were initialized from assets/model-yolo26m.xml and visually edited, then all 48 frames were divided 16 per member for manual correction. Members report completing all nine checks and cross-checking collaboratively.
- User-returned exports: chatgpt/annotation_final/{HoangAnh,Hai,Manh}.zip. Backups preserve the two exports before removal of erroneous ego_body regions in 006840/271039.
- Official grading pipeline uses the leader B1-center slice; C0 and other team slices were extracted without changing shapes. Task metadata was normalized during extraction.
- C0 was extracted retrospectively, not independently annotated before the main task. No separate blind student review is claimed. Earlier student reference exposure was not explicitly confirmed; lock-before-reveal describes the tool operation only.
- Assistant audit of B2-center is recorded in submission/r2_qa. Some peer-slice concerns remain for adjudication; see qa_review.md. No claim is made that all 48 frames are error-free.
- Immutable r1 snapshot is in submission/r1_craft. Authoritative leader rework is submission/rework/annotations-v2.xml: one additional small pedestrian in 006840. The original 48-frame member exports do not include this later addition.
- The reference is teaching material, not gold. The model comparison is not an independent test because prelabels shared its provenance.
- Evidence PNGs in submission/screenshots are rendered original-image crops, not screenshots of the CVAT application.
- K12 and stretch are explicitly omitted; no fill-ratio measurement is claimed.

## Parking correction

The returned parking_final.zip contains seven polylines and one polygon. Lines 1–6 follow visible bay dividers. Line 7 spans the image without following a visible divider; polygon 8 covers the row of marked bays rather than an established driving aisle. The leader authorized assistant correction. Line 7 was removed and a conservative interior aisle patch replaced polygon 8. chatgpt/parking_corrected.zip is the corrected export; the original ZIP is preserved. The preview was shown to the team; no separate post-correction student acceptance is claimed.

## Commands

Use Anaconda base Python. For environment checks set CVAT_URL=http://localhost:8100 and PYTHONIOENCODING=utf-8. Run lab11.py check after finalizing parking and observations. A structural pass is not a quality grade.

## Final human actions

Review the corrected parking geometry; adjudicate the documented uncertain pedestrian/class cases if the coach requires it; confirm whether collaborative QA is accepted in place of the separate blind review; submit the GitHub repository link through the course channel. No messages have been sent to the coach by the assistant.
