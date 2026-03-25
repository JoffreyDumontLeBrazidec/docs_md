---
dossier_mode: generated
slug: manual-cfec83a3-new-karras40-oldlike200k
display_label: cfec83 k40 oldlike200k
role: experiment
checkpoint_id: cfec83a3cd0644778e2bfcbacfa9f4fc
checkpoint_path: /home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/last.ckpt
lane: o96-o320
stack_flavor: new
run_id: manual_cfec83a3_new_o96_o320_20260320_oldlike200k
run_root: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k
venv: /home/ecm5702/dev/.ds-dyn/bin/activate
login_node: null
qos: null
job_ids:
- 31375341
- 31375342
- 31377164
task_note: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md
experiment_config: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/EXPERIMENT_CONFIG.yaml
sampling:
  summary: schedule_type=karras, schedule_kind=karras, num_steps=40, sigma_min=0.03,
    sigma_max=1000.0, rho=7.0, sampler=heun, S_churn=2.5, S_min=0.75, S_max=1000.0,
    S_noise=1.05
  extra_args:
    schedule_kind: karras
    num_steps: 40
    sigma_max: 1000.0
    sigma_min: 0.03
    rho: 7.0
    sampler: heun
    S_churn: 2.5
    S_min: 0.75
    S_max: 1000.0
    S_noise: 1.05
    schedule_type: karras
surfaces:
  proxy10:
    status: recorded
    promotion: promoted
    rank: 4
    scope:
      dates:
      - 20230827
      - 20230828
      - 20230829
      - 20230830
      members:
      - 1
      steps_hours:
      - 24
      - 48
      - 72
    artifacts:
      tc_stats: /home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/tc_normed_pdfs_idalia_franklin_cfec83a3_proxy10total_strict_20260320.stats.json
      spectra_summary: /home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/spectra_harmonized_proxy10total_20260320/spectra_summary.json
      compare_json: null
      scoreboard_metrics: null
  aug_26_30:
    status: recorded
    promotion: promoted
    rank: 5
    scope:
      dates:
      - 20230826
      - 20230827
      - 20230828
      - 20230829
      - 20230830
      members:
      - 1
      - 2
      - 3
      - 4
      - 5
      - 6
      - 7
      - 8
      - 9
      - 10
      steps_hours:
      - 24
      - 48
      - 72
      - 96
      - 120
    artifacts:
      sigma_csv: /home/ecm5702/perm/eval/scoreboards/sigma/manual_cfec83a3_new_o96_o320_20260320_oldlike200k_sigma_eval.csv
      tc_stats: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.stats.json
      spectra_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/spectra_step120_5dates_m10_ecmwf/spectra_summary.json
      comparison_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/spectra_step120_5dates_m10_ecmwf/comparison_summary.json
      surface_loss_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/surface_loss_summary.json
vault_published: true
vault_published_at: '2026-03-25T19:38:30Z'
vault_source_dossier: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-cfec83a3-new-karras40-oldlike200k.md
vault_room_root: /home/ecm5702/hpcperm/docs/exp/manual-cfec83a3-new-karras40-oldlike200k
vault_full_rank: '5'
vault_full_contract: eligible
vault_proxy_rank: '4'
vault_proxy_contract: eligible
---

# cfec83 k40 oldlike200k

Generated: `2026-03-25T19:38:30Z`

Storage root: `/home/ecm5702/hpcperm/docs/exp/manual-cfec83a3-new-karras40-oldlike200k`

## What this is
This room mirrors the current scoreboard-facing manual-inference artifacts into an Obsidian-friendly page with inline previews plus lightweight copied configs, stats, logs, and selected artifacts inside the vault.

> GitHub note:
> the inline PNG previews render directly here; lightweight files are copied into the vault, while bulky data such as `predictions/` and plot directories remain linked so the vault stays git-light.

