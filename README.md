# Quadrature Down Converter (QDC)

Design, LTspice simulation, and hardware realization of a quadrature down-conversion chain for the Analog Electronic Circuits course project at IIIT Hyderabad (Spring 2026).

## Team

- Navya Upadhyay
- Parth Tehlan
- Arnav Jain

## System overview

The design combines:

- a UA741 two-integrator quadrature oscillator with 1N4148 diode amplitude stabilization;
- dual NMOS switching mixers modeled in a TSMC 180 nm process;
- RC low-pass filters with a calculated 3.39 kHz cutoff; and
- an output amplifier stage for the final in-phase (I) and quadrature (Q) signals.

The oscillator drives the two mixer branches with phase-shifted local-oscillator signals. After mixing and low-pass filtering, the circuit retains the difference-frequency component while suppressing sum-frequency and higher-order components.

## Measured hardware results

| Parameter | Measured result |
| --- | ---: |
| Oscillator frequency | 143.8 kHz |
| Oscillator amplitude (I/Q) | 0.95 / 0.98 Vpp |
| Oscillator I-Q phase difference | 88.5 degrees |
| IF frequency at 150 kHz input | 4.97 kHz |
| Final I-Q phase difference | 86.2 degrees |
| Final output amplitude (I/Q) | 375 / 360 mVpp |
| LPF cutoff | 3.15 kHz |

## Repository contents

- `Oscillator_final.asc`: quadrature oscillator schematic
- `mixer_project.asc`: NMOS switching-mixer schematic
- `low_pass_project.asc`: low-pass-filter schematic
- `final_circuit.asc`: integrated QDC schematic
- `.raw`, `.fft`, and `.log` files: saved LTspice results
- `NavyaUpadhyay_ParthTehlan_ArnavJain_QDC_Report.pdf`: complete analysis, simulations, schematics, and hardware measurements

## Tools and components

LTspice, UA741 operational amplifiers, 1N4148 diodes, discrete NMOS transistors, TSMC 180 nm models, function generators, and a digital storage oscilloscope.

## Acknowledgment

Simulation files were shared with permission by Satvik Shrivastava (`blotify`) from a parallel implementation of the same course project. The linked report and hardware measurements document the implementation by Navya Upadhyay, Parth Tehlan, and Arnav Jain.

