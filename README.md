# Sensor Signal Conditioning and ADC Interface

A simulation-based analog front-end design developed using **LTspice 26.1.1**. The project demonstrates low-pass filtering, op-amp signal conditioning, reference voltage generation, and interfacing an analog signal with a 0–3.3 V ADC input range.

## Objectives

- Design an RC low-pass filter to attenuate higher-frequency components.
- Simulate op-amp-based signal conditioning.
- Generate a stable mid-supply reference of approximately 1.65 V.
- Shift and scale the conditioned signal to fit within a 0–3.3 V ADC input range.
- Verify circuit behaviour through transient and DC operating-point simulations.

## Circuit Overview

1. **RC low-pass filter:** R = 10 kΩ, C = 100 nF.
2. **Amplifier stage:** Op-amp-based signal conditioning.
3. **Reference generation:** A resistor divider and buffer provide approximately 1.65 V.
4. **ADC interface:** An op-amp stage shifts and scales the signal around the reference voltage.

## Simulation Results

| Parameter | Result |
|---|---:|
| RC cutoff frequency | 159.15 Hz |
| Reference voltage | 1.64998 V |
| ADC output DC operating point | 1.64985 V |
| ADC output minimum | 0.14113 V |
| ADC output maximum | 3.15856 V |
| ADC output peak-to-peak swing | 3.01743 V |

The simulated ADC output remains within the nominal 0–3.3 V range for the tested input signal.

## Tools Used

- LTspice 26.1.1
- Analog circuit simulation
- Transient analysis
- DC operating-point analysis
- SPICE measurement directives

## Repository Structure

- `simulation/` – LTspice schematic and supporting simulation files
- `screenshots/` – Circuit diagrams and simulation results
- `reports/` – Design notes and calculations

## Verification

The circuit was verified using LTspice simulation. The reported measurements are simulation results, not physical hardware measurements.

## Future Improvements

- Perform frequency-response and noise analysis across the complete frontend.
- Evaluate component tolerances and op-amp limitations.
- Explore ADC input protection and input loading effects.

## License

This project is licensed under the MIT License. See `LICENSE` for details.
