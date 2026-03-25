# 20260320_recent_eval_audit

- Status: in-progress
- Owner: ecm5702
- Epic: enfo_o320_scoreboard
- Started (UTC): 2026-03-20T17:01:51Z
- Last updated (UTC): 2026-03-24T17:16:29Z

## Goal
Audit recent `proxy10` and Aug 26-30 `o96 -> o320` evaluation activity, determine which checkpoint-plus-inference experiments already have generated artifacts, and check whether each one is documented in `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/` and the active hub manifests.

## Relevant Job IDs
`31445856, 31418044, 31418106, 31457433, 31457440, 31464922, 32374024, 32374025, 32374026, 32488228, 32488229, 32488230, 32488231, 32488319, 32488321, 32488322, 32488323`

## Key Paths / Artifacts
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_proxy10.yaml`
- `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_26_30.yaml`
- `/home/ecm5702/perm/eval/`

## Next Step
Monitor `32374024`, `32374026`, `32488319`, `32488321`, `32488322`, and `32488323`, then update the hub and artifact ledger once the missing ECMWF spectra summaries land.

## 2026-03-23 ECMWF spectra dependency sweep
- User asked to make sure the recent manual-inference experiment set has trusted ECMWF spectra coverage rather than only the harmonized proxy spectra.
- Inventory outcome:
  - trusted ECMWF spectra already exist for the recent full-scoreboard roots, including:
    - `/home/ecm5702/perm/eval/manual_0c446b41_new_o96_o320_20260316_lognorm35_100k`
    - `/home/ecm5702/perm/eval/manual_0e8dbd90_new_o96_o320_20260318_lognorm35_200k`
    - `/home/ecm5702/perm/eval/manual_39991df_new_o96_o320_20260317_piecewise30_h10_l20_sigma100`
    - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_oldlike100kft`
    - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100`
    - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
  - the older raw proxy attempts:
    - `/home/ecm5702/perm/eval/manual_0c446b41_proxy10_20260318`
    - `/home/ecm5702/perm/eval/manual_0e8dbd90_proxy10_20260318`
    were intentionally skipped because the corrected `proxy10total_dg` roots already hold trusted ECMWF spectra:
    - `/home/ecm5702/perm/eval/manual_0c446b41_proxy10total_dg_20260318`
    - `/home/ecm5702/perm/eval/manual_0e8dbd90_proxy10total_dg_20260318`
- The four remaining proxy10total roots without trusted ECMWF spectra were:
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_karras_n80_sigmax100k_proxy10total`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_karras_n80_sigmax100k_proxy10total`
- First submissions failed immediately:
  - jobs: `32488228`, `32488229`, `32488230`, `32488231`
  - root cause: the rendered repo-template copies resolved `REPO_ROOT` relative to `/home/ecm5702/dev/jobscripts/submit/20260323/`, so the runtime looked for `/var/eval/jobs/templates` instead of the canonical downscaling-tools checkout
- Re-rendered the same four writer scripts with the canonical repo root hardcoded to `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/downscaling-tools`, kept the proxy10total padded pair list (`024/048/072`), and relaunched:
  - `/home/ecm5702/dev/jobscripts/submit/20260323/scoreboard_write_61cf1811_20260323_piecewise30_proxy10total_ecmwf.sbatch` -> `32488319`
  - `/home/ecm5702/dev/jobscripts/submit/20260323/scoreboard_write_61cf1811_20260323_karras80_proxy10total_ecmwf.sbatch` -> `32488321`
  - `/home/ecm5702/dev/jobscripts/submit/20260323/scoreboard_write_cfec83a3_20260323_piecewise30_proxy10total_ecmwf.sbatch` -> `32488322`
  - `/home/ecm5702/dev/jobscripts/submit/20260323/scoreboard_write_cfec83a3_20260323_karras80_proxy10total_ecmwf.sbatch` -> `32488323`
- Relaunch verification:
  - all four jobs were `RUNNING` immediately after resubmission
  - nodes at submit check: `ac6-154`, `ac6-155`, `ac6-158`, `ac6-160`
  - each log reached the `=== Scoreboard writer ===` banner with `pred_count=10`, so the jobs are now past the earlier template-root failure and are actively computing the ECMWF proxy10 subset outputs

## Current State
- Documented recent roots already represented in the hub:
  - `/home/ecm5702/perm/eval/manual_0c446b41_new_o96_o320_20260316_lognorm35_100k`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_new_o96_o320_20260318_lognorm35_200k`
  - `/home/ecm5702/perm/eval/manual_39991df_new_o96_o320_20260317_piecewise30_h10_l20_sigma100`
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_oldlike100kft`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
- Generated proxy10 roots with compliant proxy artifacts but not represented in the current hub state:
  - `/home/ecm5702/perm/eval/manual_0c446b41_proxy10total_dg_20260318`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_proxy10total_dg_20260318`
