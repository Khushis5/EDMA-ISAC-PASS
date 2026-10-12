# Key numbers

Settings: $P = 30$ dBm, $D_L = 40$ m, $\phi = 0.02$. Rates are in bits/s/Hz. All values are produced by `Code/src`.

| Scheme | CR, $M=2$ | SR, $M=2$ | CR, $M=5$ | SR, $M=5$ |
|---|---|---|---|---|
| EDMA, PA at midpoint (Monte Carlo) | 29.45 | 0.065 | 51.43 | 0.286 |
| Lower bound (Theorems 1 and 2) | 29.24 | 0.060 | 43.61 | 0.110 |
| EDMA, all segments interfere | 29.45 | 0.065 | 50.89 | 0.286 |
| EDMA, PA at $U_m$ | 31.16 | 0.037 | 51.73 | 0.189 |
| EDMA, PA at $T_m$ | 26.72 | 0.163 | 47.96 | 0.398 |
| TDMA | 15.48 | 0.009 | 18.03 | 0.056 |

- $p_1(\phi)$: 0.032 for $M=2$ ($S=20$ m) and 0.278 for $M=5$ ($S=8$ m).
- EDMA/TDMA ratio over 0–30 dBm: the CR ratio is 1.85–1.90 ($M=2$) and 2.74–2.85 ($M=5$), against predicted values of 1.94 and 2.78. The SR ratio is 6.98–7.55 ($M=2$) and 4.49–5.16 ($M=5$).
- CR peak versus $M$: 51.4 at $M=5$ ($D_L=40$ m), 29.3 at $M=3$ ($D_L=20$ m), and 18.0 at $M=2$ ($D_L=10$ m).
- For $D_L=10$ m and $M \ge 3$, $p_1 \ge 0.66$ and EDMA falls below TDMA.
- SR for $D_L=40$ m as $M$ goes from 2 to 8: 0.065 → 0.524 for EDMA, and 0.009 → 0.092 for TDMA.
- Closed-form check (`verify_lb_output.txt`): $B_c$ by closed form equals the quadrature value to 4 decimals; $p_1$ by closed form is 0.0320 against 0.0319 by brute-force Monte Carlo ($M=2$), and 0.2779 against 0.2779 ($M=5$).
