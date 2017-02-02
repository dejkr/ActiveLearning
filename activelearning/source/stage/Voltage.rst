Voltage and Current Division
############################

Objective
_________

The objective of this Lab activity is to verify the voltage and current division properties of resistor networks. 

Notes
_____

As in all the ALM labs we use the following terminology when referring to the connections to the ALM1000 connector and configuring the hardware. The green shaded rectangles indicate connections to the M1000 analog I/O connector. The analog I/O channel pins are referred to as CA and CB. When configured to force voltage / measure current -V is added as in CA-V or when configured to force current  / measure voltage -I is added as in CA-I. When a channel is configured in the high impedance mode to only measure voltage -H is added as CA-H.

Scope traces are similarly referred to by channel and voltage / current. Such as CA-V , CB-V for the voltage waveforms and CA-I , CB-I for the current waveforms.

Background
__________

Voltage and Current division allow us to simplify the task of analyzing a circuit. Voltage Division allows us to calculate what fraction of the total voltage across a series string of resistors is dropped across any one resistor. For the circuit of figure 1, the Voltage Division formulas are: 

<m>V_1 =  V_S R_1/(R_1 + R_2)</m> (1) 

<m>V_2 = V_S R_2/(R_1 + R_2)</m> (2) 

.. image:: alm-cir-lab2-fig1.png

<WRAP centeralign>Figure 1. Voltage division</WRAP>

Current Division allows us to calculate what fraction of the total current into a parallel string of resistors flows through any one of the resistors. 

.. image:: alm-cir-lab2-fig2.png

<WRAP centeralign>Figure 2, Current division</WRAP>

For the circuit of figure 2, the Current Division formulas are: 

<m>I_1 = I_S R_2/(R_1 + R_2)</m> (3) 

<m>I_2 = I_S R_1/(R_1 + R_2)</m> (4) 

Materials
_________

RedPitaya
Various Resistors 470 Ω, 1 KΩ, 4.7 KΩ. and 1.5 KΩ

Procedure
_________

1. Verifying the voltage division:
 
a) Construct the circuit as shown in figure 1. Set R<sub>1</sub>= 4.7 KΩ, R<sub>2</sub>= 1.5 KΩ and use the fixed power supply 5V as voltage source Vs. Use the Volt Meter Tool to measure the voltages V<sub>1</sub> and V<sub>2</sub>

Repeat this step for R<sub>1</sub> = R<sub>2</sub> = 4.7 KΩ. and write down the measurements. 

b) Calculate the voltages V<sub>1</sub> and V<sub>2</sub> by using the formulas (1) and (2) in each case.
 
c) Compare the results from steps 1a and 1b. 

2. Verifying the current division: 

a) Construct the circuit as shown in figure 2. Set  R<sub>1</sub>= 470 Ω, R<sub>2</sub>= 1 KΩ. and Rs=470 Ω. Use the Meter Source tool to measure the currents Is, I<sub>1</sub> and I<sub>2</sub> Connect the Channel A generator output as voltage source Vs. Set CHA to source a DC voltage of +5V ( SVMI mode ). Use Channel B as an ammeter to alternately measure I<sub>1</sub> and I<sub>2</sub> by connecting the lower end of R<sub>1</sub> and R<sub>2</sub> to CHB with CHB set to 0 V ( SVMI mode ).

.. image:: alm-cir-lab2-fig4.png

<WRAP centeralign>Figure 3, Measuring I<sub>1</sub> and I<sub>2</sub></WRAP>

Repeat this step by using R<sub>1</sub>=R<sub>2</sub> = 470 Ω. and write down the measurements. 

b) Calculate the currents I<sub>1</sub> and I<sub>2</sub> by using the formulas (3) and (4). 

c) Compare the results from steps 2a and 2b. 

Questions
_________

1. How well did the measured outputs and calculated outputs compare? Explain any difference.
 
2. Can you apply current division to obtain I<sub>1</sub> and I<sub>2</sub> for the circuit shown in figure 4? Explain briefly. 

.. image:: alm-cir-lab2-fig3.png
