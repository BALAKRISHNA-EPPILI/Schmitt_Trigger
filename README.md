# Schmitt_Trigger
This repository presents the design of Analysis of CMOS Schmitt Trigger implemented using Synopsys Custom Compiler on 28nm Technology .


# Table of Contents
 * [Abstract](#Abstract)
 * [Introduction](#Introduction)
 * [Schmitt_Trigger](#Schmitt-Trigger)
 * [Four-Quadrant Analog Multiplier](#Four-Quadrant-Analog-Multiplier)
 * [Tools Used](#Tools-Used)
 * [Pre-Layout Schematics and Simulations](#Pre-Layout-Schematics-and-Simulations)
 * [Netlist of the Circuit](#Netlist-of-the-Circuit)
 * [Observations](#Observations)
 * [Author](#Author)
 * [Acknowledgements](#Acknowledgements)
 * [References](#References)

# Abstract
   Schmitt Trigger circuit is extensively utilized in analog and digital circuit (ADC) to clear up the noise problem. Hysteresis is a common disadvantage of the Schmitt Triggers that is decided through the tool dimensions, technique parameters and supply voltages. This situation gives a Schmitt Trigger circuit capability that it could perform at low voltage. The proposed circuit is designed based on Conventional  Schmitt Trigger through manipulating the association of transistors’  width-period ratio.
   
   In this paper, we are going to do the analysis of Conventional Schmitt  Trigger in 28 nm technology. We are going to carry out the whole  simulation of the proposed design of Conventional Schmitt Trigger in Synopsys custom design platform tool Software which is an EDA tool in  which we simulate our circuit in Synopsys custom design compiler tool.  From the simulation results, it has been observed that the proposed  design can perform at a low voltage of 1.8V. The circuit gives much less  propagation delay as compared to the traditional circuit. It may be widely utilized in various low voltage analogous and digital applications. 


# Introduction:

   The Schmitt trigger, delivered through Otto Schmitt in 1930s (Schmitt, 1938), and has been generally used with inside the area of communication and signal processing techniques for enhancing on/off control, decreasing the noise results in triggering devices, analog to digital conversion(ADC), and some of different rising packages such as frequency doublers, retinal focalaircraft sensors, sub-threshold SRAM, sensors, pulse width modulation  circuits, wi-fi transponders, FPGA primarily based totally gadget and sensors, etc.

<p align="center">
  
![schmitt trigger symbol](https://user-images.githubusercontent.com/88899069/155727948-4430a09e-9140-44ea-a840-63fa1726d8e6.jpg)

  Fig. 1: Analog Multipier 
</p>


           Vout = (v1*v2)/k

   It is used widely in the field of telecommunication, analog signal processing, Instrument systems etc. Analog multiplier is categorized as single quadrant which means that when both the input is positive/negative (i.e., same unipolar), two-quadrant means when one input has a positive voltage and other input could have positive or negative voltage (i.e., x is bipolar and y is unipolar), four-quadrant multiplier means when both the input is either positive or negative (i.e., when x is bipolar and y is also bipolar). 
So, in this paper, we are going to make the CMOS low power consumption analog multiplier of four-quadrant multiplier. As, four-quadrant analog multiplier is a very useful basic building block in many circuits like adaptive filters, phase-frequency detection, frequency double, function generator, frequency shifters, etc. It is also used in modulation, pll (phase-locked loop), frequency mixer, etc.

# Analog Multiplier:

<p align="center">
  

  Fig. 1: Analog Multipier 
</p>



	   	Vdd = Supply voltage of the circuit
	   	GND = Ground


# Four-Quadrant Analog Multiplier:

   The main purpose of designing a four-quadrant analog multiplier is to eliminate extra voltage reference to make a compact circuit design. By implementing and simulating this circuit in Synopsys Custom compiler tool using CMOS 28nm Technology, the device performance, density and low power consumption will be improved and achieved. The proposed design consists of a pair of common source amplifier with input transistors and the output that it gives is the square function of its input voltages v1 and v2. It contains a total of 10 transistors in which 8 are PMOS and 2 are comprised of NMOS including two resistors R1 and R2 to make the transistor to work in the proper region and the value of resistors has to be taken accordingly at the time of the simulation.  Transistor m1 to m8 acts as a non-linear cancellation path in a square root circuit. The output which comes from transistors m9 and m10 are directly going into the square root circuit block to produce differential output voltage or current which is just the product of the input signal v12 and v34. Here, v12 is the difference between v1 and v2 signal while v34 is the difference between v3 and v4 input signal and the resultant output signal Vout will be the differential output of vout1 and vout2. 

<p align="center">
	
 ![analog multipier](https://user-images.githubusercontent.com/90523478/155011823-c72c46ea-1cf8-4c27-8211-9dcab0887217.jpg)
                            Fig. 2: Four-Quadrant Analog Multiplier
	
</p>
<p>
   Hence, on observing the output waveform we conclude that the given circuit become capable to operate with the input voltage and also the requirement of low power consumption for operating the circuit is also achieved.  (And also, the requirement of achieving low power consumption also met). So, a new square root circuit can be used to realize a CMOS four-quadrant analog multiplier has been given. For the verification purpose of the multiplier circuit, a performance simulation result has been given.

# Tools Used:

<b>• Synopsys Custom Compiler:</b></br>
&emsp;The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

<b>• Synopsys 28nm PDK:</b></br>
&emsp;The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Pre-Layout Schematics and Simulations:

## Schematics:

### Four-Quadrant Analog Multiplier:


<p align="center">
  
  Fig. 3: Four-Quadrant Analog Multiplier
</p>
<p align="center">
  
  Fig. 4:Four-Quadrant Analog Multiplier Symbol
</p>

### Buffer:
This component is used to convert the generated sine wave to a proper square pulse and is placed at the output of the VCO. This is nothing but a couple of inverters placed in series. 
<p align="center">

  Fig. 5: Buffer Schematic
</p>
<p align="center">
 
  Fig. 6: Buffer Symbol
</p>

### Four-Quadrant Analog Multiplier:
The schematic of Four-Quadrant Analog Multiplier has been created using the above cells and a few transistors as shown in the below figure.
<p align="center">
  
  Fig. 7: Four-Quadrant Analog Multiplier Schematic
</p>

## Simulations:
### Transient Analysis:
   After creating and saving the schematic go to 'Tools' and open 'Primewave' to start the simulation. In the Primewave select the 'model file' i.e the '28nm PDK's .lib file presentin the HSPICE folder. After this select the 'tran' analysis in the analysis window and give the 'Start', 'Stop', and 'Step Size' parameters and save it. Then add the outputs which needs to be plotted by selecting the nets on the schematic.</br>
One other thing we need to keep in mind is that here we have loop for which an initial condition needs to be declared. For that, we have to go to 'Setup -> Convergance aids' and select the net for which we want to set an initial condition.Then go to 'Simulations -> Netlist and Run' to generate a netlist and run the simulation to get the below output.
<p align="center">
  
  Fig. 8: Four-Quadrant Analog Multiplier Transient Analysis
</p>

# Netlist of the Circuit:


# Observations:


# Author:
• Vanshika Tanwar, B.Tech(ECE), Dronacharya Group of Institutions, Greater Nodia, Uttar Pradesh.

# Acknowledgements:

- [Synopsys India](https://www.synopsys.com/)
- [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Indian Institute Of Technology (IIT) Hyderabad](https://iith.ac.in/)
- [Kunal Ghosh](https://github.com/kunalg123), Founder, VSD Corp. Pvt. Ltd
-   [VLSI System Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)

# References:
