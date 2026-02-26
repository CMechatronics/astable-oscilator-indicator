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
| Timing Components | R1, R2, C1 |
| Output Type | Digital square wave |
| PCB Type | Single-layer through-hole |

---

## Component List (BOM)

| Reference | Component | Suggested Value / Part |
|-----------|-----------|------------------------|
| U1 | Timer IC | NE555P (DIP-8) |
| R1 | Resistor | 3.3 kΩ |
| R2 | Resistor | 68 kΩ |
| C1 | Timing Capacitor (electrolytic) | 22 µF |
| C2 | Control/Noise Filter Capacitor | 10 nF (pin 5 to GND) |
| D1 | LED | Red LED (1.6 V / 20 mA) |
| R3 | Resistor | 100 Ω |
| R4 | Resistor | 47 Ω |
| D2 | Protection Diode | 1 A max (series input protection) |
| SW1 | Push Button Switch | SPST momentary |
| BT1 | Battery / DC Source | Project supply source |

> Note: R1, R2 and C1 define the oscillation frequency and duty cycle.

---

## Timing Equations (Astable Mode)

$$
\Large T_{\text{high}} = 0.693\,(R_1 + R_2)\,C
$$

$$
\Large T_{\text{low}} = 0.693\,R_2\,C
$$

$$
\Large T = T_{\text{high}} + T_{\text{low}}
$$

$$
\Large f = \frac{1}{T}
$$

$$
\Large D = \frac{R_1 + R_2}{R_1 + 2R_2}
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