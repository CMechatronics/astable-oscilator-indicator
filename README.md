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

## Timing Equations (Astable Mode)

T_high = 0.693 (R1 + R2) C  
T_low  = 0.693 (R2) C  

T = T_high + T_low  
f = 1 / T  

Duty Cycle = (R1 + R2) / (R1 + 2R2)

Adjust R1, R2 and C to obtain the desired period.

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