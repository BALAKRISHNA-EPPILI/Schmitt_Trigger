# Schmitt_Trigger
This repository presents the design of Analysis of CMOS Schmitt Trigger implemented using Synopsys Custom Compiler on 28nm Technology .


# Table of Contents

- [Abstract](#Abstract)
- [Introduction](#Introduction)
- [Schmitt Trigger](#Schmitt-Trigger)
- [Installation process](#Installation-process)
- [Tools Used](#Tools-Used)
	- [Synopsys Custom Compiler](#Synopsys-Custom-Compiler)
- [Pre-Layout Schematics and Simulations](#Pre-Layout-Schematics-and-Simulations)
	- [Schematics](#Schematics)
	- [Schmitt Trigger schematic](#Schmitt-Trigger-schematic)
	- [Symbol](#Symbol)
	- [Testbench of cell Symbol](#Testbench-of-cell-Symbol)
- [Simulations](#Simulations)
	- [Synopsys Primewave](#Synopsys-Primewave)
	- [Transient Analysis](#Transient-Analysis)
	- [Waveform](#Waveform)
- [Netlist of the Circuit](#Netlist-of-the-Circuit)
- [Log_File of the Circuit](#Log_File-of-the-Circuit)
- [References](#references)
- [Acknowledgement](#acknowledgement)
- [Author](#author)

# Abstract
   Schmitt Trigger circuit is extensively utilized in analog and digital circuit (ADC) to clear up the noise problem. Hysteresis is a common disadvantage of the Schmitt Triggers
that is decided through the tool dimensions, technique parameters and supply voltages. This situation gives a Schmitt Trigger circuit capability that it could perform at low
voltage. The proposed circuit is designed based on Conventional  Schmitt Trigger through manipulating the association of transistors’  width-period ratio.
   
   Therefore, we are going to do the analysis of Conventional Schmitt  Trigger in 28 nm technology. We are going to carry out the whole  simulation of the proposed design of
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
  Fig.1: Symbol of Schmitt Trigger
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
  Fig.2: Schmitt Trigger
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

# Installation process:
1. First we right click and create a New Folder, and we have created one folder (I give a folder named schmitt_trigger_by_balakrishna)
2. Then we go to that folder by double clicking & open terminal by right clicking. And Install PDK32nm/lib.defs.
3. Once install and then type this command

           tcsh
	   source /Applications/Synopsys/cshrc_syn_2021.09
           
4.Then You should get one welcome message if all the spellings are correct.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155874221-0ad28012-fc03-424a-89c8-d47db5d7f9b7.PNG"></br>
  Fig.3: Terminal
</p>

5.Now we are ready to open the Synopsys custom compiler and type command

           custom_compiler &
6.Then open your Custom compiler

# Tools Used:

## Synopsys Custom Compiler:
The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom
Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a
transistor level.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155798629-823e7866-48e3-4f3b-a955-8f02852f69e8.png"></br>
  Fig.4: Synopsys Custom Compiler
</p>
 
 </p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155846887-571cf34d-8d71-48fe-804e-8300112494e2.PNG"></br>
  Fig.5: Custom Compiler
</p>

<b>• Synopsys PrimeWave:</b></br>
&emsp;PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory
designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

<b>• Synopsys 28nm PDK:</b></br>
&emsp;The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Pre-Layout Schematics and Simulations:

## Schematics:

Now, I need to implement the circuit of Schmitt Trigger in Synopsys Custom Compiler Tool so, For implementing the circuit first there are some steps which one need to follow :

1) As synopsys tool open Go to "file" on left hand top corner click on it then there are several options come there click on "new" then click on library , it ask for the name so, give the name of the library which you want to create of the circuit . Now also include the library in that file for example in my circuit I included the library of 28nm PDK.

2) After performing the first step , now similarly I need to create the cell of the circuit for that go to the cell column 
Right Click on it then click on "NEW" then it ask for the name of the Cell , give it name according to your wish .

3) Similarly now for creating the schematic of our circuit we need to create a file of schematic in the view column .

For creating this file follow the step 2 as you make the cell .

Now, finally your schematic has been created and now you can implement your circuit .

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155872807-d106c4d3-743f-44a3-9467-fc0baf0bdaae.PNG"></br>
  Fig.6: Library manager
</p>


### Schmitt Trigger schematic:
This is the respective schematic of the Schmitt trigger in the Synopsys tool . It contains total of 6 MOSFETs  in which 3 are PMOS and 3 are NMOS . Also ,there are 4 labels that is  vin,Vout,VDDA and VSSA . Now in the next step we first made symbol of schematic and then create testbench of the symbol in which external supplies and elements are connected. The steps for proceeding further are given below.


</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155856022-b04a6b1b-045f-4b12-94f1-bb90c790030f.png"></br>
  Fig.7: Schmitt Trigger cell schematic
</p>

### Symbol
This is the symbol of Schmitt Trigger as in this symbol there are 2 signals  which are shown in which the upper signal or the curved signal is the sine wave signal which is the
input of schmitt trigger and the other square wave signal which indicates the output of schmitt Trigger . So, The whole symbol indicates that schmitt trigger converts the sine
wave into the square wave . 

This symbol consist of 4 pins . 

These pins are :

vin, VDDA,Vout and VSSA 

vin=Pin for Input signal 

VDDA=Power supply voltage 

Vout=Pin for output signal 

VSSA= Pin for Ground

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155876891-f7b09163-20b0-44c1-8af1-48a35c580c82.PNG"></br>
  Fig.8: cell Symbol(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155876906-80f9f21c-682f-4833-b0e3-45122cb708e5.PNG"></br>
  Fig.9: cell Symbol(b)
</p>

### Testbench of cell Symbol:

This is the testbench of the Schmitt trigger circuit in which a sine wave signal has been given on "vin" pin and a resistor is connected at the "Vout" pin for taking the output.
And At VDDA we have given the a dc power supply voltage which give power to the circuit to start working also at VSSA terminal pin a ground is connected.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155876950-9ecf0bc8-3073-4302-aea1-0aa3924dd64e.PNG"></br>
  Fig.10: cell Symbol(a)
</p>


## Simulations:
### Synopsys Primewave:
For carrying simulation process in this tool Prime Wave is used. After creating and saving & check the schematic go to 'Tools' and open 'Primewave' to start the simulation.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155877001-fff41d13-52c3-4dfe-b104-797acc6fbe5b.png"></br>
  Fig.11: Primewave(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155877032-e861bb40-0f64-4451-a8d5-4d58b5956edc.PNG"></br>
  Fig.12: Primewave(b)
</p>


In the Primewave select the 'model file' i.e the '28nm PDK's .lib file present in the HSPICE folder. Now you see that model file has been included, now the next step which we need to do now is to include the analysis 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155856509-0aeb741d-c86e-4554-be2e-549903f20b28.PNG"></br>
  Fig.13: Model file(a)
</p>
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155856560-96004639-fecd-4f55-b6f0-1b5258628aa4.PNG"></br>
  Fig.14: Model file(b)
</p>
</p

### Transient Analysis: 

Once that model file has been included, then after this select the 'tran' analysis in the analysis window and give the 'Start Time', 'Time Step' and 'Stop Time' parameters
respectively and save it. Then add the outputs on the right bottom corner in the expression column which need to be plotted by selecting the nets from the design of testbench of
the circuit .
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155876835-67096a15-2c07-4709-aeb5-467bc68b6619.PNG"></br>
  Fig.15: Analysis
</p>

Now for the simulation purpose we need to first save the state of the testbench after selecting the respected plotted variable. So, for that Go to Tectbench on top then click on
it , Go to "save state" then click on it . All the things have been written by default we just need to click "OK"

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155876848-0b46cc62-8a64-436d-834c-c212550fd8b1.PNG"></br>
  Fig.16: Save Testbench State
</p>

### Waveform:
Now, for simulating the circuit go to the simulation on the top bar click on it then there are several options come there one option is "Netlist and Run" and the other is "Run"
only but since we need our netlist also so, click on "Netlist and Run" then it loads and on transient analysis, it is showing the status of simulation like 
Simulation:Ready-----> then , Running -----> then Completed 

 Your waveform of the circuit automatically opens and your waveform is displayed finally in front of you. 
Also,  at the same time netlist is also generated so, go back to the Test Suite window and go back to the simulation button and click on "Netlist" there, click on "Display" now
the netlist of your circuit  has been displayed. 

  Also, the same procedure is followed for displaying of log file just go to simulation and click on log display then your log file has been displayed in front of you.
  
  
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155857677-558befde-d38a-4aaa-bb4b-a3d980290cfc.png"></br>
  Fig.17: Waveform(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155857688-a8b4c121-23ac-4273-9cc8-b1fe879d379a.png"></br>
  Fig.18: Waveform(b)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155857692-26faf92c-f090-4a90-8248-155b705de648.png"></br>
  Fig.19: Waveform(c)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/88899069/155857694-90c7d0ae-416f-49ee-ba66-133ba4f4b81d.png"></br>
  Fig.20: Waveform(d)
</p>

## CONCLUSION: 

The design of a CMOS Schmitt trigger may be finished if the unique circuit operation close to the transition factors is analyzed.
This evaluation offers real thresholds and lets in one to assess the distinction among the thresholds and the preliminary factors of transitions (which might be incorrectly
taken into consideration and targeted as thresholds). 
The voltage-modern-day traits of the trigger sub circuits permit one to specify the situations to make the trigger switch function more rectangular. The evaluation is legitimate
if the fabrication generation lets in the usage of the square-regulation traits of MOS devices.

# Netlist of the Circuit:

Refer to the netlist of the circuit here: <a href='Netlist'>Netlist</a>

# Log_File of the Circuit:

Refer to the log_file of the circuit here: <a href='Log_File'>Log_File</a>

# References:
[1]. https://iiste.org/Journals/index.php/ISDE/article/view/1106/1027- 

[2]. https://www.researchgate.net/profile/Konjeti-Pavan-Kumar/publication/334192413_Design_and_Analysis_of_CMOS_Schmitt_Trigger/links/6005123145851553a0508496/Design-and-Analysis-of-CMOS-Schmitt-Trigger.pdf 

[3]. https://tarjomefa.com/wp-content/uploads/2018/04/8976-English-TarjomeFa.pdf

# Acknowledgements:

- [Synopsys India](https://www.synopsys.com/)
- [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Indian Institute Of Technology (IIT) Hyderabad](https://iith.ac.in/)
- [Kunal Ghosh](https://github.com/kunalg123), Founder, VSD Corp. Pvt. Ltd
- [VLSI System Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)
- [SUMANTO KAR](https://github.com/Eyantra698Sumanto)
- [Sameer S Durgoji](https://github.com/vsdip/avsddac_3v3_sky130_v2)

# Author:
• E BALAKRISHNA, B.Tech(ECE), Dronacharya Group of Institutions, Greater Nodia, Uttar Pradesh.
