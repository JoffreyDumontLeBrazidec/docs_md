---
dossier_mode: generated
slug: manual-cfec83a3-new-piecewise30-h10-l20-sigma100
display_label: cfec83 pw30
role: experiment
checkpoint_id: cfec83a3cd0644778e2bfcbacfa9f4fc
checkpoint_path: /home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/last.ckpt
lane: o96-o320
stack_flavor: new
run_id: manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100
run_root: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100
venv: /home/ecm5702/dev/.ds-dyn/bin/activate
login_node: null
qos: null
job_ids: []
task_note: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md
experiment_config: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100/EXPERIMENT_CONFIG.yaml
sampling:
  summary: schedule_type=experimental_piecewise, schedule_kind=piecewise30, high_schedule_type=exponential,
    low_schedule_type=karras, num_steps=30, num_steps_high=10, num_steps_low=20, sigma_min=0.03,
    sigma_transition=100.0, sigma_max=100000.0, rho=7.0, sampler=heun, S_churn=2.5,
    S_min=0.75, S_max=100000.0, S_noise=1.05
  extra_args:
    schedule_kind: piecewise30
    num_steps: 30
    sigma_max: 100000.0
    sigma_min: 0.03
    rho: 7.0
    sampler: heun
    S_churn: 2.5
    S_min: 0.75
    S_max: 100000.0
    S_noise: 1.05
    schedule_type: experimental_piecewise
    sigma_transition: 100.0
    high_schedule_type: exponential
    low_schedule_type: karras
    num_steps_high: 10
    num_steps_low: 20
surfaces:
  proxy10:
    status: recorded
    promotion: promoted
    rank: 9
    scope:
      dates:
      - 20230829
      - 20230828
      - 20230830
      - 20230827
      members:
      - 1
      steps_hours:
      - 24
      - 48
      - 72
    artifacts:
      tc_stats: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total_strict.stats.json
      spectra_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total/spectra_summary.json
      compare_json: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy_tc_compare.json
      scoreboard_metrics: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/scoreboard_metrics.json
  aug_26_30:
    status: recorded
    promotion: promoted
    rank: 6
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
      sigma_csv: /home/ecm5702/perm/eval/scoreboards/sigma/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_sigma_eval.csv
      tc_stats: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.stats.json
      spectra_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100/spectra_step120_5dates_m10_ecmwf/spectra_summary.json
      comparison_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100/spectra_step120_5dates_m10_ecmwf/comparison_summary.json
      surface_loss_summary: /home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100/surface_loss_summary.json
vault_published: true
vault_published_at: '2026-03-25T19:38:41Z'
vault_source_dossier: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md
vault_room_root: /home/ecm5702/hpcperm/docs/exp/manual-cfec83a3-new-piecewise30-h10-l20-sigma100
vault_full_rank: '6'
vault_full_contract: eligible
vault_proxy_rank: '9'
vault_proxy_contract: mismatch
---

# cfec83 pw30

Generated: `2026-03-25T19:38:41Z`

Storage root: `/home/ecm5702/hpcperm/docs/exp/manual-cfec83a3-new-piecewise30-h10-l20-sigma100`

## What this is
This room mirrors the current scoreboard-facing manual-inference artifacts into an Obsidian-friendly page with inline previews plus lightweight copied configs, stats, logs, and selected artifacts inside the vault.

> GitHub note:
> the inline PNG previews render directly here; lightweight files are copied into the vault, while bulky data such as `predictions/` and plot directories remain linked so the vault stays git-light.

## Experiment identity
- slug: `manual-cfec83a3-new-piecewise30-h10-l20-sigma100`
- checkpoint id: `cfec83a3cd0644778e2bfcbacfa9f4fc`
- checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/cfec83a3cd0644778e2bfcbacfa9f4fc/last.ckpt`
- stack: `new`
- run id: `manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100`
- run root: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100`
- venv: `/home/ecm5702/dev/.ds-dyn/bin/activate`
- login node: `na`
- qos: `na`
- job ids: `na`
- sampling summary: `schedule_type=experimental_piecewise, schedule_kind=piecewise30, high_schedule_type=exponential, low_schedule_type=karras, num_steps=30, num_steps_high=10, num_steps_low=20, sigma_min=0.03, sigma_transition=100.0, sigma_max=100000.0, rho=7.0, sampler=heun, S_churn=2.5, S_min=0.75, S_max=100000.0, S_noise=1.05`
- consolidated source dossier: [`manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md`](links/provenance/manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md)

