# Automatic Gain Controller

<p align="center">
  <img src="media/images/agc_block_diagram_final.png" alt="AGC Block Diagram" width="750">
</p>

<p align="center">
  <b>Analog audio Automatic Gain Controller using op-amps and a JFET-based voltage-controlled resistor.</b>
</p>

---

## Project Overview

This repository contains the project files for our **Automatic Gain Controller (AGC)** project. The project focuses on designing, simulating, building, and testing an analog audio AGC circuit.

The circuit keeps the output audio level more stable when the input signal level changes. When the input signal is weak, the circuit increases the gain. When the input signal is high, the circuit reduces the gain. This helps to reduce clipping and keeps the output level more constant than a normal fixed-gain amplifier.

The AGC was tested using simulation, a function generator, and real audio from a mobile phone. The output was observed using an oscilloscope and also checked using a speaker.

---

## Main Features

- Analog AGC design for audio signals
- Input buffer to reduce loading effect
- Pre-amplifier stage for weak signals
- Main amplifier stage with gain control
- Peak detector for sensing output level
- User adjustable threshold setting
- User adjustable compression ratio control
- JFET-based voltage-controlled resistor
- Simulation and hardware testing
- Real audio testing using mobile phone and speaker

---

## System Block Diagram

<p align="center">
  <img src="media/images/agc_block_diagram_final.png" alt="Automatic Gain Controller Block Diagram" width="850">
</p>

The forward signal path is:

```text
Input -> Buffer -> Pre-Amplifier -> Amplifier -> Low-Pass Filter -> Output
```

The feedback path is taken from the amplifier output before the low-pass filter. The feedback signal goes through the peak detector, subtractor, compression ratio control, and voltage-controlled resistor. The voltage-controlled resistor then controls the signal level between the pre-amplifier and the amplifier.

---

## Circuit and Hardware

### Complete Circuit

<p align="center">
  <img src="media/images/report-pages/page-11.png" alt="Complete AGC Circuit" width="850">
</p>

### Breadboard Implementation

<p align="center">
  <img src="media/images/report-pages/page-15.png" alt="Breadboard Implementation" width="600">
</p>

---

## Simulation Results

### Input and Output Waveforms

<p align="center">
  <img src="media/images/report-pages/page-13.png" alt="Simulation Waveforms" width="750">
</p>

The simulation shows that the output level is more controlled compared with the changing input signal. The peak and control voltage waveform also shows how the feedback control signal changes according to the output level.

---

## Hardware Testing Results

The circuit was tested using audio input while changing the input volume. The output waveform was observed on an oscilloscope. The circuit was also connected to a speaker to check the practical sound output.

<p align="center">
  <img src="media/images/report-pages/page-17.png" alt="Oscilloscope Testing Results" width="750">
</p>

During testing, weak input signals were amplified and stronger input signals were controlled by reducing the gain. The output was not perfectly constant, but it stayed more stable than a normal fixed-gain amplifier.

---

## Main Components

| Component | Value / Part Number | Purpose |
|---|---|---|
| Operational amplifier | NE5532 | Buffer, amplification, and control stages |
| JFET | 2N5457 | Voltage-controlled resistor for gain control |
| Diode | 1N4148 | Peak detector section |
| Potentiometers | 100 kΩ | Threshold and compression ratio control |
| Capacitors | 2.2 µF, 100 nF, 10 µF | Coupling, filtering, and smoothing |
| Resistors | Various values | Gain setting, biasing, and control path |
| Audio jack | 3.5 mm audio jack | Audio input connection |
| Power supply | ±12 V | Dual supply for op-amp circuit |

---

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
| Output/Input variation ratio | 1/100 |

---

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

| Folder | Description |
|---|---|
| `docs/report` | Final report PDF, LaTeX source, and report files |
| `hardware/schematics` | Circuit schematic images and diagrams |
| `hardware/breadboard` | Breadboard photos and wiring photos |
| `simulation/proteus` | Proteus project files and simulation screenshots |
| `simulation/ltspice` | LTspice files if used |
| `data/test-results` | Oscilloscope readings, measured values, and calculations |
| `media/images` | Block diagrams, waveforms, and report images |
| `media/videos` | Demonstration video link |
| `references` | Datasheets, websites, and useful reference notes |

---

## Project Report

The final project report is available here:

```text
docs/report/G08_Automatic_Gain_Controller.pdf
```

---

## Demonstration Video

The demonstration video link can be found here:

```text
media/videos/demo-video.md
```

---

## Team

**Group 08**  
Department of Electronics and Telecommunication Engineering  
University of Moratuwa

### Group Members

- 230020R - Ahamed A.M.S.
- 230224V - Hakam M.R.A.
- 230654M - Umair A.
- 230581K - Santhosh S.

---

## Notes

This repository is created for academic and learning purposes. It contains the report, simulation files, circuit diagrams, hardware photos, test results, and reference materials related to the Automatic Gain Controller project.