## Experiment identity
- slug: `manual-cfec83a3-new-karras40-oldlike200k`
- checkpoint id: `cfec83a3cd0644778e2bfcbacfa9f4fc`
- checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/last.ckpt`
- stack: `new`
- run id: `manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
- run root: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
- venv: `/home/ecm5702/dev/.ds-dyn/bin/activate`
- login node: `na`
- qos: `na`
- job ids: `31375341, 31375342, 31377164`
- sampling summary: `schedule_type=karras, schedule_kind=karras, num_steps=40, sigma_min=0.03, sigma_max=1000.0, rho=7.0, sampler=heun, S_churn=2.5, S_min=0.75, S_max=1000.0, S_noise=1.05`
- consolidated source dossier: [`manual-cfec83a3-new-karras40-oldlike200k.md`](links/provenance/manual-cfec83a3-new-karras40-oldlike200k.md)

## Current scoreboard status
| surface | rank | contract | idalia tc | franklin tc | spectra mean | surface mse | val loss | note |
| --- | ---: | --- | ---: | ---: | ---: | ---: | ---: | --- |
| Aug 26-30 | 5 | `eligible` | 0.919355 | 0.794926 | 0.980591 | 10646.679560 | 0.066412 | Full-contract row with complete scoreboard artifacts. |
| Proxy10 | 4 | `eligible` | 0.785289 | 0.700827 | 0.969856 | 10646.679560 | 0.066412 | Frozen proxy10total row rebuilt from the March 20 run root with scoreboard-native TC and spectra artifacts. |

## Coverage summary
- predictions files: `25`
- local-plot directories: `2`
- spectra directories: `1`
- top-level PDFs/PNGs: `1`
- top-level JSON/TXT/CSV/YAML files: `5`
- logs: `6`
- extra directories: `5`

## Publication notes
- no `tc_members` PNG gallery was present in the run root
- the bulky `predictions/` directory remains linked rather than copied into the vault
- files larger than `20 MB` stay linked so the vault remains lightweight

## Key data files
| file | link | size |
| --- | --- | ---: |
| `EXPERIMENT_CONFIG.yaml` | [`EXPERIMENT_CONFIG.yaml`](links/data/EXPERIMENT_CONFIG.yaml) | 2.6 KB |
| `proxy_tc_compare.json` | [`proxy_tc_compare.json`](links/data/proxy_tc_compare.json) | 9.6 KB |
| `scoreboard_metrics.json` | [`scoreboard_metrics.json`](links/data/scoreboard_metrics.json) | 561 B |
| `surface_loss_summary.json` | [`surface_loss_summary.json`](links/data/surface_loss_summary.json) | 1.4 KB |
| `tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.stats.json` | [`tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.stats.json`](links/data/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.stats.json) | 40.8 KB |
| `predictions/` | [`predictions/`](links/data/predictions) | 25 files |

## Key top-level artifacts
| file | link | size |
| --- | --- | ---: |
| `tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.pdf` | [`tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.pdf`](links/artifacts/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.pdf) | 26.4 KB |

## Spectra directories
| directory | link | PNGs | PDFs |
| --- | --- | ---: | ---: |
| `spectra_step120_5dates_m10_ecmwf` | [`spectra_step120_5dates_m10_ecmwf`](links/spectra/spectra_step120_5dates_m10_ecmwf) | 0 | 6 |

## Local-plot directories
| directory | link | PNGs | PDFs |
| --- | --- | ---: | ---: |
| `eval` | [`eval`](links/local_plots/eval) | 0 | 0 |
| `eval_one_date_amazon_member01` | [`eval_one_date_amazon_member01`](links/local_plots/eval_one_date_amazon_member01) | 10 | 10 |

## Logs
| file | link | size |
| --- | --- | ---: |
| `autopilot_predictions.pid` | [`autopilot_predictions.pid`](links/logs/autopilot_predictions.pid) | 8 B |
| `autopilot_predictions_background.log` | [`autopilot_predictions_background.log`](links/logs/autopilot_predictions_background.log) | 0 B |
| `eval_proxy_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31375342.out` | [`eval_proxy_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31375342.out`](links/logs/eval_proxy_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31375342.out) | 9.5 KB |
| `predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31377164.out` | [`predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31377164.out`](links/logs/predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31377164.out) | 415.4 KB |
| `predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31483987.out` | [`predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31483987.out`](links/logs/predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31483987.out) | 580.9 KB |
| `predict_proxy_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31375341.out` | [`predict_proxy_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31375341.out`](links/logs/predict_proxy_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_31375341.out) | 28.8 KB |