- Incomplete recent root that is still in progress rather than documentation-ready:
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref`
- Direct proxy root launched so the same checkpoint-plus-sampler can get fast `proxy10total` results without waiting for the full `25`-file run order:
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
- Older proxy attempts with predictions but no scoreboard-native TC/spectra were also found and should be treated as partial attempts rather than documentation-ready experiments:
  - `/home/ecm5702/perm/eval/manual_0c446b41_proxy10_20260318`
  - `/home/ecm5702/perm/eval/manual_0c446b41_proxy10_ng_20260318`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_proxy10_20260318`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_proxy10_ng_20260318`

## Follow-up Actions
- Promoted the corrected proxy10total rows for:
  - `/home/ecm5702/perm/eval/manual_0c446b41_proxy10total_dg_20260318`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_proxy10total_dg_20260318`
- Updated:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_proxy10.yaml`
- Rebuilt:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/`
- Verified that the merged experiment files now report both proxy10 and Aug 26-30 performance for:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-0c446b41-new-lognorm35-100k.md`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-0e8dbd90-new-lognorm35-200k.md`
- Submitted a canonical post-writer repair job for:
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
  - sbatch script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit/20260320/scoreboard_write_56b6c4e2_20260320.sbatch`
  - job id: `31445856`
- Final state for `31445856`:
  - state: `FAILED`
  - failure cause: `/home/ecm5702/dev/downscaling-tools/eval/jobs/generate_enfo_o320_scoreboard.py` raised `ModuleNotFoundError: No module named 'eval'` when called directly from the writer template
  - despite the final failure, the repair had already written:
    - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/spectra_step120_5dates_m10_ecmwf/spectra_summary.json`
    - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/spectra_step120_5dates_m10_ecmwf/comparison_summary.json`
    - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/surface_loss_summary.json`
    - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json`
- Patched the root cause in:
  - `/home/ecm5702/dev/downscaling-tools/eval/jobs/generate_enfo_o320_scoreboard.py`
  so direct-script invocation now bootstraps the repo import path before importing `eval.jobs`.
- Re-ran the missed final steps manually:
  - regenerated `/home/ecm5702/perm/eval/scoreboards/enfo_o320_scoreboard.md`
  - wrote `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/scoreboard_metrics.json`
- Promoted the repaired `56b6` Karras80 full row into:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_26_30.yaml`
  - slug: `manual-56b6c4e2-old-karras80-sigmax100k`
