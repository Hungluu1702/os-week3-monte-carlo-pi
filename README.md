# Week 3: Monte Carlo π estimation with threads

Group lab for CO2017 Operating Systems. Three C programs estimate π = 4 × (points inside circle) / (total points) and compare a single-threaded baseline, a multi-threaded local-accumulation version and a multi-threaded shared-counter version protected by a mutex.

Task split, shared conventions and deadlines: [`docs/phan-cong-5-dau-viec.md`](docs/phan-cong-5-dau-viec.md). Read section 2 of that file before writing code.

## Layout

| Path | Owner | Content |
|---|---|---|
| `src/common.h` | Task 1 | `now_sec`, `rand01`, `print_result` |
| `src/pi_single.c` | Task 1 | Approach 1, single thread |
| `src/pi_local.c` | Task 2 | Approach 2, per-thread local counters |
| `src/pi_mutex.c` | Task 3 | Approach 3, shared counter + mutex, optional `k` |
| `Makefile` | Task 1 | `all`, `clean` |
| `scripts/run_bench.sh` | Task 4 | Runs every configuration, writes `results/raw.csv` |
| `scripts/plot.py` | Task 4 | Writes `results/summary.csv` and `figures/*.png` |
| `results/` | Task 4 | `machine.txt`, `raw.csv`, `summary.csv` |
| `figures/` | Task 4 | Plots |
| `report.pdf` | Task 5 | Final report |

Each person edits only the files they own, so pushing straight to `main` is fine. Run `git pull` before every push.

## Build and run

Build and run commands are filled in by Task 1 once the code is in.

All official measurements run on one machine (Task 4).
