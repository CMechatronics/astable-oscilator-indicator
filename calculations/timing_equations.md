## NE555 Astable Mode Equations

For the classic NE555 astable configuration:

$$
\begin{aligned}
T_{\text{high}} &= 0.693\,(R_1 + R_2)\,C_1 \\
T_{\text{low}}  &= 0.693\,R_2\,C_1 \\
T               &= T_{\text{high}} + T_{\text{low}} \\
f               &= \frac{1}{T} \\
D               &= \frac{R_1 + R_2}{R_1 + 2R_2}
\end{aligned}
$$

Where:

- $R_1$, $R_2$: timing resistors (ohms)
- $C_1$: timing capacitor (farads)
- $T_{\text{high}}$: output HIGH duration (seconds)
- $T_{\text{low}}$: output LOW duration (seconds)
- $T$: period (seconds)
- $f$: frequency (hertz)
- $D$: duty cycle (0 to 1)

## Worked Example

Given:

- $R_1 = 4.7\,\text{k}\Omega$
- $R_2 = 68\,\text{k}\Omega$
- $C_1 = 10\,\mu\text{F}$

Results:

$$
\begin{aligned}
T_{\text{high}} &= 0.693\,(R_1 + R_2)\,C_1 = 0.504\,\text{s} \\
T_{\text{low}}  &= 0.693\,R_2\,C_1 = 0.471\,\text{s} \\
T               &= 0.975\,\text{s} \\
f               &= 1.026\,\text{Hz} \\
D               &= 0.517 \approx 51.7\%
\end{aligned}
$$

Adjust $R_1$, $R_2$, and $C_1$ to obtain the desired blinking or timing interval.