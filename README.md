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
   Schmitt Trigger circuit is extensively utilized in analog and digital circuit (ADC) to clear up the noise problem. Hysteresis is a common disadvantage of the Schmitt Triggers
that is decided through the tool dimensions, technique parameters and supply voltages. This situation gives a Schmitt Trigger circuit capability that it could perform at low
voltage. The proposed circuit is designed based on Conventional  Schmitt Trigger through manipulating the association of transistors’  width-period ratio.
   
   In this paper, we are going to do the analysis of Conventional Schmitt  Trigger in 28 nm technology. We are going to carry out the whole  simulation of the proposed design of
Conventional Schmitt Trigger in Synopsys custom design platform tool Software which is an EDA tool in  which we simulate our circuit in Synopsys custom design compiler tool.
From the simulation results, it has been observed that the proposed  design can perform at a low voltage of 1.8V. The circuit gives much less  propagation delay as compared
to the traditional circuit. It may be widely utilized in various low voltage analogous and digital applications. 


# Introduction:

   The Schmitt trigger, delivered through Otto Schmitt in 1930s (Schmitt, 1938), and has been generally used with inside the area of communication and signal processing
techniques for enhancing on/off control, decreasing the noise results in triggering devices, analog to digital conversion(ADC), and some of different rising packages such as
frequency doublers, retinal focal-aircraft sensors, sub-threshold SRAM, sensors, pulse width modulation  circuits, wi-fi transponders, FPGA primarily based totally gadget and
sensors, etc.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155727948-4430a09e-9140-44ea-a840-63fa1726d8e6.jpg"></br>
  Fig.1: Schmitt Trigger
</p>


   A common disadvantage of Schmitt triggers is that the hysteresis is decided through different tools, dimensions, techniques, different parameters, factors and supply
voltages. As a result, the hysteresis varies with system conditions and a range of the parameters must be tolerated from chip to chip, area to area in addition to from batch to
batch. Several procedures had been proposed to implement a conventional Schmitt trigger. The switching thresholds are depending on the ratio of NMOS and PMOS. However, the
design exhibited racing phenomena depending on while the transition started. A low voltage Schmitt trigger is proposed on this paper that could function from 1.8V-2V at high
capacitance with much less propagation delay and strong hysteresis width by reducing the supply voltage

# Schmitt Trigger:

   A Schmitt trigger is a comparator circuit with hysteresis applied with the aid of using making use of positive feedback to the non-inverting input of a comparator or
differential amplifier, Schmitt trigger is an active circuit which converts an analog input signal to a digital output signal, the circuit is known as a cause due to the fact
the output keeps its price till the enter adjustments sufficiently to cause a change. In the non-inverting configuration, whilst the input is better than a designated
threshold, the output is high. When the input is below a different (lower) selected threshold the output is low, and when the input is among the 2 ranges the output keeps its
value. There is a near relation among the 2 forms of circuits: a Schmitt trigger may be transformed right into a latch and a latch may be transformed right into a Schmitt
trigger.
   
   Schmitt trigger devices are generally utilized in signal conditioning packages to remove noise from indicators utilized in digital circuits, mainly mechanical touch jump in
switches. They also are utilized in closed loop terrible comments configurations to implement rest oscillators, utilized in characteristic generators and switching power
supplies.
   
   The CMOS Schmitt trigger includes 3 NMOS transistors (N1, N2, and N3), and 3 PMOS transistors (P1, P2, and P3). It indicates the fundamental CMOS Schmitt trigger circuit
design.

The proposed Schmitt trigger is classified into components that is Part 1 and Part 2. Part 1 is included transistors of N1 and P1. Part2 is include inverters (N2, P2, N2, P3),
even as the inverters serve 3 purposes. First, the switching threshold of the inverter is trusted the component ratio of PMOS and NMOS (kP and kN). Part 2 employs the unique
ratio of the transistors to alternate the switching threshold of the inverter. Second, the part 2 CMOS inverters are connected in a high-quality feedback configuration,
therefore speeding up the switching process. Third, the control voltages of the CMOS inverter in part 2 controls the depth of the feedback signal, therefore the switching
threshold voltage of the Schmitt trigger.
   
    
 </p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155806677-7e1ff9d6-a06f-4281-9c05-052a0adf7555.jpg"></br>
  Fig.1: Schmitt Trigger
