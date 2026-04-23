# manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30

Generated (UTC): `2026-04-23T13:05:45Z`

## Snapshot
- Summary: Completed Aug26-30 stage1 piecewise21 rerun with TC, proxy10 ECMWF spectra comparison artifacts, surface-loss, sigma, and scoreboard metrics present.
- Comparison note: Full-contract evaluated piecewise21 row for the cfec83 checkpoint family; spectra rely on the proxy10 ECMWF comparison-summary fallback rather than the older step120 summary layout.
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.974236`
- Franklin TC extreme score: `0.968308`
- ENFO deviation: `0.053528`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.964681`
- Spectra 10v score vs ENFO O320: `0.965238`
- Spectra 2t score vs ENFO O320: `0.957922`
- Spectra mean score (10u/10v/2t): `0.962614`
- Spectra 10u distance: `0.035319`
- Spectra 10v distance: `0.034762`
- Spectra 2t distance: `0.042078`
- Spectra mean distance: `0.037386`
- Spectra coverage: `10u: step24/24 30c/100r; 10v: step24/24 30c/100r; 2t: step24/24 30c/100r; msl: step24/24 30c/80r; t_850: step24/24 30c/80r; z_500: step24/24 30c/80r`
- Surface 10v nMSE: `0.271363`
- Surface 2t nMSE: `0.006243`
- Surface MSLP nMSE: `0.048656`
- Surface SP nMSE: `0.000951`
- Surface weighted MSE: `10681.534065`
- Surface weighted nMSE: `0.096343`
- Surface loss source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/surface_loss_summary.json`
- Validation loss: `0.066421`
- Validation loss source: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30_sigma_eval.csv#sigma=1`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `new`
- Venv: `/home/ecm5702/dev/.ds-dyn/bin/activate`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `na`
- Checkpoint ID: `cfec83a3cd0644778e2bfcbacfa9f4fc`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/anemoi-by_epoch-epoch_043-step_200000.ckpt`
- Dates: `20230826, 20230827, 20230828, 20230829, 20230830`
- Members: `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`
- Steps (hours): `24, 48, 72, 96, 120`
- Eval: `piecewise21`
- Sampling: `schedule_type=experimental_piecewise, schedule_kind=stage1_piecewise, num_steps=21, sigma_max=1000.0, sigma_transition=10.0, sigma_min=0.03, high_schedule_type=exponential, low_schedule_type=karras, num_steps_high=5, num_steps_low=16, rho=7.0, sampler=heun, S_churn=2.5, S_min=0.75, S_max=1000.0, S_noise=1.05`
- Extra args source: `manifest.extra_args`
- Training noise: `New-stack checkpoint family; exact training-noise metadata still needs a trusted training-side source.`

## Evaluation Artifacts
- Task note: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/o96_o320_opti/in-progress/20260328_o96_o320_piecewise_scheduler_search.md`
- Artifacts root: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30`
- TC source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30_from_predictions.stats.json`
- Idalia TC experiment key: `manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30`
- Franklin TC experiment key: `manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30`
- Spectra source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/spectra_proxy10_subset_ecmwf/comparison_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/surface_loss_summary.json`
- Exact extra_args:
```json
{
  "S_churn": 2.5,
  "S_max": 1000.0,
  "S_min": 0.75,
  "S_noise": 1.05,
  "high_schedule_type": "exponential",
  "low_schedule_type": "karras",
  "num_steps": 21,
  "num_steps_high": 5,
  "num_steps_low": 16,
  "rho": 7.0,
  "sampler": "heun",
  "schedule_kind": "stage1_piecewise",
  "schedule_type": "experimental_piecewise",
  "sigma_max": 1000.0,
  "sigma_min": 0.03,
  "sigma_transition": 10.0
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30`
- Artifact path: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/o96_o320_opti/in-progress/20260328_o96_o320_piecewise_scheduler_search.md`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30_from_predictions.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/spectra_proxy10_subset_ecmwf/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30/surface_loss_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_cfec83a3_new_o96_o320_20260331_t10_h5_l16_scoreboard_aug26_30_sigma_eval.csv`

## What Worked
- none recorded yet

## What Did Not
- none recorded yet

## Why Better Or Not Better Yet
- no comparative claim recorded yet

## Caveats
- none recorded yet

## Ideas
- none recorded yet
