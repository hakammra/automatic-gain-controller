# Automatic Gain Controller

This repository contains the project files for our **Automatic Gain Controller (AGC)** project. The project focuses on designing, simulating, building, and testing an analog audio AGC circuit.

The circuit keeps the output audio level more stable when the input signal level changes. It uses op-amps for buffering and amplification, and a JFET as a voltage-controlled resistor for gain control.

## Project Summary

In many audio systems, the input signal is not constant. For example, a phone output, microphone signal, or recorded audio can change in level. If the input is too low, the output becomes weak. If the input is too high, the output can clip or distort.

To reduce this problem, this project uses an Automatic Gain Controller. When the input signal is weak, the circuit increases the gain. When the input signal is high, the circuit reduces the gain. This helps to keep the output level nearly constant.

## Main Features

- Analog AGC design for audio signals
- Input buffer to reduce loading effect
- Pre-amplifier stage for weak signals
- Main amplifier stage
- Peak detector for output level sensing
- Threshold setting
- Compression ratio control
- JFET-based voltage-controlled resistor
- Simulation and hardware testing
- Real audio testing using a mobile phone and speaker

## Main Components

- NE5532 operational amplifier
- 2N5457 JFET
- 1N4148 diode
- Resistors and capacitors
- Potentiometers for threshold and ratio settings
- Dual power supply
- Oscilloscope and function generator for testing

## Block Diagram

![AGC Block Diagram](media/images/agc_block_diagram_final.png)

## Repository Structure

```text
automatic-gain-controller/
├── README.md
├── docs/
│   └── report/
├── hardware/
│   ├── schematics/
│   └── breadboard/
├── simulation/
│   ├── proteus/
│   └── ltspice/
├── data/
│   └── test-results/
├── media/
│   ├── images/
│   └── videos/
└── references/
```

## Folder Details

| Folder | What to add |
|---|---|
| `docs/report` | Final report PDF, LaTeX source, and report images |
| `hardware/schematics` | Circuit schematic images, Proteus screenshots, and final circuit diagrams |
| `hardware/breadboard` | Breadboard photos and wiring photos |
| `simulation/proteus` | Proteus project files and simulation screenshots |
| `simulation/ltspice` | LTspice files if used |
| `data/test-results` | Oscilloscope readings, measured values, tables, and calculations |
| `media/images` | Block diagrams, waveforms, and report images |
| `media/videos` | Demonstration video link or video file |
| `references` | Datasheets, website links, and useful reference notes |

## Testing

The circuit was tested using a function generator and also using real audio from a mobile phone. The output was observed on an oscilloscope. A speaker was also connected to check the sound output.

During testing, the gain increased for weak input signals and reduced for stronger input signals. The output was not perfectly constant, but it was more stable than a normal fixed-gain amplifier.

## Performance Summary

| Parameter | Value |
|---|---|
| Input voltage range | 40 mV to 2 V |
| Output voltage range | 2 V to 10 V |
| Maximum gain | 100 |
| Minimum gain | 2.5 |
| Control voltage range | -6 V to 0 V |
| Frequency response | 100 Hz to 18 kHz |
| Noise level | Low |
| Clipping condition | No clipping under normal operation |

## Project Report

The final project report is available in:

```text
docs/report/G08_Automatic_Gain_Controller.pdf
```

## Demonstration Video

The demonstration video link can be found in:

```text
media/videos/demo-video.md
```

## Team

**Group 08**  
Department of Electronics and Telecommunication Engineering  
University of Moratuwa

## License

This project is for academic and learning purposes.