- Rebuilt the hub and verified:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard_26_30.png`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-56b6c4e2-old-karras80-sigmax100k.md`
- The `61cf1811` piecewise reference run has now completed the full Aug 26-30 chain:
  - inference: `31418044` (`COMPLETED`)
  - post-writer: `31418106` (`COMPLETED`)
  - landed full artifacts:
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref/tc_normed_pdfs_idalia_franklin_manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref_from_predictions.stats.json`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref/spectra_step120_5dates_m10_ecmwf/spectra_summary.json`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref/spectra_step120_5dates_m10_ecmwf/comparison_summary.json`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref/surface_loss_summary.json`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref/scoreboard_metrics.json`
- Rendered and submitted a dedicated direct proxy chain for the same `61cf1811` piecewise sampler so proxy10 is no longer blocked on the full-run file order:
  - run root: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total`
  - predict script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit/20260320/predict_proxy_61cf1811_piecewise30_20260320.sbatch`
  - eval/post script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit/20260320/eval_proxy_61cf1811_piecewise30_20260320.sbatch`
  - predict job: `31457433` (completed; wrote all `10` proxy prediction files)
  - eval/post job: `31457440` (failed after writing `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy_tc_compare.json`)
  - failure cause: `plot_pdf_tc_from_predictions` could not import `metview` because the CPU job had not loaded `ecmwf-toolbox`
  - first landed file: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/predictions/predictions_20230829_step024.nc`
  - expected outputs include:
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset_20260320/tc_normed_pdfs_idalia_franklin_61cf1811_piecewise30_proxy10total_strict_20260320.stats.json`
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total_20260320/spectra_summary.json`
- Patched the run-local proxy post script to load `ecmwf-toolbox` and verify `metview` import before the strict-TC step, then submitted a repair-only job for the missing bundle artifacts:
  - repair script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit/20260320/repair_proxy_post_61cf1811_piecewise30_20260320.sbatch`
  - repair job: `31464922` (`COMPLETED`)
- Verified the repair wrote:
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/proxy10total_subset_20260320/tc_normed_pdfs_idalia_franklin_61cf1811_piecewise30_proxy10total_strict_20260320.stats.json`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_proxy10total/spectra_harmonized_proxy10total_20260320/spectra_summary.json`
- Patched the durable canonical proxy launcher path so future proxy bundle jobs can carry sampler overrides and load `ecmwf-toolbox` automatically when writing strict scoreboard artifacts:
  - `/home/ecm5702/dev/downscaling-tools/eval/jobs/launch_proxy_eval.sh`
  - `/home/ecm5702/dev/downscaling-tools/eval/jobs/autopilot_predictions.py`
- Updated repo instructions so the easy-route proxy launcher is the documented manual fallback for sampler-override proxy work:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/instructions/inference-launching.md`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/instructions/o96-o320-manual-inference-scoreboard-policies.md`
- Promoted the repaired `61cf` piecewise proxy row into:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_proxy10.yaml`
  - slug: `manual-61cf1811-new-piecewise30-h10-l20-sigma100`
- Rebuilt the hub and verified:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard_proxy10.png`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/manual-61cf1811-new-piecewise30-h10-l20-sigma100.md`
- Submitted a same-run writer repair for the older-sampler `61cf1811` full root now that the user wants every started Aug 26-30 manual run to finish even if proxy was poor:
  - run root: `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_oldlike100kft`
  - writer script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit_aug26_30_61cf_20260320/scoreboard_write_61cf1811_20260320_oldlike100kft.sbatch`
  - repair job: `31483980` (`RUNNING` at submit check)
- Reconstructed and submitted a resumed full chain for the interrupted `cfec83a3` oldlike200k run:
  - run root: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
  - sigma repair script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit/20260320/sigma_cfec83a3_oldlike200k_repair.sbatch`
  - predict resume script: `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k/jobs/predict25_manual_cfec83a3_new_o96_o320_20260320_oldlike200k.sbatch`
  - writer repair script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scratch/submit/20260320/scoreboard_write_cfec83a3_oldlike200k_repair.sbatch`
  - sigma job: `31483984`
  - predict job: `31483987`
  - writer job: `31483989`
- Weekend full-flow submissions already queued for tonight remain valid and now have dossier-first tracking under `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/exp/`:
  - `manual-61cf1811-new-karras80-sigmax100k.md`
  - `manual-56b6c4e2-old-karras40-sigmax1000.md`
  - `manual-39991df-new-karras80-sigmax100k.md`
  - `manual-cfec83a3-new-piecewise30-h10-l20-sigma100.md`
  - `manual-cfec83a3-new-karras80-sigmax100k.md`
- Canceled the now-redundant queued rerun of the already-completed `61cf1811` piecewise full flow:
  - `scancel 31433288 31433289 31433290`

