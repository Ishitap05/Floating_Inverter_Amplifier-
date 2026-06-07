# Switched-Capacitor Based Floating Inverter Amplifier (FIA)

## Overview
This repository contains the design, simulation, and characterization of a Switched-Capacitor (SC) based Floating Inverter Amplifier (FIA).As continuous CMOS scaling restricts supply voltages, traditional operational amplifiers face severe voltage headroom limitations.This project explores the FIA as a highly efficient, compact, and energy-efficient alternative that eliminates the need for stacked tail-current sources. 

## Project Architecture
The development and verification of the SC-FIA were carried out in Cadence Virtuoso across three progressive phases:

**Phase 1: Ideal SC Amplifier Baseline** Designed a baseline switched-capacitor amplifier utilizing ideal switches and a Voltage-Controlled Voltage Source (VCVS). This phase verified the theoretical closed-loop voltage gain driven by charge conservation and validated correct non-overlapping clock timing.
***Phase 2: Differential FIA Characterization** Developed a fully differential FIA core utilizing matched CMOS inverter pairs powered dynamically by a floating reservoir capacitor. Time-averaged transconductance was extensively characterized using Python by sweeping transistor finger counts (15 to 200) and reservoir capacitance (8 pF to 128 pF), identifying an optimal performance knee-point near 95 pF.
***Phase 3: Full System Integration** Integrated the characterized FIA core into the differential SC topology, replacing the ideal VCVS.The final circuit successfully demonstrated non-inverting discrete-time charge transfer and stable closed-loop amplification under low-voltage constraints.

## Key Features
**Tail-Current-Free Design:** Maximizes voltage headroom and enables robust operation at severely scaled supply voltages.
***Enhanced Transconductance Efficiency:** Sums the transconductance of both NMOS and PMOS devices simultaneously during the active amplification phase.
***Inherent Self-Biasing:** The inverter-based architecture naturally self-biases without requiring complex continuous-time Common-Mode Feedback (CMFB) circuitry.
