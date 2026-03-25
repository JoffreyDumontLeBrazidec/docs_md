# manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total

Generated (UTC): `2026-03-24T16:37:33Z`

## Snapshot
- Summary: Direct proxy10total row for the cfec83 piecewise sampler with strict member-1 TC and spectra artifacts.
- Comparison note: Dedicated proxy10total run using the canonical 10 late-August pairs with member 1 only and the piecewise30 sampler override.
- Role: `experiment`
- Contract status: `mismatch`
- Contract detail: dates: expected [20230827, 20230828, 20230829, 20230830], got [20230829, 20230828, 20230830, 20230827]
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.654797`
- Franklin TC extreme score: `0.804913`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.967998`
- Spectra 10v score vs ENFO O320: `0.963923`
- Spectra 2t score vs ENFO O320: `0.974774`
- Spectra mean score (10u/10v/2t): `0.968898`
- Spectra 10u distance: `0.032002`
- Spectra 10v distance: `0.036077`
- Spectra 2t distance: `0.025226`
- Spectra mean distance: `0.031102`
- Spectra coverage: `10 curves`
- Surface weighted MSE: `3900.165095`
- Surface loss source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/surface_loss_summary.json`
- Validation loss: `na`
- Validation loss source: `na`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `new`
- Venv: `/home/ecm5702/dev/.ds-dyn/bin/activate`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `na`
- Checkpoint ID: `cfec83a3cd0644778e2bfcbacfa9f4fc`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/last.ckpt`
- Dates: `20230829, 20230828, 20230830, 20230827`
- Members: `1`
- Steps (hours): `24, 48, 72`
- Eval (schedule+steps): `piecewise30`
- Sampling: `schedule_type=experimental_piecewise, schedule_kind=experimental_piecewise, high_schedule_type=exponential, low_schedule_type=karras, num_steps=30, num_steps_high=10, num_steps_low=20, sigma_min=0.03, sigma_transition=100.0, sigma_max=100000.0, rho=7.0, sampler=heun, S_churn=2.5, S_min=0.75, S_max=100000.0, S_noise=1.05`
- Extra args source: `manifest.extra_args`
- Training noise: `New-stack checkpoint family; exact training-noise metadata still needs a trusted training-side source.`

## Evaluation Artifacts
- Task note: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md`
- Artifacts root: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- TC source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total_strict.stats.json`
- Idalia TC experiment key: `manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- Franklin TC experiment key: `manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- Spectra source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/surface_loss_summary.json`
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
  "schedule_kind": "experimental_piecewise",
  "schedule_type": "experimental_piecewise",
  "sigma_max": 100000.0,
  "sigma_min": 0.03,
  "sigma_transition": 100.0
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- Artifact path: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total_strict.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/surface_loss_summary.json`

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
