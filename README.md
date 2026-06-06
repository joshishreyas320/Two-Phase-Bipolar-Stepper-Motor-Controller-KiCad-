# Two Phase Bipolar Stepper Motor Controller

> KiCad PCB Design | 2-Layer Board | L297 + L298N Driver

---

## Project Description
A 2-phase bipolar stepper motor controller PCB designed using **KiCad**. The board uses the **L297 stepper sequencer IC** and **L298N dual H-bridge driver** to provide full-bridge drive for a 2-phase bipolar stepper motor. Supports STEP/DIR input from any MCU, with flyback diode protection and screw terminal connectors for motor and power wiring.

**Short Description (≤350 chars):**
> 2-phase bipolar stepper motor driver PCB using L297+L298N ICs. Supports STEP/DIR input, full-bridge drive up to 2A/channel, with flyback diode protection. Designed in KiCad with Gerber output.

---

## Key Components

| Component | Description |
|-----------|-------------|
| **L297** | Stepper motor controller IC – generates phase sequences from STEP/DIR |
| **L298N** | Dual full-bridge driver – up to 46V, 2A per channel (4A peak) |
| **Schottky Diodes (8x)** | Flyback protection for H-bridge inductive switching |
| **Screw Terminals (J1–J4)** | Motor coil and power supply connections |
| **Capacitors** | Power decoupling and filtering |
| **Current Sense Resistors** | Motor current feedback to L297 |

---

## Design Features
- Full-bridge bipolar drive for both stepper motor windings
- L297 auto-generates A/B/C/D phase winding sequences from STEP/DIR
- L298N handles high current switching up to 2A/channel continuously
- 8x Schottky flyback diodes protect driver from inductive voltage spikes
- Screw terminal blocks for easy motor and power wiring
- Complete Gerber files generated for PCB fabrication

---

## Signal Flow
```
MCU / Signal Source
       ↓
  STEP / DIR Inputs
       ↓
  L297 – Phase Sequencer (STEP/DIR → Phase A/B/C/D)
       ↓
  L298N – Dual H-Bridge Driver
       ↓
  Stepper Motor Coils (2-Phase Bipolar)
       ↑
  Flyback Diodes ← Inductive Kickback Protection
```

---

## Files Included
- two_phase_bipolar_stepper_motor.kicad_sch – Schematic
- two_phase_bipolar_stepper_motor.kicad_pcb – PCB Layout
- GREBBER_FILES_for_stepper_motor_controller/ – Gerber files for manufacturing
- Drill files/ – NC Drill files (PTH + NPTH)

---

