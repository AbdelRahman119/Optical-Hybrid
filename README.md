# Optical-Hybrid

## Introduction

This VerilogA module, named "Hybrid_model," is designed to model a hybrid optical system with input parameters for electric field magnitudes and phases. It calculates the real and imaginary components of the electric field at four different points within the system.
Our hybrid consists of two 3dB couplers, one that couples the Electric field that carries the signal (Es) with the LO electric field (ELO) and the other coupler does the same thing but after giving the ELO and 90 degrees phase shift.

The four Output electric fields from the optical hybrid Equal:
- E1=1/√2(Es+ELO)
- E2=1/√2(Es-ELO)
- E3=1/√2(Es+j*ELO)
- E4=1/√2(Es-j*ELO)

## Module Inputs and Outputs

- **Inputs:**
  - Es_mag: Magnitude of the electric field for the source.
  - Es_phase: Phase of the electric field for the source.
  - Elo_mag: Magnitude of the electric field for the local oscillator.
  - Elo_phase: Phase of the electric field for the local oscillator.

- **Outputs:**
  - E1_real, E1_img: Real and imaginary components of electric field E1.
  - E2_real, E2_img: Real and imaginary components of electric field E2.
  - E3_real, E3_img: Real and imaginary components of electric field E3.
  - E4_real, E4_img: Real and imaginary components of electric field E4.

## Parameters

- **phase_err_degree:** Degree of phase error, defaulted to 0.
- **amplitude_error:** Amplitude error, defaulted to 0.

## Analog Behavior

The module includes an analog block where the real and imaginary components of the electric field are calculated based on the input parameters. Additionally, the phase error and amplitude error are accounted for in the calculations.

## Usage

1. **Input Parameters:** Provide the input parameters Es_mag, Es_phase, Elo_mag, and Elo_phase to the module.
2. **Simulation:** Simulate the VerilogA module using a compatible simulator, ensuring proper connection of input and output ports.
3. **Observation:** Analyze the output signals E1_real, E1_img, E2_real, E2_img, E3_real, E3_img, E4_real, and E4_img to understand the behavior of the hybrid optical system.