## 2026-03-23 karras40 completion follow-up
- User asked to cover the active `o320` comparison set with `piecewise30` and `karras40`.
- Verified before relaunch:
  - full `piecewise30` rows already exist for:
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref`
    - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_piecewise30_h10_l20_sigma100`
    - `/home/ecm5702/perm/eval/manual_39991df_new_o96_o320_20260317_piecewise30_h10_l20_sigma100`
    - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot`
  - full `karras40` rows already exist for:
    - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_oldlike100kft`
    - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
- Verified the remaining `karras40` full gaps were:
  - `39991df` full writer completion on the historical full25 root `/home/ecm5702/perm/eval/manual_39991df8_new_o96_o320_20260311_full25_m10_fix3`
  - `56b6c4e2` fresh old-stack full rerun because `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260320_karras40_sigmax1000` failed before predictions landed
- Verified historical failure causes before relaunch:
  - `31433302` (`39991df` `k80` inference) failed because the generated `EXTRA_ARGS_JSON` was malformed and `json.loads()` raised `JSONDecodeError`
  - `31433297` (`56b6c4e2` `k40` inference) failed because the older strict template did not expose the fixed `eval.jobs.checkpoint_profile` import path in the old-stack env
  - `31433296` (`56b6c4e2` `k40` sigma) still fails deeper in the old-stack sigma evaluator with `TypeError: 'NoneType' object is not subscriptable` inside `ds_interface`, so the fresh relaunch intentionally skips sigma and runs inference plus writer only
- Submitted:
  - writer-only completion for existing `39991df` `k40` full25 root:
    - script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/jobscripts/submit/20260323/scoreboard_write_39991df8_20260323_karras40_from_existing.sbatch`
    - job: `32374024`
  - fresh old-stack `56b6c4e2` `k40` full rerun:
    - inference script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/jobscripts/submit/20260323/inference_56b6c4e2_20260323_karras40_sigmax1000.sbatch`
    - writer script: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/jobscripts/submit/20260323/scoreboard_write_56b6c4e2_20260323_karras40_sigmax1000.sbatch`
    - jobs: `32374025` (inference), `32374026` (writer; dependency `afterok:32374025`)
- Submit-time state:
  - `32374024`: `RUNNING`
  - `32374025`: `RUNNING`
  - `32374026`: `PENDING (Dependency)`

## Next Step
- Monitor `32374024`, `32374025`, and `32374026`, then promote the completed `39991df` and `56b6c4e2` `karras40` full rows into the canonical hub once the missing artifacts land.

## 2026-03-24 config capture and step120 plot audit
- User asked for the full `EXPERIMENT_CONFIG` coverage of the active manual comparison set plus a reusable template, and also asked for `step120` local plots across the same run family.
- Created a reusable provenance-first template at:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/experiment_config_capture_template.yaml`
- Created a concrete inventory covering the current comparison run set at:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/experiment_config_inventory.yaml`
- The inventory distinguishes:
  - `capture_status: exact` when `/home/ecm5702/perm/eval/<run>/EXPERIMENT_CONFIG.yaml` exists
  - `capture_status: reconstructed` when the run had to be rebuilt from `manual_inference_run_info.txt`, job scripts, and/or runtime logs
  - `step120_local_plot_status: blocked` for the single `56b6c4e2` `karras40` rerun that still lacks a `step120` prediction file
- The new config inventory now points to the exact or reconstructed config provenance for the discussed runs, including:
  - `/home/ecm5702/perm/eval/manual_0c446b41_new_o96_o320_20260316_lognorm35_100k`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_new_o96_o320_20260318_lognorm35_200k`
  - `/home/ecm5702/perm/eval/manual_9c9db7b7_new_o96_o320_20260310_full25_yfix2`
  - `/home/ecm5702/perm/eval/manual_39991df_new_o96_o320_20260317_piecewise30_h10_l20_sigma100`
  - `/home/ecm5702/perm/eval/manual_39991df8_new_o96_o320_20260311_full25_m10_fix3`
  - `/home/ecm5702/perm/eval/manual_39991df_new_o96_o320_20260323_karras_n80_sigmax100k`
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot`
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260323_karras40_sigmax1000`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260323_piecewise30_h10_l20_sigma100_ref`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_oldlike100kft`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260323_karras_n80_sigmax100k`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_karras_n80_sigmax100k`
- Also backfilled the missing `20230826 step120` Amazon plots for:
  - `/home/ecm5702/perm/eval/manual_0c446b41_new_o96_o320_20260316_lognorm35_100k`
  - `/home/ecm5702/perm/eval/manual_0e8dbd90_new_o96_o320_20260318_lognorm35_200k`
  - `/home/ecm5702/perm/eval/manual_9c9db7b7_new_o96_o320_20260310_full25_yfix2`
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`

## 2026-03-24 2t spectra small-scale comparison
- User asked whether the live scoreboard is hiding useful `2t` spectra differences between the `56b6c4e2`, `61cf1811`, and `cfec83a3` checkpoint families, especially in the small-scale tail relative to `enfo_o320`.
- Compared the canonical full-row roots that feed the current Aug `26-30` scoreboard:
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_oldlike100kft`
  - `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260323_karras_n80_sigmax100k`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_piecewise30_h10_l20_sigma100`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260320_oldlike200k`
  - `/home/ecm5702/perm/eval/manual_cfec83a3_new_o96_o320_20260323_karras_n80_sigmax100k`