</p>

	   	Vdd = Supply voltage of the circuit
	   	GND = Ground
		
		
   The operation of the circuit may be defined as follows. Let's anticipate first of all that the input signal VIN is low. And the output signal VOUT is low too. So, transistors
of N1, N3 is withinside the reduce off areas and P1, P3 is withinside the saturation areas. To transfer the VIN from low to high, the transistor N1 activates regularly, the
voltage of node C decreases, at the same time as the VOUT regularly increases. when the same resistor of C node to ground decreases, flattening the voltage of node C further,
which improve the rate of the switch in the VOUT. Since the control voltage may be used to set the threshold voltage of P3, and hence the quantity of a further contemporary
source of P3, the switching threshold voltage from low to high (VLH) may be adjusted through the controlling voltage. when the input voltage is high, the output voltage is
likewise high. So, the transistors of P1, P3 is withinside reduce off the areas and N1, N3 is withinside the saturation areas. To switch the VIN from high to low, the transistor
of P1 activates regularly, the voltage of node C increases, even as the VOUT regularly decreases. When the voltage of node C is better than the switching voltage of the inverter
(P2 and N2), N3 turns off and P3 activates regularly. As the result, the identical resistor of the C node to VDD decreases, pulling up the voltage of node C further, which
improve the rate of the switch withinside the VOUT. Since the control voltage may be used to set the threshold voltage of N3, and therefore the quantity of an additional current
sink of N3, the switching threshold voltage from high to low (VHL) may be adjusted through the controlling voltage. The minimum VHL takes place when it reaches about VDD.

  Hence, in the end, we can conclude that this proposed Schmitt trigger is modified by using 6 transistors having less power consumption and also its area estimates are also
reduced as this whole simulation has been carried out in 28nm technology which is performed in Synopsys custom design tool. Therefore, the characteristic and operations of low
power Schmitt trigger isverified from the given simulation.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155806959-5a51ebc7-b601-40d1-b085-f810e9cb6fbb.jpg"></br>
  Fig.1: Refrence Waveform
</p>

# Tools Used:

## Synopsys Custom Compiler:
The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom
Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a
transistor level.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155798629-823e7866-48e3-4f3b-a955-8f02852f69e8.png"></br>
  Fig.3: Synopsys Custom Compiler
</p>
 
 </p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155846887-571cf34d-8d71-48fe-804e-8300112494e2.PNG"></br>
  Fig.1: Custom Compiler
</p>

<b>• Synopsys PrimeWave:</b></br>
&emsp;PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory
designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

<b>• Synopsys 28nm PDK:</b></br>
&emsp;The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Pre-Layout Schematics and Simulations:

## Schematics:
### Schmitt Trigger schematic:
This is the schematic of Schmitt Trigger in Synopsys custom compiler Tool which consist of 3 PMOS amd 3 NMOS in which after the PMOS and NMOS connections are complete I
connected the input labels that is vin and output labels Vout providng VDDA label for power supply and VSSA label for ground.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155856022-b04a6b1b-045f-4b12-94f1-bb90c790030f.png"></br>
  Fig.1: Schmitt Trigger cell schematic
</p>