## Provenance
| file | link | size |
| --- | --- | ---: |
| `manual-cfec83a3-new-karras40-oldlike200k.md` | [`manual-cfec83a3-new-karras40-oldlike200k.md`](links/provenance/manual-cfec83a3-new-karras40-oldlike200k.md) | 11.7 KB |
| `manual-cfec83a3-new-karras40-oldlike200k.md` | [`manual-cfec83a3-new-karras40-oldlike200k.md`](links/provenance/manual-cfec83a3-new-karras40-oldlike200k.md) | 4.2 KB |
| `manual-cfec83a3-new-karras40-oldlike200k.md` | [`manual-cfec83a3-new-karras40-oldlike200k.md`](links/provenance/manual-cfec83a3-new-karras40-oldlike200k.md) | 4.1 KB |
| `20260320_recent_eval_audit.md` | [`20260320_recent_eval_audit.md`](links/provenance/20260320_recent_eval_audit.md) | 33.2 KB |

## Extra directories
| file | link | size |
| --- | --- | ---: |
| `eefo_o96/` | [`eefo_o96/`](links/extra/eefo_o96) | directory |
| `enfo_o320/` | [`enfo_o320/`](links/extra/enfo_o320) | directory |
| `jobs/` | [`jobs/`](links/extra/jobs) | directory |
| `plots/` | [`plots/`](links/extra/plots) | directory |
| `predictions_step120_5dates/` | [`predictions_step120_5dates/`](links/extra/predictions_step120_5dates) | directory |

## Local plot gallery
### `predictions_20230826_step024` / `amazon_forest_member01_baseline.png`
![amazon_forest_member01_baseline.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step024/amazon_forest_member01_baseline.png)
### `predictions_20230826_step048` / `amazon_forest_member01_baseline.png`
![amazon_forest_member01_baseline.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step048/amazon_forest_member01_baseline.png)
### `predictions_20230826_step072` / `amazon_forest_member01_baseline.png`
![amazon_forest_member01_baseline.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step072/amazon_forest_member01_baseline.png)
### `predictions_20230826_step096` / `amazon_forest_member01_baseline.png`
![amazon_forest_member01_baseline.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step096/amazon_forest_member01_baseline.png)
### `predictions_20230826_step120` / `amazon_forest_member01_baseline.png`
![amazon_forest_member01_baseline.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step120/amazon_forest_member01_baseline.png)
## Spectra previews
### `physical_models_spectra_10u_sfc.pdf`
[`physical_models_spectra_10u_sfc.pdf`](links/spectra/spectra_step120_5dates_m10_ecmwf/physical_models_spectra_10u_sfc.pdf)
![](previews/spectra_10u_sfc_p01.png)
### `physical_models_spectra_10v_sfc.pdf`
[`physical_models_spectra_10v_sfc.pdf`](links/spectra/spectra_step120_5dates_m10_ecmwf/physical_models_spectra_10v_sfc.pdf)
![](previews/spectra_10v_sfc_p01.png)
### `physical_models_spectra_2t_sfc.pdf`
[`physical_models_spectra_2t_sfc.pdf`](links/spectra/spectra_step120_5dates_m10_ecmwf/physical_models_spectra_2t_sfc.pdf)
![](previews/spectra_2t_sfc_p01.png)
### `physical_models_spectra_sp_sfc.pdf`
[`physical_models_spectra_sp_sfc.pdf`](links/spectra/spectra_step120_5dates_m10_ecmwf/physical_models_spectra_sp_sfc.pdf)
![](previews/spectra_sp_sfc_p01.png)
### `physical_models_spectra_t_850.pdf`
[`physical_models_spectra_t_850.pdf`](links/spectra/spectra_step120_5dates_m10_ecmwf/physical_models_spectra_t_850.pdf)
![](previews/spectra_t_850_p01.png)
### `physical_models_spectra_z_500.pdf`
[`physical_models_spectra_z_500.pdf`](links/spectra/spectra_step120_5dates_m10_ecmwf/physical_models_spectra_z_500.pdf)
![](previews/spectra_z_500_p01.png)
## TC PDF previews
### `tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.pdf`
[`tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.pdf`](links/artifacts/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions.pdf)
![](previews/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions_p01.png)
![](previews/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_oldlike200k_from_predictions_p02.png)

