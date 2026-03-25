# manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630

Generated (UTC): `2026-03-24T16:37:29Z`

## Snapshot
- Summary: Old-stack full-contract Karras80 sigmax100k rerun with repaired TC, spectra, and surface-loss artifacts.
- Comparison note: Full-contract old-stack candidate matched against the new-stack n80/sigmax100k family; scoreboard artifacts were repaired from finished predictions on 2026-03-20.
- Role: `experiment`
- Contract status: `eligible`
- Contract detail: dates: ok
- Contract detail: members: ok
- Contract detail: steps: ok

## Metrics
- Idalia TC extreme score: `0.921282`
- Franklin TC extreme score: `0.738797`
- Spectra reference: `ENFO O320`
- Spectra 10u score vs ENFO O320: `0.970530`
- Spectra 10v score vs ENFO O320: `0.962424`
- Spectra 2t score vs ENFO O320: `0.987382`
- Spectra mean score (10u/10v/2t): `0.973445`
- Spectra 10u distance: `0.029470`
- Spectra 10v distance: `0.037576`
- Spectra 2t distance: `0.012618`
- Spectra mean distance: `0.026555`
- Spectra coverage: `10 pairs`
- Surface weighted MSE: `10788.103067`
- Surface loss source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/surface_loss_summary.json`
- Validation loss: `na`
- Validation loss source: `na`

## Environment And Run
- Lane: `o96-o320`
- Stack flavor: `old`
- Venv: `/home/ecm5702/dev/.ds-old/bin/activate`
- HPC login node: `na`
- HPC partition: `na`
- HPC QoS: `na`
- HPC job IDs: `30822676, 31445856`
- Checkpoint ID: `56b6c4e2a6064878841dba0635c7be44`
- Checkpoint path: `/home/ecm5702/scratch/aifs/checkpoint/56b6c4e2a6064878841dba0635c7be44/last.ckpt`
- Dates: `20230826, 20230827, 20230828, 20230829, 20230830`
- Members: `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`
- Steps (hours): `24, 48, 72, 96, 120`
- Eval (schedule+steps): `karras80`
- Sampling: `num_steps=80, rho=7.0, sampler=heun, sigma_max=100000.0, sigma_min=0.03, S_max=100000.0`
- Extra args source: `manifest.extra_args`
- Training noise: `Old-stack checkpoint family; exact training-noise metadata still needs a trusted training-side source.`

## Evaluation Artifacts
- Task note: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md`
- Artifacts root: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
- TC source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json`
- Idalia TC experiment key: `manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
- Franklin TC experiment key: `manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
- Spectra source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/spectra_step120_5dates_m10_ecmwf/spectra_summary.json`
- Surface source: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/surface_loss_summary.json`
- Exact extra_args:
```json
{
  "S_churn": 2.5,
  "S_max": 100000.0,
  "S_min": 0.75,
  "S_noise": 1.05,
  "num_steps": 80,
  "rho": 7.0,
  "sampler": "heun",
  "sigma_max": 100000.0,
  "sigma_min": 0.03
}
```
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630`
- Artifact path: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/epics/enfo_o320_scoreboard/in-progress/20260320_recent_eval_audit.md`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/EXPERIMENT_CONFIG.yaml`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/tc_normed_pdfs_idalia_franklin_manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630_from_predictions.stats.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/spectra_step120_5dates_m10_ecmwf/spectra_summary.json`
- Artifact path: `/home/ecm5702/perm/eval/manual_56b6c4e2_old_o96_o320_20260319_karras_n80_sigmax100k_aug2630/surface_loss_summary.json`

## What Worked
- The full Aug26-30 prediction tree was already complete, so the repair could recover spectra, TC, and surface-loss outputs without rerunning inference.
- The repaired row now has a scoreboard-compatible spectra summary and a per-run scoreboard metrics sidecar.

## What Did Not
- The original post-writer failed at the ENFO scoreboard refresh because the generator script lacked a direct-invocation import bootstrap.
- Sigma losses are still unavailable for this run family because no sigma CSV was found under /home/ecm5702/perm/eval/scoreboards/sigma/.

## Why Better Or Not Better Yet
- Better than leaving the Karras80 old-stack comparison family out of the canonical full scoreboard now that the core TC, spectra, and surface metrics are present.

## Caveats
- none recorded yet

## Ideas
- Compare this row directly against the 39991df Karras80 sigmax100k peer and the old-stack piecewise anchor.
