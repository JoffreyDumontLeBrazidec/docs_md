# manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16

Generated (UTC): `2026-04-23T13:05:45Z`

## Snapshot
- Summary: Sampler sweep finalist (piecewise21) on 59e40596 300k checkpoint.
- Comparison note: na
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.963081`
- Franklin TC extreme score: `0.964164`
- ENFO deviation: `0.075433`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.971849`
- Spectra 10v score vs ENFO O320: `0.971103`
- Spectra 2t score vs ENFO O320: `0.956937`
- Spectra mean score (10u/10v/2t): `0.966629`
- Spectra 10u distance: `0.028151`
- Spectra 10v distance: `0.028897`
- Spectra 2t distance: `0.043063`
- Spectra mean distance: `0.033371`
- Spectra coverage: `30 pairs`
- Surface 10v nMSE: `0.267682`
- Surface 2t nMSE: `0.006111`
- Surface MSLP nMSE: `0.048357`
- Surface SP nMSE: `0.000939`
- Surface weighted MSE: `10587.422618`
- Surface weighted nMSE: `0.095226`
- Surface loss source: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/surface_loss_summary.json`
- Validation loss: `0.060484`
- Validation loss source: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16_sigma_eval.csv#sigma=1`

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
- Eval: `piecewise21`
- Sampling: `S_churn=2.5, S_max=1000.0, S_min=0.75, S_noise=1.05, high_schedule_type=exponential, low_schedule_type=karras, num_steps=21, num_steps_high=5, num_steps_low=16, rho=7.0, sampler=heun, schedule_type=experimental_piecewise, sigma_max=1000.0, sigma_min=0.03, sigma_transition=10.0`
- Extra args source: `experiment_config.sampling_config_json`
- Training noise: `na`

## Evaluation Artifacts
- Task note: `na`
- Artifacts root: `na`
- TC source: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/tc_normed_pdfs_idalia_franklin_manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16_from_predictions.stats.json`
- Idalia TC experiment key: `manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16`
- Franklin TC experiment key: `manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16`
- Spectra source: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/spectra_proxy10_subset_ecmwf/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/surface_loss_summary.json`
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
  "schedule_type": "experimental_piecewise",
  "sigma_max": 1000.0,
  "sigma_min": 0.03,
  "sigma_transition": 10.0
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/tc_normed_pdfs_idalia_franklin_manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16_from_predictions.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/spectra_proxy10_subset_ecmwf/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16/surface_loss_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_59e40596_new_o96_o320_20260422_pw21_t10_h5_l16_sigma_eval.csv`

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
