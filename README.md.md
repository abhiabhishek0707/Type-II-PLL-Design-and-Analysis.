# Design and Analysis of Type-II PLL

A transistor-level **Type-II Phase-Locked Loop (PLL)** designed and analyzed in **180 nm CMOS using Cadence Virtuoso** for frequency synthesis.

## Project Overview

The PLL integrates a **Phase-Frequency Detector (PFD), charge pump, loop filter, ring VCO, and frequency divider** in a closed-loop architecture.

**Reference Frequency:** 10 MHz  
**Target Output Frequency:** 1.2 GHz  
**Supply Voltage:** 1.8 V  
**Feedback Divider:** 128:1  
**Technology:** 180 nm CMOS  
**Simulation:** 5 μs transient analysis

## Key Specifications

| Parameter | Value |
|---|---|
| Reference Frequency | 10 MHz |
| Target VCO Frequency | 1.2 GHz |
| Simulated VCO Frequency | 1.2041 GHz |
| Supply Voltage | 1.8 V |
| Feedback Divider | 128:1 |
| Maximum Power | 3.6 mW |
| Deterministic Jitter | 20 ps p-p |
| Random Jitter | 5 ps RMS |
| Control Voltage | ~0.9 V |

## PLL Architecture

**Reference Clock → PFD → Charge Pump → Loop Filter → Ring VCO → ÷128 Divider → PFD**

- **PFD:** Generates UP/DOWN pulses from the phase and frequency difference.
- **Charge Pump:** Converts PFD pulses into the loop-filter current.
- **Loop Filter:** Generates the VCO control voltage and influences loop stability.
- **Ring VCO:** Generates the high-frequency output controlled by the loop voltage.
- **Divider:** Divides the VCO output by 128 for closed-loop feedback.

## Simulation & Analysis

Performed **5 μs transient analysis** to evaluate:

- VCO output frequency and waveform
- Control-voltage settling
- PFD UP/DOWN pulses
- Divider feedback
- PLL lock behavior
- Charge-pump mismatch
- VCO nonlinearity
- PFD reset timing
- Control-voltage ripple and jitter

The simulated VCO output reached **1.2041 GHz** for a **10 MHz reference**, demonstrating the intended frequency-synthesis operation.

## Design Optimization

The design was analyzed and optimized through transistor sizing, charge-pump current matching, VCO biasing, and PFD reset-timing adjustments to improve **lock stability, control-voltage settling, and overall PLL performance**.

## Tools

- **Cadence Virtuoso**
- **180 nm CMOS Technology**
- Transistor-level schematic design
- Transient simulation and waveform analysis

## Author

**Abhishek Anand**  
M.Tech – Microelectronics, Photonics & RF  
Indian Institute of Technology Guwahati
