# M2 (Technical Artifact) — Performance Analysis of ISAC-PASS under EDMA Geometry

**Category:** Research Project
**Student:** Khushi Shah (AU2440045), single-member group
**Mentor:** Prof. Dhaval Patel

## Summary

This project analyses how line-of-sight (LoS) blockage affects a multi-segment pinching-antenna system (PASS) that performs integrated sensing and communication (ISAC). Each waveguide segment activates one pinching antenna at the midpoint of its user and target, and all segments operate at the same time (EDMA geometry). Blockage of the cross-segment links controls three impairments at once: interference, clutter and leakage.

The M2 technical artifact has two parts:

- **Analytical framework:**
  - a closed-form mean cross-segment LoS probability $p_1(\phi)$;
  - closed-form lower bounds on the ergodic sum communication rate (CR) and sensing rate (SR), valid for any number of segments $M$;
  - a high-SNR condition, $p_1(\phi) < 1/2$, under which EDMA outperforms TDMA.
- **Simulation artifact:** a Monte Carlo simulator ($10^5$ placements, with exact averaging over blockage states) that includes three benchmarks: PA at the user, PA at the target, and TDMA. The simulator is verified against every closed form.

The full performance evaluation is planned for M3.

## Folder map

| Folder | Contents |
|---|---|
| `Report/` | `M2_Khushi_Shah_Report.pdf` (5 pages); LaTeX source in `Report/src/` |
| `Video/` | Walkthrough link (`M2_Khushi_Shah_video_link`)
| `Code/` | Simulator, plotting and verification code (`Code/src/`); see `Code/README.md`. This is a simulation-only project with no external dataset. |
| `Results/` | Figures, the output of the closed-form check (`verify_lb_output.txt`), and `key_numbers.md` |

## Reproduce

```bash
cd Code/src
python plot_all.py
python verify_lb.py
```