### Symbol
This is the symbol of Schmitt Trigger as in this symbol the four circles which are shown indicates that there are input vin sine signal 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155856045-a7532a1f-84c7-4c6a-9323-705d3144356f.png"></br>
  Fig.1: cell Symbol(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155856281-6e5160ed-0ad5-4b14-b18b-6b31b524c55a.png"></br>
  Fig.1: cell Symbol(b)
</p>

### Testbench of cell Symbol:
This is the testbench of Four Quadrant Analog Multiplier in which its symbol is used and in which the other external connections are provided. Here, the Sinewave signal is used
for providing input to the multiplier and 3 Resistors are used named R1, R2 and R3 also Dc supply is given at 1.8v for providing power supply to the circuit and ground is
provided at VSSA.
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155808230-4e9c3687-2e32-4491-869c-7a786b563721.png"></br>
  Fig.1: cell Symbol(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155808359-29696b0e-9b4f-4144-b1df-5d0ab08e9439.png"></br>
  Fig.1: cell Symbol(b)
</p>


## Simulations:
### Synopsys Primewave:
For carrying simulation process in this tool Prime Wave is used. After creating and saving & check the schematic go to 'Tools' and open 'Primewave' to start the simulation.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155808359-29696b0e-9b4f-4144-b1df-5d0ab08e9439.png"></br>
  Fig.1: Primewave
</p>
In the Primewave select the 'model file' i.e the '28nm PDK's .lib file present in the HSPICE folder. Now you see that model file has been included, now the next step which we need to do now is to include the analysis 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155800668-ec14c672-31f7-4888-9d79-2fd74a7c1e27.png"></br>
  Fig.12: Model file
</p>
</p>

### Transient Analysis:
  Once that model file has been included, then after this select the 'tran' analysis in the analysis window and give the 'Start Time', 'Time Step' and 'Stop Time' parameters and
 save it. Then add the outputs which needs to be plotted by selecting the nets from the design.
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155800180-c6f8e2e6-10e9-41b1-b4c4-0980034b6ff4.png"></br>
  Fig.13: Analysis
</p>

Now, we need to save the testbench state for that Go to "Testbench" on the top left corner and then "click" on it then Go to "Save state", Press "OK" or hit "Enter".

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155801132-972f490a-b6c5-4279-a818-3c71af949878.png"></br>
  Fig.14: Save Testbench State
</p>

### Waveform:
For simulation and netlist Go to "Simulation" on the top left corner and then click on "Netlist and Run", the Respective Waveform has now been generated of Analog Multiplier
also at the same time netlist was generated automatically. To see the netlist click on "netlist" and then go to "Display", text viewer will open in which the generated netlist
has been displayed. Also, for the Log file go to simulation and then click on "Log File", the log file is displayed.


This is the output waveform of input v1 and v3.
</p>

### Schmitt Trigger:




### Schmitt Trigger:
The schematic of Schmitt Trigger has been created using the above cells and a few transistors as shown in the below figure.
<p align="center">
  
  Fig. 7: Four-Quadrant Analog Multiplier Schematic
</p>

## Simulations:
### Transient Analysis:
   After creating and saving the schematic go to 'Tools' and open 'Primewave' to start the simulation. In the Primewave select the 'model file' i.e the '28nm PDK's .lib file presentin the HSPICE folder. After this select the 'tran' analysis in the analysis window and give the 'Start', 'Stop', and 'Step Size' parameters and save it. Then add the outputs which needs to be plotted by selecting the nets on the schematic.</br>
One other thing we need to keep in mind is that here we have loop for which an initial condition needs to be declared. For that, we have to go to 'Setup -> Convergance aids' and select the net for which we want to set an initial condition.Then go to 'Simulations -> Netlist and Run' to generate a netlist and run the simulation to get the below output.
<p align="center">
  
  Fig. 8: Schmitt Trigger Transient Analysis
</p>

# Netlist of the Circuit:


# Observations:


# Author:
• E Balakrishna, B.Tech(ECE), Dronacharya Group of Institutions, Greater Nodia, Uttar Pradesh.

# Acknowledgements:

- [Synopsys India](https://www.synopsys.com/)
- [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Indian Institute Of Technology (IIT) Hyderabad](https://iith.ac.in/)
- [Kunal Ghosh](https://github.com/kunalg123), Founder, VSD Corp. Pvt. Ltd
- [VLSI System Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)

# References:


copy

</p>
<p align="center">
  <img src=""></br>
  Fig.1: Schmitt Trigger
</p>
