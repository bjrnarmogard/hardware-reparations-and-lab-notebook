# NE555 Lab Circuit - Resistance Measurement Setup

This project documents the schematic design, simulation, and hardware layout of a laboratory experiment circuit based on the classic NE555 timer integrated circuit. The design translates concepts from text to a production-ready hardware prototype.

## Reference & Inspiration
- **Source:** *Practical Electronics* Magazine, **September 2026** issue.
- **Section:** *Circuit Surgery* – "Measuring resistance with a 555 timer chip".
- **Implementation:** The LTspice simulation parameters follow the magazine's methodology for verifying stable oscillation and signal behavior. The subsequent KiCad schematic capture, custom footprint assignment for laboratory hand-soldering, and 3D PCB layout verification were performed independently as standalone hardware development.

## Technical Summary
- **Circuit Architecture:** Configured as an astable multivibrator (oscillator) designed to output a stable square wave where frequency variations can be used to determine resistance parameters.
- **Signal Integrity:** Includes local 0.1µF decoupling capacitors placed closely to the VCC/GND pins of the ICs to suppress switching noise and stabilize the internal comparator thresholds.
- **PCB Design:** Developed in KiCad using Through-Hole Technology (THT) footprints (DIP-8 for the NE555P) to ensure high thermal tolerance during assembly with unregulated soldering irons. Traces are routed using clean 45-degree angles to optimize copper geometry and maintain manufacturing rule compliance. 
- **Testing Interface:** Dedicated 1-pin headers are integrated directly at the output pins (OUT) to serve as physical test points for secure oscilloscope probing.

## Tools Used
- **LTspice:** Analog circuit simulation and waveform verification.
- **KiCad EDA:** Schematic capture, trace routing, and 3D visualization.
