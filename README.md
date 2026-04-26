# Fire Detection PCB 

## Project Overview
This project is a hardware-based Fire Detection System designed for real-time monitoring and safety alerts. The system utilizes an analog comparator architecture to detect thermal changes and trigger a dual-stage (audio-visual) alarm.

## Technical Specifications
- **Control Logic:** LM358 Operational Amplifier (Differential Comparator Mode)
- **Primary Sensor:** NTC Thermistor (Negative Temperature Coefficient)
- **Actuators:** 5V/9V Buzzer and High-Brightness LEDs
- **Power Management:** 9V DC input with integrated current-limiting resistors
- **Calibration:** Multi-turn Potentiometer for precision threshold tuning

## Hardware Components & Theory

### 1. LM358 Integrated Circuit (The Comparator)
The LM358 acts as the "brain" of the system. It compares two input voltages:
- **Reference Voltage ($V_{ref}$):** Set by the Potentiometer.
- **Sensor Voltage ($V_{sens}$):** Determined by the voltage divider containing the Thermistor.
When $V_{sens}$ crosses $V_{ref}$, the output swings high, activating the alarm circuit.

### 2. The Potential Divider & Potentiometer
- **Resistors:** Fixed resistors are used to bias the transistors and protect the LEDs from overcurrent.
- **Potentiometer:** Functions as a variable voltage divider, allowing for sensitivity calibration across different ambient environments.


## Chemical & Physical Principles

### The Sourcing Process (NTC Thermistor)
The detection relies on the **Negative Temperature Coefficient** of the semiconductor material:
1. **Thermal Excitation:** Heat energy increases the kinetic energy of atoms in the thermistor.
2. **Charge Carrier Generation:** This energy allows electrons to jump from the valence band to the conduction band.
3. **Resistance Drop:** The increase in free charge carriers decreases the electrical resistance ($R$).
4. **Voltage Detection:** As resistance drops, the voltage across the thermistor changes according to Ohm's Law ($V = I \times R$), providing the trigger signal for the LM358.

## PCB Fabrication Process
The PCB was developed through a standard chemical etching process:
1. **Layout Design:** Schematic and trace routing designed for signal integrity.
2. **Transfer:** The circuit pattern was transferred to a copper board.
3. **Etching:** A chemical bath (Ferric Chloride)(FeCl3) was used to remove unwanted copper, leaving the conductive traces.
4. **Assembly:** Components were manually soldered, ensuring cold-joint prevention for reliable operation in high-heat scenarios.

## Hardware Visuals
![Assembled PCB Build](<img width="1142" height="1600" alt="WhatsApp Image 2026-04-26 at 20 10 09" src="https://github.com/user-attachments/assets/1341b36d-df6e-4e2e-bd06-a6f48060d47d" />
)

---
*Developed as a practical study in Analog Circuit Design and Physical Computing.*
