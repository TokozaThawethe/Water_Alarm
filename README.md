# Water-Alarm

## Overview
This project marks the start of my journey into practical PCB design. I began learning KiCAD by following tutorial videos from DigiKey on YouTube, applying the concepts to design a simple water alarm PCB.

### What the Circuit Does
My first hands-on attempt at designing a printed circuit board.
- Designed as a basic water detection alarm.
- When water bridges the positive voltage supply to the gate of a MOSFET, it acts as a switch, powering a loud buzzer to alert you. This could help notify you of a potential flood, a leak under the sink, or a toilet overflow—anywhere water shouldn’t be.
- A simple, portable solution to detect unwanted water.
- The DigiKey tutorial videos I followed are linked at the bottom of this page.

### Why I Built This Project
The goal was to learn the fundamentals of PCB design and familiarise myself with the KiCAD environment through hands-on experience. It’s a simple application, but every journey starts somewhere, and this project gave me a solid foundation to build on.


## Circuit Design
### How the circuit works
Under normal conditions, the circuit remains open and no current flows through the screw terminal. When water bridges the terminals, the circuit is completed, allowing a voltage to be applied to the gate of the MOSFET. This switches the MOSFET on, enabling power from the DC barrel jack to drive the buzzer. The audible alert provides immediate indication of water presence, allowing early intervention and helping prevent escalation into more serious damage.

### Key Design Decisions
One important design decision involved changing the MOSFET footprint from TO-92_Inline to TO-92_HandSolder. The inline footprint places the pads very close together (approximately 50 mils / 1.27 mm), which increases the risk of solder bridging during hand soldering. The hand-solder footprint provides greater pad spacing, making the board easier and safer to assemble while reducing the likelihood of short circuits.

images/MOSFET_TO-92_HandSolder.png = <img width="323" height="320" alt="MOSFET_TO-92_HandSolder" src="https://github.com/user-attachments/assets/b2eb7f3b-398f-493d-a5be-37fab3caeb17" />

![New MOSFET](images/MOSFET_TO-92_HandSolder.png)


<!-- <img width="355" height="320" alt="MOSFET_TO-92_Inline" src="https://github.com/user-attachments/assets/7c4b0f98-05f6-4f2c-994e-e8294588d87a"> -->
<!-- <img width="323" height="320" alt="MOSFET_TO-92_HandSolder" src="https://github.com/user-attachments/assets/36c4f26c-ec3d-42fa-b312-84b54043bf33" /> -->



________________
## Schematic
Include:
- Screenshot of schematic
- Notes on important sections

## PCB Layout
- Board size:
- Number of layers:
- Design rules considered
- Screenshot of PCB layout

## Files Structure
```text
schematic/
pcb/
images/
fabrication/
