# Zone table (slice của bạn)

Lệnh `python3 lab11.py model` tự ghi bảng số (cùng cách đếm với `r1_craft/compare.md` và `model_compare.md`); chạy lại lệnh sẽ cập nhật bảng và giữ nguyên phần nhận xét. Bạn chỉ viết mục Nhận xét.

| Zone | n_ref | L missing | L spurious | M missing (`LR_noM` + `R_only`) | M thừa (`LM_noR` + `M_only`) | Lỗi L chính (`what`) |
|---|---:|---:|---:|---:|---:|---|
| center | 10 | 0 | 0 | 5 | 6 | — |
| mid | 7 | 1 | 1 | 3 | 6 | MISSING (1) |
| edge | 3 | 0 | 0 | 2 | 5 | — |

## Nhận xét

Learner discrepancies are concentrated in mid (1 missing, 1 spurious); center and edge have none at IoU 0.5. Model absolute missing count is highest at center (5), while spurious counts tie center/mid (6 each). Edge has only three reference objects, so its proportions are unstable.

Rider fragments, class mapping of three-wheelers and small occluded people are visible failure mechanisms. Fisheye distortion is a hypothesis to test, not an established model-domain cause. Three frames, threshold choice, reference uncertainty and model-derived initialization limit generalization. IoU 0.7 reduces learner geometric matches from 19 to 15; 0.3 and 0.5 both give 19. A match is not necessarily class-correct in all reports.
