# manual_cfec83a3_new_o96_o320_20260320_oldlike200k

Generated (UTC): `2026-03-24T16:37:33Z`

## Snapshot
- Summary: Frozen member-1 proxy10total subset copied out of the March 20 run root.
- Comparison note: Corrected proxy10total row using the canonical 10 late-August pairs with member 1 only, frozen before the full25 continuation could overwrite the proxy files.
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.785289`
- Franklin TC extreme score: `0.700827`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.967958`
- Spectra 10v score vs ENFO O320: `0.966045`
- Spectra 2t score vs ENFO O320: `0.975564`
- Spectra mean score (10u/10v/2t): `0.969856`
- Spectra 10u distance: `0.032042`
- Spectra 10v distance: `0.033955`
- Spectra 2t distance: `0.024436`
- Spectra mean distance: `0.030144`
- Spectra coverage: `10 curves`
- Surface weighted MSE: `10646.679560`
- Surface loss source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/surface_loss_summary.json`
- Validation loss: `0.066412`
- Validation loss source: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_cfec83a3_new_o96_o320_20260320_oldlike200k_sigma_eval.csv#sigma=1`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `new`
- Venv: `/home/ecm5702/dev/.ds-dyn/bin/activate`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `31375341, 31375342, 31377164`
- Checkpoint ID: `cfec83a3cd0644778e2bfcbacfa9f4fc`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/last.ckpt`
- Dates: `20230827, 20230828, 20230829, 20230830`
- Members: `1`
- Steps (hours): `24, 48, 72`
- Eval (schedule+steps): `karras40`
- Sampling: `num_steps=40, rho=7.0, sampler=heun, sigma_max=1000.0, sigma_min=0.03, S_max=1000.0`
- Extra args source: `manifest.extra_args`
- Training noise: `New-stack oldlike200k candidate evaluated under the corrected proxy10total policy.`

## Evaluation Artifacts
- Task note: `na`
- Artifacts root: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
- TC source: `/home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/tc_normed_pdfs_idalia_franklin_cfec83a3_proxy10total_strict_20260320.stats.json`
- Idalia TC experiment key: `manual_cfec83a3_new_o96_o320_20260320_oldlike200k_proxy10total_20260320`
- Franklin TC experiment key: `manual_cfec83a3_new_o96_o320_20260320_oldlike200k_proxy10total_20260320`
- Spectra source: `/home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/spectra_harmonized_proxy10total_20260320/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/surface_loss_summary.json`
- Exact extra_args:
```json
{
  "S_max": 1000.0,
  "num_steps": 40,
  "rho": 7.0,
  "sampler": "heun",
  "sigma_max": 1000.0,
  "sigma_min": 0.03
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/tc_normed_pdfs_idalia_franklin_cfec83a3_proxy10total_strict_20260320.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/spectra_harmonized_proxy10total_20260320/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/surface_loss_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/scoreboards/sigma/manual_cfec83a3_new_o96_o320_20260320_oldlike200k_sigma_eval.csv`

## What Worked
- Frozen member-1 proxy files were preserved cleanly in repo scratch.
- Scoreboard-native TC and spectra artifacts now exist for the proxy10total contract.

## What Did Not
- The proxy gate itself still failed against the anchor comparison.
- This is a fast-screen row, not the production full25 row.

## Why Better Or Not Better Yet
- no comparative claim recorded yet

## Caveats
- Original run root is still being continued toward full25 elsewhere.

## Ideas
- none recorded yet
