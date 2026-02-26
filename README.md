# NE555 Astable Oscillator Module

Compact PCB module based on the NE555 timer configured in astable mode.  
Designed as a reusable visual or acoustic indicator board.

---

## Overview

This board implements a classic NE555 astable oscillator capable of generating periodic square-wave output signals.

The output can drive:

- LED indicators
- Buzzers
- External logic input stages

The oscillation period is defined by two resistors and one capacitor, allowing easy timing customization.

---

## Technical Specifications

| Parameter | Value |
|------------|--------|
| Timer IC | NE555P |
| Supply Voltage | 5–12 V DC |
| Oscillator Mode | Astable |
| Timing Components | R1, R2, C |
| Output Type | Digital square wave |
| PCB Type | Single-layer through-hole |

---

## Component List (BOM)

| Reference | Component | Suggested Value / Part |
|-----------|-----------|------------------------|
| U1 | Timer IC | NE555P (DIP-8) |
| R1 | Resistor | 1 kΩ to 100 kΩ |
| R2 | Resistor | 1 kΩ to 1 MΩ |
| C1 | Timing Capacitor | 100 nF to 1000 µF |
| C2 | Decoupling Capacitor | 100 nF (ceramic, near U1 VCC-GND) |
| D1 (optional) | Indicator LED | 3 mm or 5 mm |
| R3 (if D1 used) | LED Current Limiting Resistor | 220 Ω to 1 kΩ |
| J1 | Power Connector | 2-pin terminal (5–12 V DC) |
| J2 | Output Connector | 2-pin terminal / header |

> Note: R1, R2 and C1 define the oscillation frequency and duty cycle. Choose values according to the target timing.

---

## Timing Equations (Astable Mode)

$$
\begin{aligned}
T_{\text{high}} &= 0.693\,(R_1 + R_2)\,C \\
T_{\text{low}}  &= 0.693\,R_2\,C \\
T               &= T_{\text{high}} + T_{\text{low}} \\
f               &= \frac{1}{T} \\
D               &= \frac{R_1 + R_2}{R_1 + 2R_2}
\end{aligned}
$$

Where:

- $T_{\text{high}}$: output HIGH duration (s)
- $T_{\text{low}}$: output LOW duration (s)
- $T$: period (s)
- $f$: frequency (Hz)
- $D$: duty cycle (0 to 1)

Detailed derivation and worked example: [calculations/timing_equations.md](calculations/timing_equations.md)

---

## Repository Structure

- `hardware/schematics/` → Circuit schematic
- `hardware/pcb/` → PCB layout, 3D model (.step)
- `hardware/gerber/` → Manufacturing files
- `media/` → Rendered images and usage example
- `calculations/` → Timing equations reference

---

## Applications

- Level indicators
- Periodic warning signals
- Blinking LED modules
- Simple timing circuits
- Educational electronics projects

---

## Manufacturing

Gerber files are included for direct PCB fabrication.
A 3D STEP model is provided for mechanical integration.