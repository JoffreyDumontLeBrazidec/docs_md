---
doc_type: lane-hub
lane: o320-o1280
vault_target: /home/ecm5702/hpcperm/docs/exp/o320_o1280
updated_utc: 2026-04-23T12:34:00Z
tags:
  - o1280
  - o320-o1280
  - inference
  - future-viz
---
# o320_o1280

Status: active
Owner: ecm5702
Last Updated (UTC): 2026-04-23
Source Links:
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/checkpoint-eval-pipeline/checkpoint-dossiers/f03c9e.md`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/checkpoint-eval-pipeline/in-progress/20260325_da4d_o320_o1280_proxy10pair_manual_eval.md`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/o1280-first-runs/in-progress/20260310_o1280_250k_fork_reset_from_f03c9e.md`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/instructions/vault-publishing.md`

## Summary
This hub collects the durable `o320 -> o1280` inference surfaces that are most useful for later visualization work in the Obsidian vault tree at `/home/ecm5702/hpcperm/docs/exp/o320_o1280/`.

## Rooms
| room | status | purpose | source |
| --- | --- | --- | --- |
| [`181be03e-full25`](181be03e-full25/README.md) | `completed` | 200k checkpoint full25 eval, lean PDF bundle layout, sigma pending | `/home/ecm5702/perm/eval/manual_181be03e_new_o320_o1280_20260421_manual_eval` |
| [`f03c9e-full25`](f03c9e-full25/README.md) | `completed` | stable Aug 26-30 `full25` predictions plus TC and trusted ECMWF spectra | `/home/ecm5702/perm/eval/manual_f03c9e_100k_full25_20260309_yfix1` |
| [`da4d902b-proxy-watch`](da4d902b-proxy-watch/README.md) | `in-progress` | latest `step_013872` proxy-like run watch surface; no predictions written yet | `/home/ecm5702/perm/eval/manual_da4d902b_new_o320_o1280_20260325_proxy10pair_m1_step013872` |

## Future-viz hooks
- Prediction NetCDFs are exposed from the stable `f03c9e` room under `links/data/predictions/`.
- Spectra summaries and PDF bundles are exposed under the stable room's `links/artifacts/spectra_ecmwf/`.
- Idalia TC stats JSON is exposed under the stable room's `links/artifacts/tc_idalia_regridded/`.
- Existing intermediate local-plot PNGs are copied into the stable room's `previews/` gallery for quick glanceable browsing.
- The pending `da4d902b` watch room already records the checkpoint, run roots, job lineage, and failed-attempt logs so the next publish refresh can add real outputs in place.
