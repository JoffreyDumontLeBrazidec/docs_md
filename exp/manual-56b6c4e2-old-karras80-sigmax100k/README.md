---
dossier_mode: generated
slug: manual-56b6c4e2-old-karras80-sigmax100k
display_label: 56b6 old k80 sigmax100k
role: experiment
checkpoint_id: 56b6c4e2a6064878841dba0635c7be44
checkpoint_path: /home/ecm5702/scratch/aifs/checkpoint/56b6c4e2a6064878841dba0635c7be44/last.ckpt
lane: o96-o320
stack_flavor: old
run_id: manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630
run_root: /home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630
venv: /home/ecm5702/dev/.ds-old/bin/activate
login_node: null
qos: null
job_ids:
- 30822676
- 31445856
task_note: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md
experiment_config: /home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/EXPERIMENT_CONFIG.yaml
sampling:
  summary: num_steps=80, rho=7.0, sampler=heun, sigma_max=100000.0, sigma_min=0.03,
    S_max=100000.0
  extra_args:
    num_steps: 80
    rho: 7.0
    sampler: heun
    sigma_max: 100000.0
    sigma_min: 0.03
    S_churn: 2.5
    S_min: 0.75
    S_max: 100000.0
    S_noise: 1.05
surfaces:
  proxy10:
    status: not_yet_recorded
    promotion: not_promoted
    rank: null
    scope: {}
    artifacts:
      tc_stats: null
      spectra_summary: null
      compare_json: null
      scoreboard_metrics: null
  aug_26_30:
    status: recorded
    promotion: promoted
    rank: 4
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
      sigma_csv: null
      tc_stats: /home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json
      spectra_summary: /home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/spectra_step120_5dates_m10_ecmwf/spectra_summary.json
      comparison_summary: null
      surface_loss_summary: /home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/surface_loss_summary.json
vault_published: true
vault_published_at: '2026-03-25T19:38:37Z'
vault_source_dossier: /etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-56b6c4e2-old-karras80-sigmax100k.md
vault_room_root: /home/ecm5702/hpcperm/docs/exp/manual-56b6c4e2-old-karras80-sigmax100k
vault_full_rank: '4'
vault_full_contract: eligible
vault_proxy_rank: na
vault_proxy_contract: na
---

# 56b6 old k80 sigmax100k

Generated: `2026-03-25T19:38:37Z`

Storage root: `/home/ecm5702/hpcperm/docs/exp/manual-56b6c4e2-old-karras80-sigmax100k`

## What this is
This room mirrors the current scoreboard-facing manual-inference artifacts into an Obsidian-friendly page with inline previews plus lightweight copied configs, stats, logs, and selected artifacts inside the vault.

> GitHub note:
> the inline PNG previews render directly here; lightweight files are copied into the vault, while bulky data such as `predictions/` and plot directories remain linked so the vault stays git-light.

## Experiment identity
- slug: `manual-56b6c4e2-old-karras80-sigmax100k`
- checkpoint id: `56b6c4e2a6064878841dba0635c7be44`
- checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/56b6c4e2a6064878841dba0635c7be44/last.ckpt`
- stack: `old`
- run id: `manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
- run root: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
- venv: `/home/ecm5702/dev/.ds-old/bin/activate`
- login node: `na`
- qos: `na`
- job ids: `30822676, 31445856`
- sampling summary: `num_steps=80, rho=7.0, sampler=heun, sigma_max=100000.0, sigma_min=0.03, S_max=100000.0`
- consolidated source dossier: [`manual-56b6c4e2-old-karras80-sigmax100k.md`](links/provenance/manual-56b6c4e2-old-karras80-sigmax100k.md)

## Current scoreboard status
| surface | rank | contract | idalia tc | franklin tc | spectra mean | surface mse | val loss | note |
| --- | ---: | --- | ---: | ---: | ---: | ---: | ---: | --- |
| Aug 26-30 | 4 | `eligible` | 0.921282 | 0.738797 | 0.973445 | 10788.103067 | na | Full-contract row with repaired TC, spectra, and surface metrics; sigma CSV remains absent. |
| Proxy10 | na | `na` | na | na | na | na | na | na |

