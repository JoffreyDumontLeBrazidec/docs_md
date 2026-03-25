---
doc_type: experiment-room
lane: o320-o1280
slug: da4d902b-proxy-watch
status: in-progress
checkpoint_family: da4d902b71084ecc884a938c4b8930d3
canonical_repo_source: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/o320_o1280/da4d902b-proxy-watch/README.md
vault_target: /home/ecm5702/hpcperm/docs/exp/o320_o1280/da4d902b-proxy-watch/README.md
run_root: /home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872
tags:
  - o1280
  - o320-o1280
  - inference
  - proxy-like
  - in-progress
  - future-viz
---
# da4d902b proxy watch

Status: in-progress
Owner: ecm5702
Last Updated (UTC): 2026-03-25
Source Links:
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/checkpoint-eval-pipeline/in-progress/20260325_da4d_o320_o1280_proxy10pair_manual_eval.md`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/checkpoint-eval-pipeline/completed-tasks/20260325_o320_o1280_weak_agent_manual_eval_hardening.md`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/o1280-first-runs/in-progress/20260310_o1280_250k_fork_reset_from_f03c9e.md`

## What this is
This room is the watch surface for the latest `da4d902b71084ecc884a938c4b8930d3` `o320 -> o1280` proxy-like manual inference. It exists so future visualization work already has a stable landing place even before the canonical rerun writes prediction files.

> GitHub/Obsidian note:
> current `links/` entries point to the frozen checkpoint, failed-attempt logs, and provenance notes. The canonical `_r1` rerun root does not exist yet.

## Identity
- checkpoint family / child run: `da4d902b71084ecc884a938c4b8930d3`
- frozen checkpoint file: [`anemoi-by_epoch-epoch_002-step_013872.ckpt`](links/data/anemoi-by_epoch-epoch_002-step_013872.ckpt)
- lane: `o320-o1280`
- scope: `10` proxy-like date/step pairs, member `1`
- initial run root: `/home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872`
- canonical rerun root: `/home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872_r1`
- sampling: `{"num_steps":40,"sigma_max":1000.0,"sigma_min":0.03,"rho":7.0,"sampler":"heun","S_max":1000.0}`

## Current status
- No prediction files have been written yet.
- The first ad hoc chain created the initial run root and `EXPERIMENT_CONFIG.yaml`, but every predict attempt failed before producing `predictions_*.nc`.
- The canonical rerun chain from `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/downscaling-tools/eval/jobs/templates/submit_o320_o1280_manual_eval_flow.sh` was still scheduler-held at the latest captured note.

## Attempt history
| job | state at latest note | meaning |
| --- | --- | --- |
| `50029754` | `failed` | initial predict attempt hit broken nested quoting for `--extra-args-json` |
| `50029758` | `failed` | single-GPU OOM (`torch.OutOfMemoryError`) |
| `50029762` | `failed` | launched without matching multi-rank distributed posture (`Expected world_size=4, got 1`) |
| `50029786` | `pending` | canonical `_r1` predict rerun from the hardened helper |
| `50029787` | `dependency` | local plots after `50029786` |
| `50029788` | `dependency` | proxy spectra after `50029786` |
| `50029789` | `dependency` | native TC after `50029786` |

## Planned future-viz hooks
- `/home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872_r1/predictions/`
- `/home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872_r1/logs/`
- `/home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872_r1/EXPERIMENT_CONFIG.yaml`
- downstream local plots, proxy spectra, and native TC outputs after the first successful prediction write

## Current provenance and logs
- initial experiment config: [`EXPERIMENT_CONFIG.yaml`](links/data/EXPERIMENT_CONFIG.yaml)
- live task note: [`20260325_da4d_o320_o1280_proxy10pair_manual_eval.md`](links/provenance/20260325_da4d_o320_o1280_proxy10pair_manual_eval.md)
- hardening note: [`20260325_o320_o1280_weak_agent_manual_eval_hardening.md`](links/provenance/20260325_o320_o1280_weak_agent_manual_eval_hardening.md)
- training lineage note: [`20260310_o1280_250k_fork_reset_from_f03c9e.md`](links/provenance/20260310_o1280_250k_fork_reset_from_f03c9e.md)
- failed attempt logs:
  - [`predict_proxy10_50029754.out`](links/logs/predict_proxy10_50029754.out)
  - [`predict_proxy10_50029758.out`](links/logs/predict_proxy10_50029758.out)
  - [`predict_proxy10_50029762.out`](links/logs/predict_proxy10_50029762.out)
