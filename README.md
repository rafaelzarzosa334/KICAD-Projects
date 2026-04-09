# ±12V Dual Rail Power Supply for High-Voltage Measurement System

## Overview
This project is a compact ±12V dual-rail power supply designed to support precision analog circuitry, specifically op-amp buffering stages used in a high-voltage resistive-capacitive divider for plasma diagnostics.

The supply provides stable, low-noise positive and negative voltage rails required for accurate signal conditioning of fast, high-voltage transients (~kV range) measured in a plasma jet environment.

---

## Design Objectives
- Generate stable ±12V rails from a single DC input source  
- Provide low-noise power suitable for sensitive analog measurements  
- Support op-amps (e.g., OPA140, ADA4622) used in high-impedance buffering  
- Maintain electrical isolation from high-voltage measurement nodes  
- Ensure robust operation in a lab environment with fast transient events  

---

## System Description

### Input Stage
- External DC input (via barrel jack)
- Designed to interface with an isolated DC-DC converter module (±12V output)

### Power Conversion
- Dual-rail generation using an isolated DC-DC converter
- Provides symmetric +12V and -12V rails for op-amp operation

### Filtering & Decoupling
- Bulk capacitors for low-frequency ripple suppression  
- Local ceramic decoupling capacitors placed near op-amp supply pins  
- Layout optimized to minimize noise coupling into analog signal paths  

### Distribution
- Power rails routed to multiple analog channels (HV divider outputs)
- Ground plane used for consistent reference and noise reduction  

---

## PCB Design Considerations

### Noise Mitigation
- Solid analog ground plane to reduce impedance and noise  
- Short trace lengths for power delivery to critical components  
- Separation between power and signal routing where possible  

### High-Voltage Environment Awareness
- Physical separation between low-voltage power circuitry and HV measurement inputs  
- Consideration of creepage and clearance distances in mixed-voltage system  

### Connectorization
- Barrel jack input for easy lab integration  
- Output headers for distributing ±12V rails to multiple channels  

---

## Applications
- High-voltage probe systems  
- Plasma diagnostics instrumentation  
- Analog signal conditioning circuits  
- General-purpose dual-rail op-amp power supply  

---

## Key Components
- Isolated DC-DC converter (±12V output)  
- Decoupling capacitors (ceramic and bulk)  
- Low-noise op-amp compatibility (OPA140, ADA4622, etc.)  

---

## Files Included
- KiCad Project (`kicad Project 9.0`)  
- KiCad schematic (`kicad Schematic 9.0`)  
- PCB layout (`KiCad Board 9.0`)  
- Fabrication files (`Gerber`)  
- Board rendering (`.png`)  

---

## Design Challenges & Solutions

### Challenge: Noise Sensitivity in Measurement System
High-voltage transient measurements require extremely clean supply rails to avoid corrupting buffered signals.

**Solution:**  
Implemented local decoupling at each op-amp and maintained a continuous ground plane to reduce noise coupling.

---

### Challenge: Integration with HV Divider System
The power supply operates in close proximity to high-voltage circuitry (~kV), introducing potential interference and safety concerns.

**Solution:**  
Maintained physical and electrical separation between HV and low-voltage domains and designed layout with careful routing and spacing.

---

### Challenge: Stable Dual-Rail Generation
Ensuring symmetric and stable ±12V rails under varying load conditions.

**Solution:**  
Used an isolated DC-DC converter with appropriate bulk capacitance and distribution strategy to maintain voltage stability.

---

## Future Improvements
- Add onboard voltage regulation for tighter rail stability  
- Include LED indicators for rail status  
- Improve connector robustness for repeated lab use  
- Perform noise characterization and ripple measurements  

---

## Author
Rafael Larsen Zarzosa  
Mechanical Engineering Student – Embry-Riddle Aeronautical University  
Undergraduate Research Assistant – Space and Atmospheric Instrumentation Lab (SAIL)
