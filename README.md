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

Each person edits only the files they own.

## Workflow: branch, pull request, review

`main` is protected. Nobody pushes to it directly:

1. `git switch main && git pull`, then `git switch -c task<N>-<topic>` (for example `task2-pi-local`).
2. Commit on that branch, then `git push -u origin HEAD`.
3. Open a pull request into `main` and request a review from **@PTAxHVA (Tuấn Anh)**.
4. Tuấn Anh reviews and merges. Do not merge your own PR.

AI assistants must follow the same rules; they are written out in [`AGENTS.md`](AGENTS.md), and `CLAUDE.md`, `GEMINI.md` and `.github/copilot-instructions.md` point to it.

## Build and run

Build and run commands are filled in by Task 1 once the code is in.

All official measurements run on one machine (Task 4).
