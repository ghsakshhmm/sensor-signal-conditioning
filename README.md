# Sensor Signal Conditioning and ADC Interface

This project is about designing and simulating an analog front end using **LTspice 26.1.1**. It takes a small input signal, filters and conditions it, and adjusts it to fit within a 0–3.3 V ADC input range.

## What I wanted to do

- Design an RC low-pass filter to reduce higher-frequency components.
- Use op-amp stages for signal conditioning.
- Generate a 1.65 V reference voltage.
- Shift and scale the signal for a 0–3.3 V ADC input.
- Check the circuit using different LTspice simulations.

## Circuit Overview

1. **RC Low-Pass Filter:** Uses a 10 kΩ resistor and 100 nF capacitor to filter the input signal.
2. **Amplifier Stage:** Amplifies the filtered signal.
3. **Reference Voltage:** Uses a resistor divider and buffer to generate approximately 1.65 V.
4. **ADC Interface:** Shifts and scales the signal so that the output stays within the intended ADC input range.

## Simulation Results

| Parameter | Result |
|---|---:|
| RC filter cutoff frequency | 159.15 Hz |
| Reference voltage | 1.64998 V |
| ADC output DC voltage | 1.64985 V |
| Minimum ADC output | 0.14113 V |
| Maximum ADC output | 3.15856 V |
| Peak-to-peak output swing | 3.01743 V |

The simulated output stays within the nominal 0–3.3 V range for the input signal tested.

The cutoff frequency was calculated using:

\[
f_c=\frac{1}{2\pi RC}
\]

For R = 10 kΩ and C = 100 nF, the cutoff frequency is approximately 159.15 Hz.

## Simulations Performed

- Transient response
- DC operating-point analysis
- AC frequency-response analysis
- Noise analysis
- Minimum and maximum output voltage measurements using SPICE directives

## Tools Used

- LTspice 26.1.1
- Analog circuit simulation
- SPICE measurement directives

## Files

- `Sensor_Frontend_ADC_Interface.asc` - Main LTspice schematic
- `Sensor_Frontend_ADC_Interface.log` - Simulation log and measurement results
- `Sensor_Frontend_ADC_Interface.plt` - Saved waveform plot settings
- `screenshots/` - Circuit diagrams and simulation results
- `LICENSE` - MIT License

## How to Run

1. Open `Sensor_Frontend_ADC_Interface.asc` in LTspice.
2. Run the simulation.
3. Check the waveforms and output voltages.
4. Open the simulation log to see the measured values.

## Limitations and Future Scope

This project has been designed and tested in simulation only. No physical hardware testing has been performed.

Some improvements that could be explored next:
- Study the effect of component tolerances.
- Check op-amp limitations and ADC input loading.
- Explore input protection for the ADC.
- Test the circuit with different sensor signals.
- Compare simulation results with a physical circuit in the future.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
