# manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot

Generated (UTC): `2026-03-24T16:37:33Z`

## Snapshot
- Summary: Corrected proxy10total row under the 10-total member-1 contract.
- Comparison note: Corrected proxy10total row using the canonical 10 late-August pairs with member 1 only.
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.911372`
- Franklin TC extreme score: `1.000000`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.952414`
- Spectra 10v score vs ENFO O320: `0.958627`
- Spectra 2t score vs ENFO O320: `0.973634`
- Spectra mean score (10u/10v/2t): `0.961558`
- Spectra 10u distance: `0.047586`
- Spectra 10v distance: `0.041373`
- Spectra 2t distance: `0.026366`
- Spectra mean distance: `0.038442`
- Spectra coverage: `10 curves`
- Surface weighted MSE: `10783.899057`
- Surface loss source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/surface_loss_summary.json`
- Validation loss: `na`
- Validation loss source: `na`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `old`
- Venv: `/home/ecm5702/dev/.ds-old/bin/activate`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `na`
- Checkpoint ID: `56b6c4e2a6064878841dba0635c7be44`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/56b6c4e2a6064878841dba0635c7be44/last.ckpt`
- Dates: `20230827, 20230828, 20230829, 20230830`
- Members: `1`
- Steps (hours): `24, 48, 72`
- Eval (schedule+steps): `piecewise30`
- Sampling: `schedule_type=experimental_piecewise, schedule_kind=piecewise30, high_schedule_type=exponential, low_schedule_type=karras, num_steps=30, num_steps_high=10, num_steps_low=20, sigma_min=0.03, sigma_transition=100.0, sigma_max=100000.0, rho=7.0, sampler=heun, S_churn=2.5, S_min=0.75, S_max=100000.0, S_noise=1.05`
- Extra args source: `manifest.extra_args`
- Training noise: `Old-stack piecewise/classic baseline with strict late-August manual evaluation complete.`

## Evaluation Artifacts
- Task note: `na`
- Artifacts root: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot`
- TC source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/proxy10total_subset_20260318/tc_normed_pdfs_idalia_franklin_56b6c4e2_proxy10total_strict_20260318.stats.json`
- Idalia TC experiment key: `manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot_proxy10total_20260318`
- Franklin TC experiment key: `manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot_proxy10total_20260318`
- Spectra source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/spectra_harmonized_proxy10total_20260318/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/surface_loss_summary.json`
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
  "schedule_kind": "piecewise30",
  "schedule_type": "experimental_piecewise",
  "sigma_max": 100000.0,
  "sigma_min": 0.03,
  "sigma_transition": 100.0
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/proxy10total_subset_20260318/tc_normed_pdfs_idalia_franklin_56b6c4e2_proxy10total_strict_20260318.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/spectra_harmonized_proxy10total_20260318/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot/surface_loss_summary.json`

## What Worked
- Uses the corrected 10-total proxy contract instead of the superseded 10x10 policy.
- Carries scoreboard-native TC stats plus direct spectra summary from the member-1 subset predictions.

## What Did Not
- This is a fast-screen row, not the old full25 production contract.

## Why Better Or Not Better Yet
- Better than the legacy j2hh manual row for clean-scoreboard use because this run is already spectra-complete.

## Caveats
- none recorded yet

## Ideas
- Use this bundle as the clean standing proxy10total comparison surface.
