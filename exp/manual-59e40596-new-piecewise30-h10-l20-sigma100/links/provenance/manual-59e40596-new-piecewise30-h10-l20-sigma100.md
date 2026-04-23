# manual_59e4_300k

Generated (UTC): `2026-04-23T13:05:45Z`

## Snapshot
- Summary: Baseline pw30 evaluation of the imported 59e40596 300k checkpoint.
- Comparison note: na
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.966706`
- Franklin TC extreme score: `0.969437`
- ENFO deviation: `0.041250`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.976465`
- Spectra 10v score vs ENFO O320: `0.980711`
- Spectra 2t score vs ENFO O320: `0.984856`
- Spectra mean score (10u/10v/2t): `0.980678`
- Spectra 10u distance: `0.023535`
- Spectra 10v distance: `0.019289`
- Spectra 2t distance: `0.015144`
- Spectra mean distance: `0.019322`
- Spectra coverage: `50 pairs`
- Surface 10v nMSE: `0.267161`
- Surface 2t nMSE: `0.006098`
- Surface MSLP nMSE: `0.048352`
- Surface SP nMSE: `0.000939`
- Surface weighted MSE: `10588.762470`
- Surface weighted nMSE: `0.094995`
- Surface loss source: `/home/ecm5702/perm/eval/manual_59e4_300k/surface_loss_summary.json`
- Validation loss: `0.060472`
- Validation loss source: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_59e4_300k_sigma_eval.csv#sigma=1`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `new`
- Venv: `na`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `na`
- Checkpoint ID: `59e40596023d4f72a1c5e2027805d7df`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/59e40596023d4f72a1c5e2027805d7df/anemoi-by_epoch-epoch_260-step_300000.ckpt`
- Dates: `20230826, 20230827, 20230828, 20230829, 20230830`
- Members: `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`
- Steps (hours): `24, 48, 72, 96, 120`
- Eval: `piecewise30`
- Sampling: `S_churn=2.5, S_max=100000.0, S_min=0.75, S_noise=1.05, high_schedule_type=exponential, low_schedule_type=karras, num_steps=30, num_steps_high=10, num_steps_low=20, rho=7.0, sampler=heun, schedule_type=experimental_piecewise, sigma_max=100000.0, sigma_min=0.03, sigma_transition=100.0`
- Extra args source: `experiment_config.sampling_config_json`
- Training noise: `na`

## Evaluation Artifacts
- Task note: `na`
- Artifacts root: `na`
- TC source: `/home/ecm5702/perm/eval/manual_59e4_300k/tc_normed_pdfs_idalia_franklin_manual_59e4_300k_from_predictions.stats.json`
- Idalia TC experiment key: `manual_59e4_300k`
- Franklin TC experiment key: `manual_59e4_300k`
- Spectra source: `/home/ecm5702/perm/eval/manual_59e4_300k/spectra_step120_5dates_m10/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_59e4_300k/surface_loss_summary.json`
- Exact extra_args:
```json
{
  "S_churn": 2.5,
  "S_max": 100000.0,
  "S_min": 0.75,
  "S_noise": 1.05,
  "high_schedule_type": "exponential",
  "low_schedule_type": "karras",
  "num_steps": 30,
  "num_steps_high": 10,
  "num_steps_low": 20,
  "rho": 7.0,
  "sampler": "heun",
  "schedule_type": "experimental_piecewise",
  "sigma_max": 100000.0,
  "sigma_min": 0.03,
  "sigma_transition": 100.0
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_59e4_300k/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_59e4_300k/tc_normed_pdfs_idalia_franklin_manual_59e4_300k_from_predictions.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_59e4_300k/spectra_step120_5dates_m10/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_59e4_300k/surface_loss_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_59e4_300k_sigma_eval.csv`

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