## Coverage summary
- predictions files: `25`
- local-plot directories: `1`
- spectra directories: `1`
- top-level PDFs/PNGs: `1`
- top-level JSON/TXT/CSV/YAML files: `6`
- logs: `2`
- extra directories: `4`

## Publication notes
- no `tc_members` PNG gallery was present in the run root
- the bulky `predictions/` directory remains linked rather than copied into the vault
- files larger than `20 MB` stay linked so the vault remains lightweight

## Key data files
| file | link | size |
| --- | --- | ---: |
| `EXPERIMENT_CONFIG.yaml` | [`EXPERIMENT_CONFIG.yaml`](links/data/EXPERIMENT_CONFIG.yaml) | 3.5 KB |
| `manual_inference_run_info.txt` | [`manual_inference_run_info.txt`](links/data/manual_inference_run_info.txt) | 643 B |
| `predictions_manifest.csv` | [`predictions_manifest.csv`](links/data/predictions_manifest.csv) | 66.3 KB |
| `scoreboard_metrics.json` | [`scoreboard_metrics.json`](links/data/scoreboard_metrics.json) | 520 B |
| `surface_loss_summary.json` | [`surface_loss_summary.json`](links/data/surface_loss_summary.json) | 1.4 KB |
| `tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json` | [`tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json`](links/data/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json) | 41.0 KB |
| `predictions/` | [`predictions/`](links/data/predictions) | 25 files |

## Key top-level artifacts
| file | link | size |
| --- | --- | ---: |
| `tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.pdf` | [`tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.pdf`](links/artifacts/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.pdf) | 26.6 KB |

## Spectra directories
| directory | link | PNGs | PDFs |
| --- | --- | ---: | ---: |
| `spectra_step120_5dates_m10_ecmwf` | [`spectra_step120_5dates_m10_ecmwf`](links/spectra/spectra_step120_5dates_m10_ecmwf) | 0 | 6 |

## Local-plot directories
| directory | link | PNGs | PDFs |
| --- | --- | ---: | ---: |
| `eval_one_date_amazon_member01` | [`eval_one_date_amazon_member01`](links/local_plots/eval_one_date_amazon_member01) | 1 | 2 |

## Logs
| file | link | size |
| --- | --- | ---: |
| `predict25_30822676.out` | [`predict25_30822676.out`](links/logs/predict25_30822676.out) | 327.9 KB |
| `tc_eval_30822693.out` | [`tc_eval_30822693.out`](links/logs/tc_eval_30822693.out) | 5.7 KB |

## Provenance
| file | link | size |
| --- | --- | ---: |
| `manual-56b6c4e2-old-karras80-sigmax100k.md` | [`manual-56b6c4e2-old-karras80-sigmax100k.md`](links/provenance/manual-56b6c4e2-old-karras80-sigmax100k.md) | 8.6 KB |
| `manual-56b6c4e2-old-karras80-sigmax100k.md` | [`manual-56b6c4e2-old-karras80-sigmax100k.md`](links/provenance/manual-56b6c4e2-old-karras80-sigmax100k.md) | 5.0 KB |
| `20260320_recent_eval_audit.md` | [`20260320_recent_eval_audit.md`](links/provenance/20260320_recent_eval_audit.md) | 33.2 KB |
| `56b6c4e2.md` | [`56b6c4e2.md`](links/provenance/56b6c4e2.md) | 3.4 KB |

## Extra directories
| file | link | size |
| --- | --- | ---: |
| `eefo_o96/` | [`eefo_o96/`](links/extra/eefo_o96) | directory |
| `enfo_o320/` | [`enfo_o320/`](links/extra/enfo_o320) | directory |
| `predictions_step120_5dates/` | [`predictions_step120_5dates/`](links/extra/predictions_step120_5dates) | directory |
| `tc_aug26_30_regridded_20260319/` | [`tc_aug26_30_regridded_20260319/`](links/extra/tc_aug26_30_regridded_20260319) | directory |

## Local plot gallery
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
### `tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.pdf`
[`tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.pdf`](links/artifacts/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.pdf)
![](previews/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions_p01.png)
![](previews/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions_p02.png)

