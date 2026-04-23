# O96->O320 current manual-scoreboard vault

Generated: `2026-04-23T14:03:32Z`

Storage root: `/home/ecm5702/hpcperm/docs/published/scoreboard_o96_o320`

## What this is
This hub mirrors the current O96->O320 scoreboard surfaces plus the top full-scoreboard manual experiments into a room-style vault layout for local Obsidian browsing.

## Publish model
- canonical hub: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320`
- vault root: `/home/ecm5702/hpcperm/docs`
- published mirror: `/home/ecm5702/hpcperm/docs/published/scoreboard_o96_o320`
- selection mode: `idalia-franklin-mean`
- selection rule: current default uses the mean of Idalia and Franklin TC extreme scores

## Current scoreboards
### Aug 26-30
[`scoreboard_26_30.png`](scoreboard_26_30.png)
![](scoreboard_26_30.png)

[`scoreboard_26_30_metrics_availability.png`](scoreboard_26_30_metrics_availability.png)
![](scoreboard_26_30_metrics_availability.png)

### Proxy10
[`scoreboard_proxy10.png`](scoreboard_proxy10.png)
![](scoreboard_proxy10.png)

[`scoreboard_proxy10_metrics_availability.png`](scoreboard_proxy10_metrics_availability.png)
![](scoreboard_proxy10_metrics_availability.png)

## Published experiment rooms
| combo tc mean | full rank | proxy rank | experiment | checkpoint | schedule | idalia tc | franklin tc | spectra mean | room |
| ---: | ---: | ---: | --- | --- | --- | ---: | ---: | ---: | --- |
| 0.972035 | 1 | 4 | `56b6 old pw30 classic` | `56b6c4e2a6` | `piecewise30` | 0.977885 | 0.966184 | 0.968647 | [room](../../exp/manual-56b6c4e2-old-piecewise30-h10-l20-sigma100/README.md) |
| 0.971272 | 4 | na | `cfec83 pw21 t10/h5/l16` | `cfec83a3cd` | `piecewise21` | 0.974236 | 0.968308 | 0.962614 | [room](../../exp/manual-cfec83a3-new-piecewise21-t10-h5-l16/README.md) |
| 0.968071 | 8 | na | `59e4 300k pw30` | `59e4059602` | `piecewise30` | 0.966706 | 0.969437 | 0.980678 | [room](../../exp/manual-59e40596-new-piecewise30-h10-l20-sigma100/README.md) |
| 0.963623 | 13 | na | `59e4 300k pw21 t10/h5/l16` | `59e4059602` | `piecewise21` | 0.963081 | 0.964164 | 0.966629 | [room](../../exp/manual-59e40596-new-piecewise21-t10-h5-l16/README.md) |

## Source paths
- source hub: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320`
- full scoreboard csv: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/source_26_30/scoreboard.csv`
- proxy scoreboard csv: `/etc/ecmwf/nfs/dh2_home_a/ecm5702/dev/docs/docs/scoreboard_o96_o320/state/source_proxy10/scoreboard.csv`

## Meta files
- [`meta/selection.yaml`](meta/selection.yaml)
- [`meta/full_top_rows.csv`](meta/full_top_rows.csv)
- [`meta/proxy_selected_rows.csv`](meta/proxy_selected_rows.csv)