- Method used for the tail check:
  - reused the cached `2t_sfc/ampl_*.npy` spectra curves already written under each run root
  - matched them against `/home/ecm5702/hpcperm/reference_spectra/enfo_o320/2t_sfc`
  - kept the same subset that the current scoreboard can actually compare: `20230826-20230830`, `step120`, members `1` and `2` only, because the shared `enfo_o320` cache only carries those two members for that exact late-August subset
- Findings:
  - best overall raw-cache `2t` closeness is `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260323_karras_n80_sigmax100k` with overall relative L2 `0.012355`
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630` is very close behind at `0.012937`
  - inside the `61cf1811` family, the `k80` row wins on the full-curve score, but the piecewise row `/home/ecm5702/perm/eval/manual_61cf1811_new_o96_o320_20260320_piecewise30_h10_l20_sigma100_ref` has the best extreme-tail (`l=240-318`) relative L2 at `0.014066`; the `k40` row is clearly worse in that same tail band at `0.016569`
  - inside the `cfec83a3` family, the rows look good in the upper-middle small-scale band (`l=160-239`), with relative L2 `0.009830` for piecewise and `0.010247` for `k80`, but all three `cfec83a3` rows lose too much power in the extreme tail (`l=240-318`): geometric mean power ratios only `0.986245` (piecewise), `0.984473` (`k40`), and `0.982611` (`k80`) relative to `enfo_o320`
  - that same `cfec83a3` tail weakness also appears as steeper-than-reference tail slopes (`delta log-log slope` from `-0.038798` to `-0.043610`), whereas the `61cf1811` tail slopes stay closer to `enfo_o320` (`-0.027460` to `-0.036758`)
  - practical interpretation: `cfec83a3` is competitive on the mid/high part of the `2t` small-scale band but fades too aggressively at the very end of the tail, while `61cf1811` keeps the most balanced tail shape and therefore wins the current full-curve scoreboard metric
- Important caveats:
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260312_piecewise30_h10_l20_sigma100_classic_piecewisegen4_mixedroot` still shows an excellent legacy `2t` score (`0.002316`), but that number comes from the older `spectra/spectra_summary.json` healpy-from-predictions path and does not have the same raw `ampl_*.npy` tail cache as the newer rows, so it should not be treated as directly apples-to-apples for the tail-band comparison without regenerating it with the same reference subset
  - `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260323_karras40_sigmax1000` is still excluded because the run never produced the full `step120` prediction set after the OOM failure

