# High-Voltage Measurement and Signal Conditioning System

## Overview
This repository contains the design and implementation of a high-voltage measurement and signal conditioning system developed for plasma diagnostics applications.

The system is designed to safely measure fast, high-voltage transients (~kV range) and convert them into accurate, low-noise signals suitable for standard laboratory measurement equipment such as oscilloscopes and digitizers.

The project is divided into two primary subsystems:
1. High-Voltage Resistive-Capacitive Divider and Buffer
2. ±12V Dual Rail Power Supply

Together, these systems form a complete signal chain from high-voltage input to conditioned, measurable output.

---

## System Architecture

### High-Voltage Divider and Buffer
- Scales high-voltage signals down to a safe range  
- Uses resistive-capacitive compensation to preserve transient response  
- Incorporates op-amp buffering for impedance matching and signal integrity  

### ±12V Dual Rail Power Supply
- Provides stable, low-noise ±12V rails  
- Powers the op-amp buffering stages  
- Designed to operate reliably in a high-noise, high-voltage lab environment  

---

## Key Engineering Focus Areas
- High-voltage safety (creepage, clearance, isolation)  
- Signal integrity and bandwidth preservation  
- Noise reduction and grounding strategy  
- Impedance matching to 50 Ω measurement systems  
- Robust PCB design for mixed-voltage environments  

---

## Applications
- Plasma diagnostics instrumentation  
- Pulsed power systems  
- High-voltage probe development  
- Precision analog signal conditioning  

---

## Repository Structure
/High_Voltage_Divider_Circuit_KiCad/        → High-voltage measurement system  
/Power_Supply_Project_KiCad/       → Dual-rail power supply  

---

Each project folder contains:
- KiCad schematics and PCB layouts  
- Fabrication (Gerber) files  
- Board renderings and documentation  

---

## Design Context
This system was developed as part of undergraduate research in plasma diagnostics, where accurate measurement of fast, high-voltage events is critical for understanding system behavior.

Special attention was given to maintaining measurement accuracy in a high-noise environment while ensuring safe operation around high-voltage sources.

---

## Author
Rafael Larsen Zarzosa  
Mechanical Engineering Student – Embry-Riddle Aeronautical University  
Undergraduate Research Assistant – Space and Atmospheric Instrumentation Lab (SAIL)
