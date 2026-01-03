# Water-Alarm

## Overview
This project marks the start of my journey into practical PCB design. I began learning KiCAD by following tutorial videos from DigiKey on YouTube, applying the concepts to design a simple water alarm PCB.

<p align="center">
<img alt="3D View - Intro" width="600px" src="3D View - Intro.png" />
</p>
<p align="center"> 
3D View of Board with components
<br clear="left">

##

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
One important design decision involved changing the MOSFET footprint from **TO-92_Inline [left]** to **TO-92_HandSolder [right]**. The inline footprint places the pads very close together (approximately 50 mils / 1.27 mm), which increases the risk of solder bridging during hand soldering. The hand-solder footprint provides greater pad spacing, making the board easier and safer to assemble while reducing the likelihood of short circuits.

<img align="left" alt="MOSFET_TO-92_Inline" width="400px" src="MOSFET_TO-92_Inline.png" />
<img align="left" alt="MOSFET_TO-92_HandSolder" width="365px"src="MOSFET_TO-92_HandSolder.png" />
<br clear="left">
<p align="center"> 
MOSFET Inline Footprint [left] & MOSFET HandSolder Footprint[right]
<br clear="left">
  


## Schematic

<p align="center">
  <img  alt="Schematic"  src="Water_Alarm_Schematic.png" width="600" />
</p>
<p align="center"> 
Schematic of Water Alarm Circuit
<br clear="left">
<br clear="left">
  
- External DC supply to connect via DC Barrel Jack (**J1**).
- Power Flags (**PWR_FLAGs**) used to indicate valid power sources to Electrical Rules Checker (ERC). 
- Voltage Supply (**VCC**) rail powers the buzzer, LED indicator, and MOSFET drain.

- Screw Terminal (**J2**) provides an external trigger input (e.g. water sensor electrodes).
- When water touches the contacts, conductivity will increase, leading to the gate voltage rising, activating the alarm.
- MOSFET Gate is driven by sensor input; drain controls current to buzzer.
- Buzzer activates when MOSFET conducts.

- Resistor 1 (**R1, 10MΩ**) acts as a pull-down resistor, keeping the MOSFET OFF when input (**J1**) is not connected to any supply (VCC) or ground.
- C1 (1nF) filters fast transients and reduces false triggering due to noise by absorbing any high-frequency signals.
- RC network improves the stability of the gate signal.

- LED provides visual indication of system power/alarm state.
- Design supports either external 12V supply or 9V battery source.
- However, only one power source should be connected at a time.


## PCB Layout
### Board size:

<img align="left" alt="Board Dimensions" width="480px" src="PCB_Board_Dimensions.png" />
<img align="left" alt="Board Dimension - 3D" width="483px" src="PCB_Board_Dimension_3D.png" />
<br clear="left">
<br clear="left">
<p align="center"> 
Dimensions: 52.84 x 44.03mm
<br clear="left">
  
##
### Buzzer Design:

<p align="center">
<img alt="Buzzer Design Symbol Editor" width="500px" src="Buzzer_Design_Symbol_Editor.png" />
</p>
<p align="center"> 
Buzzer Design using Symbol Editor
<br clear="left">
  
##
### PCB Copper Layers:
<img align="left" alt="Front Copper Layer" width="490px" src="Front Copper Layer.png" />
<img align="left" alt="Back Copper Layer" width="480px" src="Back Copper Layer.png" />
<br clear="left">
<p align="center"> 
Front Copper Layer & Back Copper Layer
<br clear="left">
  
##
### PCB Board Layouts:
<p align="center">
<img alt="PCB_Board_Layout_angle" width="500px" src="PCB_Board_Layout_angle.png" />
</p>
<p align="center"> 
PCB Board layout - Angle view
<br clear="left">
  
##

<img align="left" alt="PCB_Board_Layout_top" width="375px" src="PCB_Board_Layout_top.png" />
<img align="left" alt="PCB_Board_Layout_bottom" width="398px" src="PCB_Board_Layout_bottom.png" />
<br clear="left">
<p align="center"> 
Top View & Bottom View
<br clear="left">
  
##

<img align="left" alt="3D View_top" width="400px" src="3D View_top.png" />
<img align="left" alt="3D View_angle" width="335px" src="3D View_angle.png" />
<br clear="left">
<p align="center"> 
3D View: How the board will look with the components added
<br clear="left">
  
##

<img align="left" alt="3D View_angle2" width="358px" src="3D View_angle2.png" />
<img align="left" alt="3D View_bottom" width="395px" src="3D View_bottom.png" />
<br clear="left">
<p align="center"> 
More 3D Views
<br clear="left">
  
##
