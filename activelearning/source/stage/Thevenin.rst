Thévenin Equivalent Circuit and Maximum Power Transfer
######################################################

Objective
_________

The objective of this Lab activity is to verify Thévenin's theorem by obtaining the Thévenin equivalent voltage (V<sub>TH</sub>) and Thévenin equivalent resistance (R<sub>TH</sub>) for the given circuit. Verify the Maximum  Power Transfer Theorem. 

Notes
_____

As in all the ALM labs we use the following terminology when referring to the connections to the M1000 connector and configuring the hardware. The green shaded rectangles indicate connections to the M1000 analog I/O connector. The analog I/O channel pins are referred to as CA and CB. When configured to force voltage / measure current -V is added as in CA-V or when configured to force current / measure voltage -I is added as in CA-I. When a channel is configured in the high impedance mode to only measure voltage -H is added as CA-H.

Scope traces are similarly referred to by channel and voltage / current. Such as CA-V , CB-V for the voltage waveforms and CA-I , CB-I for the current waveforms.

Background
__________

Thévenin's Theorem is a process by which a complex circuit is reduced to an equivalent circuit consisting of a single voltage source (V<sub>TH</sub>) in series with a single resistance (R<sub>TH</sub>) and a load resistance (R<sub>L</sub>). After creating the Thévenin Equivalent Circuit, the load voltage V<sub>L</sub> or the load current I<sub>L</sub> may be easily determined. 

One of the principal uses of Thévenin's theorem is to replace a large portion of a circuit, often a more complicated and uninteresting part, by a simple equivalent. The new simpler circuit enables rapid calculations of the voltage, current, and power which the more complicated original circuit is able to deliver to a load. It also helps to choose the optimal value of the load (resistance) for maximum power transfer. 

.. image:: alm-cir-lab4-fig1.png

<WRAP centeralign>Figure 1.</WRAP>

.. image:: alm-cir-lab4-fig1.png

<WRAP centeralign>Figure 2: Thévenin Equivalent Circuit of Figure 1</WRAP>

2. The Maximum Power Transfer Theorem states that an independent voltage source in series with a resistance R<sub>S</sub> or an independent current source in parallel with a resistance R<sub>S</sub>, delivers a maximum power to the load resistance R<sub>L</sub> when R<sub>L</sub> = R<sub>S</sub>. 

In terms of a Thévenin Equivalent Circuit, maximum power is delivered to the load resistance R<sub>L</sub> when R<sub>L</sub> is equal to the Thévenin equivalent resistance R<sub>TH</sub> of the circuit.

.. image:: alm-cir-lab4-fi31.png

<WRAP centeralign>Figure 3: Maximum Power Transfer</WRAP>
 
Materials
_________

RedPitaya
Multimeter
Various Resistors (100 Ω, 330 Ω, 470 Ω, 1 KΩ and 1.5 KΩ)

Procedure
_________

1. Verifying the Thévenin's theorem:\\ 
a) Construct the circuit of figure 1 using the following component values: 

 R<sub>1</sub> = 330 Ω\\
 R<sub>2</sub> = 470 Ω\\
 R<sub>3</sub> = 470 Ω\\
 R<sub>4</sub> = 330 Ω\\
 R<sub>5</sub> = 1 KΩ\\
 R<sub>L</sub> = 1.5 KΩ\\
 V<sub>S</sub> = +5V

b) Accurately measure the voltage V<sub>L</sub> across the load resistance using ALM1000 Volt Meter Tool. Use the Volt Meter Tool by connecting channel CA to the + node of V<sub>L</sub> and connect channel CB to the - node. V<sub>L</sub> will be the difference between CA volts and CB volts. This value will later be compared to the one you will find using Thevenin Equivalent. 

c) Find V<sub>TH</sub>: Remove the load resistance R<sub>L</sub> and measure the open circuit voltage V<sub>OC</sub> across the terminals. Use the Volt Meter Tool by connecting channel CA to the + node of V<sub>OC</sub> and connect channel CB to the - node. V<sub>OC</sub> will be the difference between CA volts and CB volts. This is equal to V<sub>TH</sub>. See figure 4.

.. image:: alm-cir-lab4-fig4.png

<WRAP centeralign>Figure 4: Measuring the Thevenin Voltage</WRAP>

d) Find R<sub>TH</sub>: Remove the source voltage V<sub>S</sub> and construct the circuit as shown in figure 5. Use multimeter in Ohmmeter mode to measure the resistance looking into the opening where R<sub>L</sub> was. This gives R<sub>TH</sub>. Make sure there is no power applied to the circuit before measuring with the Ohmmeter and the ground connection has been moved as shown. 

.. image:: alm-cir-lab4-fig5.png

<WRAP centeralign>Figure 5: Measuring the Thevenin Resistance R<sub>TH</sub>.</WRAP>

e) Obtaining V<sub>TH</sub> and R<sub>TH</sub>, construct the circuit of figure 2. Create the value of R<sub>TH</sub> using a series and or parallel combination of resistors from your parts kit. Using the Meter - Source Tool connect channel CA for the V<sub>TH</sub> source and set the value to what you measured for VTH in step c). 

.. image:: alm-cir-lab4-fig6.png

<WRAP centeralign>Figure 6: Thevenin Equivalent Construction</WRAP>

f) With R<sub>L</sub> set to the 1.5 KΩ used in step b) measure the V<sub>L</sub> for the equivalent circuit and compare it to the V<sub>L</sub> obtained in step b). This verifies the Thévenin theorem. 

g) Optional: Repeat steps 1 b) to 1 f) for R<sub>L</sub> = 2.2 KΩ

2. Verifying the Maximum Power Transfer theorem: 

a) Construct the circuit as in figure 7 using the following values: 

V<sub>S</sub> = +5 V\\
R<sub>1</sub> = R<sub>2</sub> = 470 Ω\\
R<sub>3</sub> = 1 KΩ\\
R<sub>L</sub> = combinations of 1 KΩ and 100 Ω resistors ( figure 8 )

.. image:: alm-cir-lab4-fig8.png

<WRAP centeralign>Figure 7: Circuit for Maximum Power Theorem</WRAP>

b) Use the Volt Meter Tool by connecting channel CA to the + node of V<sub>L</sub> and connect channel CB to the - node across R<sub>L</sub>. V<sub>L</sub> will be the difference between CA volts and CB volts.
 
c) To find the value of R<sub>L</sub> for which maximum power is transferred, vary the load resistances by constructing series / parallel combinations of 1 KΩ and 100 Ω for R<sub>L</sub> between 500 Ω to 1400 Ω in 100 Ω steps as shown in figure 8. For each value of R<sub>L</sub> write down V<sub>L</sub>.

.. image:: alm-cir-lab4-fig7.png

<WRAP centeralign>Figure 8. R<sub>L</sub> configurations</WRAP>
 
d) Calculate the power for each load resistor value using P<sub>L</sub>=V<sub>L</sub><sup>2</sup>/R<sub>L</sub>. Then, interpolate between your measurements to calculate the load resistor value corresponding to the maximum power (P<sub>L</sub>-max). This value should be equal to R<sub>TH</sub> of circuit in figure 7 with respect to load terminals. 

Questions
_________

1. Calculate the percentage error difference between the load voltages obtained for circuits of figure 1 and figure 2. 

2. Using Voltage Division for circuit of figure 2, calculate V<sub>L</sub>. Compare it to the measured values. Explain any differences. 

3. Calculate the maximum power transmitted to the load R<sub>L</sub> obtained for the circuit of figure 3. 


