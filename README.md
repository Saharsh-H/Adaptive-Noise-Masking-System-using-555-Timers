# Multi-Band Adaptive Noise Masking System using 555 Timers

An Analog Circuits Laboratory project that explores **adaptive noise masking** using analog signal processing and custom **555 timer-based voltage-controlled oscillators (VCOs)**.

Instead of cancelling unwanted sound, the system analyzes ambient audio and generates adaptive masking tones across multiple frequency bands, reducing the perceived impact of environmental noise.

---

## 📖 Project Overview

Traditional noise reduction systems attempt to remove unwanted sound. This project takes a different approach by implementing an **adaptive noise masking system** entirely using analog circuits.

The incoming audio signal is divided into multiple frequency bands. Each band's intensity is converted into a control voltage that drives a dedicated 555 timer VCO. The generated tones are then mixed and amplified to produce a masking signal that adapts to the surrounding acoustic environment.

### Key Idea

| Detected Noise | Generated Masking Tone |
|---------------|-----------------------|
| Low Frequency Noise | Low Frequency Tone |
| Mid Frequency Noise | Mid Frequency Tone |
| High Frequency Noise | High Frequency Tone |

---

## 🏗️ System Architecture

```text
Microphone
    │
    ▼
Signal Splitter
    │
 ┌──┼──┐
 ▼  ▼  ▼
LPF BPF HPF
 │   │   │
 ▼   ▼   ▼
Envelope Detectors
 │   │   │
 ▼   ▼   ▼
555 Timer VCOs
 │   │   │
 └──┼──┘
    ▼
Masking Mixer
    ▼
Amplifier
    ▼
Speaker
```

---

## ⚙️ Circuit Design

### Multi-Band Filtering

The captured audio signal is separated into:

- Low-Pass Filter (LPF)
- Band-Pass Filter (BPF)
- High-Pass Filter (HPF)

This allows the system to independently analyze different regions of the frequency spectrum.

### Envelope Detection

Each filtered signal is passed through an envelope detector that converts the AC audio waveform into a DC control voltage proportional to the signal strength.

### Custom 555 Timer VCO

Each frequency band drives a dedicated NE555-based voltage-controlled oscillator. As the control voltage changes, the oscillator frequency changes accordingly, generating adaptive masking tones.

### Signal Mixing and Amplification

The outputs of all VCOs are combined using a mixer stage and then amplified before being sent to the speaker.

---

## 🔩 Components Used

- NE555 Timer ICs
- LM358 Operational Amplifiers
- Resistors and Capacitors
- Diodes for Envelope Detection
- Audio Amplifier Stage
- Speaker Output
- Power Supply

---

## 📁 Repository Structure

```text
.
├── Project Report.pdf
├── Multisim Files/
└── README.md
```

---

## 🎥 Demonstration Video

Watch the complete project demonstration here:

https://www.youtube.com/watch?v=h92l8Er9oFM

The demonstration showcases:

- Multi-band filtering
- Envelope detection
- Custom 555 timer VCO operation
- Adaptive frequency response
- Complete system functionality

---

## 📄 Documentation

The complete design, circuit schematics, simulation results, and project details are available in:

- `Project Report.pdf`

---

## 👥 Credits & Contributors

This project was created as part of the **Electronics Lab course at IIIT Bangalore**.

**Contributors:**
- Abel B Aliyas
- Gnan Ravi Gowda
- Karan Kandpal
- Pranava Swarup
- Saharsh S Hiremath
- Sahil Chauhan
- Tharun M
- Yash Sultania 

---