## 2026-03-24 family spectra bundle
- User asked for the current `56b6c4e2`, `61cf1811`, and `cfec83a3` family spectra plots to be gathered into one stable place before revisiting the scoreboard scoring rule.
- Built a hub-local bundle at:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/spectra_family_compare`
- Contents:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/spectra_family_compare/10u_sfc`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/spectra_family_compare/10v_sfc`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/spectra_family_compare/2t_sfc`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/spectra_family_compare/bundle_manifest.json`
- Coverage:
  - copied `24` PDFs total (`8` runs x `3` variables)
  - included the canonical full rows currently promoted in `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_26_30.yaml` for the three checkpoint families
- Format note:
  - most rows use ECMWF-tools `physical_models_spectra_*` overlays
  - the legacy `56b6c4e2` piecewise row is still represented by its canonical `spectra/spectra_{10u,10v,2t}.pdf` outputs because the promoted full root does not have the newer ECMWF overlay PDFs

## 2026-03-24 high-k spectra rescoring completed
- User asked to change the spectra pillar so only wavenumbers `l > 100` contribute, then recalculate the live scoreboard surfaces with that rule.
- Completed the code/docs/test side earlier in the day, then finished the artifact rewrite and hub rebuild:
  - rewrote all active raw-cache summaries under `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_26_30.yaml`
  - rewrote all active summary-only proxy/full summaries under `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/manifest_proxy10.yaml` and the remaining legacy full rows
  - rebuilt the canonical hub at `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/`
- The live manifests now pass a clean audit for spectra inputs:
  - no active promoted row is still pointing at a stale pre-`l > 100` `spectra_summary.json`
  - no active promoted row is still missing its referenced `spectra_summary.json`
- Also cleaned up two stale proxy-manifest paths that had still referenced deleted `~/dev/docs` scratch bundles:
  - repointed `manual-61cf1811-new-karras40-oldlike100kft` to the surviving proxy bundle under `/home/ecm5702/perm/eval/manual_61cf1811_proxy10total_20260320/`
  - recreated the missing `cfec83a3` Karras40 frozen proxy bundle under `/home/ecm5702/perm/eval/manual_cfec83a3_proxy10total_20260320/` using the canonical `10` proxy bundle pairs and member `1` only, then repointed `manual-cfec83a3-new-karras40-oldlike200k` to that `~/perm/eval` bundle
- Refreshed scoreboard paths verified after rebuild:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard_26_30.png`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard_proxy10.png`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/source_26_30/scoreboard.csv`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/source_proxy10/scoreboard.csv`
- Current readback of the rescored `61cf1811` / `cfec83a3` / legacy `56b6c4e2` rows:
  - full Aug `26-30` surface:
    - `manual-61cf1811-new-piecewise30-h10-l20-sigma100`: `spectra_10v_score_vs_reference=0.951560`, `spectra_mean_score_vs_reference=0.967218`
    - `manual-61cf1811-new-karras40-oldlike100kft`: `spectra_10v_score_vs_reference=0.958534`, `spectra_mean_score_vs_reference=0.972325`
    - `manual-61cf1811-new-karras80-sigmax100k`: `spectra_10v_score_vs_reference=0.957072`, `spectra_mean_score_vs_reference=0.970356`
    - `manual-cfec83a3-new-piecewise30-h10-l20-sigma100`: `spectra_10v_score_vs_reference=0.972759`, `spectra_mean_score_vs_reference=0.979096`
    - `manual-cfec83a3-new-karras40-oldlike200k`: `spectra_10v_score_vs_reference=0.975783`, `spectra_mean_score_vs_reference=0.980591`
    - `manual-cfec83a3-new-karras80-sigmax100k`: `spectra_10v_score_vs_reference=0.977468`, `spectra_mean_score_vs_reference=0.980929`
    - `manual-56b6c4e2-old-piecewise30-h10-l20-sigma100`: `spectra_10v_score_vs_reference=0.966089`, `spectra_mean_score_vs_reference=0.968647`
  - proxy10 surface:
    - `manual-61cf1811-new-piecewise30-h10-l20-sigma100`: `spectra_10v_score_vs_reference=0.947028`, `spectra_mean_score_vs_reference=0.957483`
    - `manual-61cf1811-new-karras40-oldlike100kft`: `spectra_10v_score_vs_reference=0.961598`, `spectra_mean_score_vs_reference=0.966698`
    - `manual-61cf1811-new-karras80-sigmax100k`: `spectra_10v_score_vs_reference=0.955836`, `spectra_mean_score_vs_reference=0.961731`
    - `manual-cfec83a3-new-piecewise30-h10-l20-sigma100`: `spectra_10v_score_vs_reference=0.963923`, `spectra_mean_score_vs_reference=0.968898`
    - `manual-cfec83a3-new-karras40-oldlike200k`: `spectra_10v_score_vs_reference=0.966045`, `spectra_mean_score_vs_reference=0.969856`
    - `manual-cfec83a3-new-karras80-sigmax100k`: `spectra_10v_score_vs_reference=0.964606`, `spectra_mean_score_vs_reference=0.968948`
    - `manual-56b6c4e2-old-piecewise30-h10-l20-sigma100`: `spectra_10v_score_vs_reference=0.958627`, `spectra_mean_score_vs_reference=0.961558`

## 2026-03-24 spectra readability tweak
- User noted that the refreshed spectra scores were still visually too compressed because the top-level snapshot showed only the mean spectra score on a full `0..1` axis, which hides meaningful differences once all promoted rows cluster near `1.0`.
- Updated `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/scripts/plot_scoreboard_snapshot.py` so the live snapshot now:
  - keeps the official spectra pillar panel as the mean score vs `enfo_o320`
  - zooms the spectra x-axis to the observed score range for the current surface instead of always using the full `0..1`
  - adds a dedicated `10v` detail panel so known weak-`10v` families such as `61cf1811` do not disappear behind the mean of `10u`, `10v`, and `2t`
- Follow-up bugfixes from the next user review:
  - fixed row alignment by forcing the metric panels to use the same `y` limits as the metadata panel rather than relying on `barh()` autoscaling
  - removed the extra title-adjacent note text from the non-spectra panels
  - changed the snapshot row ordering so experiment rows now sort by `spectra_mean_score_vs_reference` instead of the old Idalia-first plotting order
- Follow-up simplification from the next user review:
  - removed the temporary standalone `10v` detail panel and returned the snapshot to a single spectra pillar
  - clarified in the snapshot summary text that the red/green/purple/blue bar colors come from `contract_status` metadata (`eligible`, `mismatch`, `missing-scope`, `other/unknown`) rather than from score magnitude
- Rebuilt the hub after this display change, so the current top-level PNGs at:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard_26_30.png`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/scoreboard_proxy10.png`
  now use a simpler single-spectra presentation without changing the underlying CSV metrics; only the snapshot presentation changed, and the snapshot row order is now spectra-first.

## 2026-03-24 proxy10 is not a reliable proxy for TC ordering
- Compared the live TC rows in:
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/source_proxy10/scoreboard.csv`
  - `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/source_26_30/scoreboard.csv`
- Conclusion for future scoreboard discussion: treat `proxy10` as a coarse screening surface only, **not** as a trustworthy proxy for final TC ranking.
- Evidence from the official scoreboard TC rank (`tc_rank`, which still uses Idalia as the primary event):
  - top-10 overlap is high (`9/10`), but shared rows still move by about `2.7` rank places on average
  - notable drift includes `61cf18112f piecewise30` moving from proxy rank `7` to Aug `26-30` rank `1`, and `39991df812 piecewise30` moving from proxy rank `3` to Aug `26-30` rank `9`
- Evidence from the user-preferred Franklin-only view (`franklin_tc_extreme_score`):
  - top-10 overlap drops to `8/10`
  - shared rows still move by about `2.5` rank places on average
  - notable drift includes `cfec83a3cd karras40` moving from proxy Franklin rank `7` to Aug `26-30` Franklin rank `1`, and `39991df812 karras40` moving from proxy Franklin rank `5` to Aug `26-30` Franklin rank `11`
- Operational interpretation:
  - `proxy10` can still help reject obviously weak TC runs quickly
  - do **not** use `proxy10` to finalize TC ordering, especially when the decision depends on Franklin behavior or on close ranking among the leading runs