## Current scoreboard status
| surface | rank | contract | idalia tc | franklin tc | spectra mean | surface mse | val loss | note |
| --- | ---: | --- | ---: | ---: | ---: | ---: | ---: | --- |
| Aug 26-30 | 6 | `eligible` | 0.909171 | 0.742939 | 0.979096 | 10671.348770 | 0.066417 | Full-contract row with complete scoreboard artifacts. |
| Proxy10 | 9 | `mismatch` | 0.654797 | 0.804913 | 0.968898 | 3900.165095 | na | Direct proxy10total row with strict TC and spectra artifacts. |

## Coverage summary
- predictions files: `25`
- local-plot directories: `1`
- spectra directories: `1`
- top-level PDFs/PNGs: `1`
- top-level JSON/TXT/CSV/YAML files: `6`
- logs: `0`
- extra directories: `3`

## Publication notes
- no `tc_members` PNG gallery was present in the run root
- the bulky `predictions/` directory remains linked rather than copied into the vault
- files larger than `20 MB` stay linked so the vault remains lightweight

## Key data files
| file | link | size |
| --- | --- | ---: |
| `EXPERIMENT_CONFIG.yaml` | [`EXPERIMENT_CONFIG.yaml`](links/data/EXPERIMENT_CONFIG.yaml) | 3.1 KB |
| `manual_inference_run_info.txt` | [`manual_inference_run_info.txt`](links/data/manual_inference_run_info.txt) | 1.3 KB |
| `predictions_manifest.csv` | [`predictions_manifest.csv`](links/data/predictions_manifest.csv) | 66.0 KB |
| `scoreboard_metrics.json` | [`scoreboard_metrics.json`](links/data/scoreboard_metrics.json) | 577 B |
| `surface_loss_summary.json` | [`surface_loss_summary.json`](links/data/surface_loss_summary.json) | 1.4 KB |
| `tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.stats.json` | [`tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.stats.json`](links/data/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.stats.json) | 41.1 KB |
| `predictions/` | [`predictions/`](links/data/predictions) | 25 files |

## Key top-level artifacts
| file | link | size |
| --- | --- | ---: |
| `tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.pdf` | [`tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.pdf`](links/artifacts/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.pdf) | 26.4 KB |

## Spectra directories
| directory | link | PNGs | PDFs |
| --- | --- | ---: | ---: |
| `spectra_step120_5dates_m10_ecmwf` | [`spectra_step120_5dates_m10_ecmwf`](links/spectra/spectra_step120_5dates_m10_ecmwf) | 0 | 6 |

## Local-plot directories
| directory | link | PNGs | PDFs |
| --- | --- | ---: | ---: |
| `eval_one_date_amazon_member01` | [`eval_one_date_amazon_member01`](links/local_plots/eval_one_date_amazon_member01) | 5 | 5 |

## Logs
No files published.

## Provenance
| file | link | size |
| --- | --- | ---: |
| `manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md` | [`manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md`](links/provenance/manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md) | 14.1 KB |
| `manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md` | [`manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md`](links/provenance/manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md) | 5.0 KB |
| `manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md` | [`manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md`](links/provenance/manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md) | 5.0 KB |
| `20260320_recent_eval_audit.md` | [`20260320_recent_eval_audit.md`](links/provenance/20260320_recent_eval_audit.md) | 33.2 KB |

## Extra directories
| file | link | size |
| --- | --- | ---: |
| `eefo_o96/` | [`eefo_o96/`](links/extra/eefo_o96) | directory |
| `enfo_o320/` | [`enfo_o320/`](links/extra/enfo_o320) | directory |
| `predictions_step120_5dates/` | [`predictions_step120_5dates/`](links/extra/predictions_step120_5dates) | directory |

## Local plot gallery
### `predictions_20230826_step024` / `amazon_forest_central_member01_classic.png`
![amazon_forest_central_member01_classic.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step024/amazon_forest_central_member01_classic.png)
### `predictions_20230826_step048` / `amazon_forest_central_member01_classic.png`
![amazon_forest_central_member01_classic.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step048/amazon_forest_central_member01_classic.png)
### `predictions_20230826_step072` / `amazon_forest_central_member01_classic.png`
![amazon_forest_central_member01_classic.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step072/amazon_forest_central_member01_classic.png)
### `predictions_20230826_step096` / `amazon_forest_central_member01_classic.png`
![amazon_forest_central_member01_classic.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step096/amazon_forest_central_member01_classic.png)
### `predictions_20230826_step120` / `amazon_forest_central_member01_classic.png`
![amazon_forest_central_member01_classic.png](links/local_plots/eval_one_date_amazon_member01/predictions_20230826_step120/amazon_forest_central_member01_classic.png)
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
### `tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.pdf`
[`tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.pdf`](links/artifacts/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions.pdf)
![](previews/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions_p01.png)
![](previews/tc_normed_pdfs_idalia_franklin_manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_from_predictions_p02.png)

