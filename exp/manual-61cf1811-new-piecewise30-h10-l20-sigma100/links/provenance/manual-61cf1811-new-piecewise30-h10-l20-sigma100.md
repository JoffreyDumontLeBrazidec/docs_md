# manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total

Generated (UTC): `2026-03-24T16:37:33Z`

## Snapshot
- Summary: Direct member-1 proxy10total run for the piecewise30 reference sampler.
- Comparison note: Direct proxy10total row using the canonical 10 late-August pairs with member 1 only and the explicit piecewise30 `(10/20)` sampler override, launched separately so fast proxy results do not wait on the full Aug26-30 run.
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.716516`
- Franklin TC extreme score: `0.746305`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.952404`
- Spectra 10v score vs ENFO O320: `0.947028`
- Spectra 2t score vs ENFO O320: `0.973018`
- Spectra mean score (10u/10v/2t): `0.957483`
- Spectra 10u distance: `0.047596`
- Spectra 10v distance: `0.052972`
- Spectra 2t distance: `0.026982`
- Spectra mean distance: `0.042517`
- Spectra coverage: `10 curves`
- Surface weighted MSE: `3990.344360`
- Surface loss source: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/surface_loss_summary.json`
- Validation loss: `na`
- Validation loss source: `na`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `new`
- Venv: `/home/ecm5702/dev/.ds-dyn/bin/activate`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `31457433, 31457440, 31464922`
- Checkpoint ID: `61cf18112f9f4e5da192ae930b40aa79`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/61cf18112f9f4e5da192ae930b40aa79/anemoi-by_epoch-epoch_021-step_100000.ckpt`
- Dates: `20230827, 20230828, 20230829, 20230830`
- Members: `1`
- Steps (hours): `24, 48, 72`
- Eval (schedule+steps): `piecewise30`
- Sampling: `schedule_type=experimental_piecewise, high_schedule_type=exponential, low_schedule_type=karras, num_steps=30, num_steps_high=10, num_steps_low=20, sigma_min=0.03, sigma_transition=100.0, sigma_max=100000.0, sampler=heun`
- Extra args source: `manifest.extra_args`
- Training noise: `New-stack checkpoint family; exact training-noise metadata still needs a trusted training-side source.`

## Evaluation Artifacts
- Task note: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_61cf1811_piecewise30_reference_sampler.md`
- Artifacts root: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- TC source: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset_20260320/tc_normed_pdfs_idalia_franklin_61cf1811_piecewise30_proxy10total_strict_20260320.stats.json`
- Idalia TC experiment key: `manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total_20260320`
- Franklin TC experiment key: `manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total_20260320`
- Spectra source: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total_20260320/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/surface_loss_summary.json`
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
- Artifact path: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- Artifact path: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_61cf1811_piecewise30_reference_sampler.md`
- Artifact path: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset_20260320/tc_normed_pdfs_idalia_franklin_61cf1811_piecewise30_proxy10total_strict_20260320.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total_20260320/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/surface_loss_summary.json`

## What Worked
- The proxy-first path was split cleanly from the still-running full Aug26-30 evaluation, so fast results no longer depended on full-run file order.
- The repaired proxy bundle now has canonical strict TC stats and a 10-curve spectra summary for the standing proxy scoreboard.

## What Did Not
- The first proxy post-step forgot to load `ecmwf-toolbox` before the regridded TC stage, so a repair job was needed.
- This is a fast-screen row, not the production full25 row.

## Why Better Or Not Better Yet
- no comparative claim recorded yet

## Caveats
- none recorded yet

## Ideas
- Use this as the direct proxy reference for the piecewise30 sampler while the full Aug26-30 run continues separately.
