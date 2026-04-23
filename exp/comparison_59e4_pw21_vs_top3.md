# O96→O320 Comparison: 59e4 300k pw21 vs Top Performers

Generated (UTC): `2026-04-23T14:05:00Z`

## Selected Experiments

| Rank | Checkpoint | Stack | Steps | Sampler | Composite | TC | Spectra | CRPS | Surface nMSE |
|------|-----------|-------|-------|---------|-----------|-----|---------|------|-------------|
| 1 | 56b6c4e2 | old | 300k | pw30 | **0.9779** | 0.966 | **0.031** | 0.969 | 0.276 |
| 4 | cfec83a3 | new | 200k | pw21 | 0.9742 | 0.968 | 0.054 | 0.963 | 0.271 |
| 8 | 59e40596 | new | 300k | pw30 | 0.9667 | 0.969 | 0.041 | **0.981** | **0.267** |
| 13 | 59e40596 | new | 300k | pw21 | 0.9631 | 0.964 | 0.075 | 0.967 | 0.268 |

## Key Observations

- **Composite gap**: 59e4 300k trails the leader by ~1.5 points (0.963–0.967 vs 0.974–0.978).
- **Surface loss advantage**: 59e4 has the lowest surface nMSE (0.267), suggesting the extra 100k training steps improved pixel-level fidelity.
- **Spectra weakness**: 59e4 pw21 has the worst spectra score (0.075) in the selection. The pw30 sampler halves this gap (0.041).
- **CRPS strength**: 59e4 pw30 has the best CRPS (0.981) in the entire scoreboard, indicating good probabilistic calibration.
- **Sampler effect**: pw30 consistently outperforms pw21 across both checkpoints, with the largest gain in spectra.

## Experiment Rooms

- [[manual-56b6c4e2-old-piecewise30-h10-l20-sigma100|Rank 1: 56b6c4e2 pw30]]
- [[manual-cfec83a3-new-piecewise21-t10-h5-l16|Rank 4: cfec83a3 pw21]]
- [[manual-59e40596-new-piecewise30-h10-l20-sigma100|Rank 8: 59e40596 pw30]]
- [[manual-59e40596-new-piecewise21-t10-h5-l16|Rank 13: 59e40596 pw21]]

## Spectra Previews

### Rank 1: 56b6c4e2 pw30 (best spectra 0.031)
![[manual-56b6c4e2-old-piecewise30-h10-l20-sigma100/previews/spectra_10u_sfc_p01.png]]
![[manual-56b6c4e2-old-piecewise30-h10-l20-sigma100/previews/spectra_2t_sfc_p01.png]]

### Rank 8: 59e40596 pw30 (spectra 0.041)
![[manual-59e40596-new-piecewise30-h10-l20-sigma100/previews/spectra_10u_p01.png]]
![[manual-59e40596-new-piecewise30-h10-l20-sigma100/previews/spectra_2t_p01.png]]

### Rank 13: 59e40596 pw21 (spectra 0.075)
![[manual-59e40596-new-piecewise21-t10-h5-l16/previews/spectra_10u_sfc_p01.png]]
![[manual-59e40596-new-piecewise21-t10-h5-l16/previews/spectra_2t_sfc_p01.png]]

## TC Previews

### Rank 1: 56b6c4e2 pw30
![[manual-56b6c4e2-old-piecewise30-h10-l20-sigma100/previews/tc_normed_pdfs_idalia_franklin_56b6c4e2_full25_strict_20260317_p01.png]]

### Rank 8: 59e40596 pw30
![[manual-59e40596-new-piecewise30-h10-l20-sigma100/previews/tc_normed_pdfs_idalia_franklin_manual_59e4_300k_from_predictions_p01.png]]

### Rank 13: 59e40596 pw21
![[manual-59e40596-new-piecewise21-t10-h5-l16/previews/tc_normed_pdfs_idalia_franklin_manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16_from_predictions_p01.png]]

## Source

- Scoreboard: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard.md`
- Published hub: `/home/ecm5702/hpcperm/docs/published/scoreboard_o96_o320/`
