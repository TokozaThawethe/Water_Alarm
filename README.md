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
- How the circuit works (block-level) : The only way for the electricity to flow through both the wires in the screw terminal is when the circuit is closed (completed). This will only happen when water connects them. This will send a voltage to the gate of the MOSFET transistor, causing it to allow the voltage from the DC Jack Barrel to power the buzzer. The buzzer sounds, signalling you that there is a water problem which requires your attention. This circuit can prevent disaster from escalating.
- Why key arrangement were used: One key choice was when the footprint of the MOSFET was changed from a....

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
