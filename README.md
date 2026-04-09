# High-Voltage Resistive-Capacitive Divider and Buffered Measurement System

## Overview
This project is a high-voltage resistive-capacitive (RC) divider designed to safely measure fast, high-voltage transients (~kV range) in plasma diagnostics applications. The system scales down high-voltage signals to a measurable range and incorporates an op-amp buffering stage to accurately interface with 50 Ω digitizers and oscilloscopes.

The design is intended for use in a plasma jet experimental setup, where rapid voltage changes and electromagnetic interference require careful signal conditioning and impedance management.

---

## Design Objectives
- Accurately scale high-voltage signals (~kV) to safe, measurable levels  
- Preserve fast transient response (µs timescale)  
- Minimize signal distortion and bandwidth limitations  
- Provide impedance matching to measurement equipment (50 Ω systems)  
- Isolate measurement electronics from high-voltage domains  
- Ensure reliable operation in a noisy plasma environment  

---

## System Description

### Resistive Divider Network
- High-voltage resistive divider (e.g., 1 MΩ / 1 kΩ configuration)  
- Reduces input voltage by a factor of ~1000:1  
- Designed to handle high voltage while maintaining measurement accuracy  

### Capacitive Compensation
- Parallel capacitors added across divider resistors  
- Compensates for frequency-dependent behavior of the divider  
- Tuned to maintain waveform fidelity for fast transient signals  

### Buffering Stage
- Unity-gain op-amp buffer (OPA140)  
- High input impedance minimizes loading on divider  
- Low output impedance enables accurate signal transmission to measurement equipment  

### Output Interface
- Designed to drive 50 Ω input impedance (oscilloscope/digitizer)  
- Prevents amplitude attenuation and signal distortion due to loading effects  

---

## PCB Design Considerations

### High-Voltage Safety
- Careful creepage and clearance spacing between HV and low-voltage nodes  
- Physical separation of HV input traces from signal conditioning circuitry  
- Layout designed to reduce risk of arcing and unintended coupling  

### Signal Integrity
- Short trace paths for sensitive analog signals  
- Minimization of parasitic capacitance and inductance  
- Controlled routing to preserve high-frequency signal components  

### Grounding Strategy
- Dedicated analog ground plane  
- Proper return paths to reduce noise and ground loops  
- Shielding considerations when used inside a metal enclosure (Faraday cage)  

---

## Applications
- Plasma diagnostics and high-voltage experiments  
- Pulsed power systems  
- High-voltage probe design  
- Fast transient voltage measurement systems  

---

## Key Components
- High-voltage resistors (divider network)  
- Compensation capacitors (C0G/NP0 preferred for stability)  
- Precision op-amps (OPA140)  
- SMA or coaxial output connectors for signal integrity  

---

## Files Included
- KiCad Project (KiCad 9.0)  
- KiCad schematic (KiCad 9.0)  
- PCB layout (KiCad Board 9.0)  
- Fabrication files (Gerbers)  
- Board rendering (.png)  

---

## Design Challenges & Solutions

### Challenge: Signal Attenuation Due to Measurement Equipment
Direct connection of the divider to a 50 Ω oscilloscope input caused significant amplitude reduction.

**Solution:**  
Implemented a unity-gain op-amp buffer to isolate the divider from the load and provide a low-output-impedance signal to the measurement system.

---

### Challenge: Preserving Fast Transient Response
High-voltage pulses in the plasma system occur on microsecond timescales, requiring adequate bandwidth.

**Solution:**  
Introduced capacitive compensation across the divider to match time constants and preserve waveform fidelity.

---

### Challenge: Noise and Interference from Plasma Environment
The measurement system operates in a high-EMI environment with strong electromagnetic disturbances.

**Solution:**  
Used a grounded enclosure (Faraday cage), careful PCB layout, and shielding practices to minimize noise coupling.

---

### Challenge: High-Voltage Isolation
Sensitive electronics must be protected from kV-level input signals.

**Solution:**  
Maintained strict separation between HV and low-voltage regions and designed the divider to safely drop voltage before buffering.

---

## Future Improvements
- Characterize bandwidth and frequency response experimentally  
- Improve impedance matching for long cable runs  
- Add transient protection (TVS diodes, filtering stages)  
- Perform calibration against a commercial high-voltage probe  

---

## Author
Rafael Larsen Zarzosa  
Mechanical Engineering Student – Embry-Riddle Aeronautical University  
Undergraduate Research Assistant – Space and Atmospheric Instrumentation Lab (SAIL)
