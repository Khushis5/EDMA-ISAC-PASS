# M2 — Performance Analysis of ISAC-PASS under EDMA Geometry

**Category:** Research Project
**Student:** Khushi Shah (AU2440045), single-member group


## Summary

This project analyses how line-of-sight (LoS) blockage affects a multi-segment pinching-antenna system (PASS) that performs integrated sensing and communication (ISAC). Each waveguide segment activates one pinching antenna at the midpoint of its user and target, and all segments operate concurrently (EDMA geometry). Blockage of the cross-segment links controls three impairments at once: interference, clutter and leakage.

M2 delivers:

- a closed-form mean cross-segment LoS probability $p_1(\phi)$;
- closed-form lower bounds on the ergodic sum communication rate (CR) and sensing rate (SR), valid for any number of segments $M$;
- a high-SNR condition, $p_1(\phi) < 1/2$, under which EDMA outperforms TDMA;
- a Monte Carlo simulator ($10^5$ drops, with exact blockage averaging) that validates all three, plus three benchmarks: PA at the user, PA at the target, and TDMA.

## Folder map

| Folder | Contents |
|---|---|
| `Report/` | `M2_Khushi_Shah_Report.pdf`; LaTeX source in `Report/src/` |
| `Video/` | Walkthrough link (`M2_Khushi_Shah_video_link.md`), 6 slides (`M2_Khushi_Shah_Slides.pptx`), script (`video_script.md`) |
| `Code/` | Simulator and plotting code (`Code/src/`); see `Code/README.md` |
| `Data/` | Simulation-only project: no external dataset. Parameters are documented in `Data/README.md` |
| `Results/` | The four figures, the network-model figure, the closed-form check output, and `key_numbers.md` |

## Reproduce

```bash
cd Code/src
python plot_all.py
python verify_lb.py
```
