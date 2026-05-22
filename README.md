# Doherty-Load-Modulation-Simulation-Testbench

## Motivation

In practical Doherty PA design, the output network's load modulation behavior should be validated in EDA **before** co-simulating with active transistors.
Here is an example ADS testbench for simulating a Doherty PA output matching network. It plots the impedances presented to the main and auxiliary amplifiers and the network loss.

## Setup

- Main and auxiliary amplifiers are modeled as **ideal current sources** with a **90° phase offset**.
- Transistor parasitic capacitance needs to be included as part of the network.
- Current probes monitor the impedance seen by each amplifier as input drive is swept.
- The current profile follows **classical parallel Doherty theory**: the main current ramps linearly from zero to peak, while the auxiliary current stays at zero until 6 dB back-off, then ramps linearly to peak.
