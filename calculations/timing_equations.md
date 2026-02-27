## NE555 Astable Mode Equations

For the classic NE555 astable configuration:

LaTeX view (desktop):

$$
T_{high} = 0.693 (R_1 + R_2) C_1
$$

$$
T_{low} = 0.693 R_2 C_1
$$

$$
T = T_{high} + T_{low}
$$

$$
f = \frac{1}{T}
$$

$$
D = \frac{R_1 + R_2}{R_1 + 2R_2}
$$

Fallback (mobile-friendly):

- Thigh = 0.693 * (R1 + R2) * C1
- Tlow  = 0.693 * R2 * C1
- T     = Thigh + Tlow
- f     = 1 / T
- D     = (R1 + R2) / (R1 + 2 * R2)

Where:

- R1, R2: timing resistors (ohms)
- C1: timing capacitor (farads)
- Thigh: output HIGH duration (seconds)
- Tlow: output LOW duration (seconds)
- T: period (seconds)
- f: frequency (hertz)
- D: duty cycle (0 to 1)

## Worked Example

Given:

- R1 = 4.7 kΩ
- R2 = 68 kΩ
- C1 = 10 µF

Results:

LaTeX view (desktop):

$$
T_{high} = 0.693 (R_1 + R_2) C_1 = 0.504\ s
$$

$$
T_{low} = 0.693 R_2 C_1 = 0.471\ s
$$

$$
T = 0.975\ s
$$

$$
f = 1.026\ Hz
$$

$$
D = 0.517 \approx 51.7\%
$$

Fallback (mobile-friendly):

- Thigh = 0.693 * (R1 + R2) * C1 = 0.504 s
- Tlow  = 0.693 * R2 * C1 = 0.471 s
- T     = 0.975 s
- f     = 1.026 Hz
- D     = 0.517 (~51.7%)

Adjust R1, R2, and C1 to obtain the desired blinking or timing interval.