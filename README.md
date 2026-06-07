# Switched-Capacitor Based Floating Inverter Amplifier (FIA)

## Overview
[cite_start]This repository contains the design, simulation, and characterization of a Switched-Capacitor (SC) based Floating Inverter Amplifier (FIA)[cite: 5, 18]. [cite_start]As continuous CMOS scaling restricts supply voltages, traditional operational amplifiers face severe voltage headroom limitations[cite: 14]. [cite_start]This project explores the FIA as a highly efficient, compact, and energy-efficient alternative that eliminates the need for stacked tail-current sources[cite: 15, 16, 285]. 

## Project Architecture
[cite_start]The development and verification of the SC-FIA were carried out in Cadence Virtuoso across three progressive phases[cite: 60, 278]:

* [cite_start]**Phase 1: Ideal SC Amplifier Baseline** Designed a baseline switched-capacitor amplifier utilizing ideal switches and a Voltage-Controlled Voltage Source (VCVS)[cite: 6]. [cite_start]This phase verified the theoretical closed-loop voltage gain driven by charge conservation and validated correct non-overlapping clock timing[cite: 32, 280].
* [cite_start]**Phase 2: Differential FIA Characterization** Developed a fully differential FIA core utilizing matched CMOS inverter pairs powered dynamically by a floating reservoir capacitor[cite: 93, 94]. [cite_start]Time-averaged transconductance was extensively characterized using Python by sweeping transistor finger counts (15 to 200) and reservoir capacitance (8 pF to 128 pF), identifying an optimal performance knee-point near 95 pF.
* [cite_start]**Phase 3: Full System Integration** Integrated the characterized FIA core into the differential SC topology, replacing the ideal VCVS[cite: 203, 283]. [cite_start]The final circuit successfully demonstrated non-inverting discrete-time charge transfer and stable closed-loop amplification under low-voltage constraints[cite: 216, 254].

## Key Features
* [cite_start]**Tail-Current-Free Design:** Maximizes voltage headroom and enables robust operation at severely scaled supply voltages[cite: 261].
* [cite_start]**Enhanced Transconductance Efficiency:** Sums the transconductance of both NMOS and PMOS devices simultaneously during the active amplification phase[cite: 39, 40].
* [cite_start]**Inherent Self-Biasing:** The inverter-based architecture naturally self-biases without requiring complex continuous-time Common-Mode Feedback (CMFB) circuitry[cite: 262].
