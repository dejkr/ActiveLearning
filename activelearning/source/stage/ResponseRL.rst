Transient Response of an RL Circuit
###################################

Objective
_________

The objective of this Lab activity is to study the transient response of inductor circuits using a series RL configuration and understand the time constant concept.

Notes
_____

As in all the ALM labs we use the following terminology when referring to the connections to the M1000 connector and configuring the hardware. The green shaded rectangles indicate connections to the M1000 analog I/O connector. The analog I/O channel pins are referred to as CA and CB. When configured to force voltage / measure current -V is added as in CA-V or when configured to force current  / measure voltage -I is added as in CA-I. When a channel is configured in the high impedance mode to only measure voltage -H is added as CA-H.

Scope traces are similarly referred to by channel and voltage / current. Such as CA-V , CB-V for the voltage waveforms and CA-I , CB-I for the current waveforms.

Background
__________

This lab activity is similar to the RC Lab activity 5, except that the capacitor is replaced by an inductor. In this experiment, you will apply a square waveform to the RL circuit to analyze the transient response of the circuit. The pulse width relative to the circuit's time constant determines how it is affected by the RL circuit. 

Time Constant (t): It is a measure of time required for certain changes in voltages and currents in RC and RL circuits. Generally, when the elapsed time exceeds five time constants (5t) after switching has occurred, the currents and voltages have reached their final value, which is also called steady-state response. 
 
The time constant of an RL circuit is the equivalent inductance divided by the Thévenin resistance as viewed from the terminals of the equivalent inductor. 

<m>t = L / R</m> (1) 

A Pulse is a voltage or current that changes from one level to another and back again. If a waveform's high time equals its low time, it is called a square wave. The length of each cycle of a pulse train is its period (T). The pulse width (tp) of an ideal square wave is equal to half the time period. 

The relation between pulse width and frequency for the square wave is given by: 
 
<m>f=1/(2t_p)</m> (2)

.. image:: alm-cir-lab6-fig1.png

<WRAP centeralign>Figure 1: Series RL circuit</WRAP>

In an R-L circuit, voltage across the inductor decreases with time while in the RC circuit the voltage across the capacitor increased with time. Thus, current in an RL circuit has the same form as voltage in an RC circuit: they both rise to their final value exponentially according to 1 - e<sup>$s$-$s$ t/t</sup>. 

The expression for the current in the Inductor is given by:

<m>I_L(t) = RV( 1 - e^-(R/L)t )  t >= 0</m> (3)

where, V is the applied source voltage to the circuit for t = 0. The response curve is increasing and is shown in figure 2. 

.. image:: alm-cir-lab6-fig2.png

<WRAP centeralign>Figure 2: Current in Inductor increasing in a Series RL circuit.</WRAP>

(Time axis normalized by t) 

The expression for the current decay across the Inductor is given by: 
 
<m>I_L(t) = I_0 e^-(R/L)t  t >= 0</m> (4)

where, 

I<sub>0</sub> is the initial current stored in the inductor at t = 0 

L/R = t is time constant. 
 
The response curve is a decaying exponential and is shown in figure 3. 

.. image:: alm-cir-lab6-fig3.png

<WRAP centeralign>Figure 3: Current decay through the Inductor for Series RL circuit.</WRAP>

Since it is possible to directly measure the current through the Inductor ( current supplied by driving source ) with the ALM1000, we will measure and compare both the current and the output voltage across the Resistor. The resistor waveform should be similar to the inductor current as V<sub>R</sub>=I*L<sub>R</sub>. From the waveforms on the scope, we should be able to measure the time constant t which should be equal to t = L / R<sub>total</sub>. 

Here, R<sub>total</sub> is the total resistance and can be calculated from R<sub>total</sub> = R inductance+ R. 
 
R inductance is the measured value of inductor resistance and can be measured by connecting inductance to an ohmmeter prior to running the experiment.

Materials
_________

RedPitaya
Multimeter
1 - Resistor 220 Ω
1 - Inductor 20 mH ( 2 10 mH in series )

Procedure
_________

1. Measure the combined inductor and resistor resistance R<sub>total</sub> by using an Ohmmeter. You can use the ALM1000 Ohmmeter Tool to do this. Remember that the Ohmmeter tool measures resistance with respect to ground when you connect the series connected L<sub>1</sub> and R<sub>1</sub>.

2. Set up the circuit shown in figure 4 on your solderless breadboard with the component values R<sub>1</sub> = 220 Ω and L<sub>1</sub> = 20mH. Open the Oscilloscope application

.. image:: alm-cir-lab6-fig4.png

<WRAP centeralign>Figure 4: Experiment Set-Up</WRAP>

3. Set the channel A AWG Min value to 0.5 and Max value to 4.5V to apply a 4Vp-p square wave centered on 2.5 V as the input voltage to the circuit. From the AWG A Mode drop down menu select the SVMI mode. From the AWG A Shape drop down menus select Square. From the AWG B Mode drop down menu select the Hi-Z mode.
 
Calculate the applied frequency using equation (2) for tp = 5t 

4. From the ALICE Curves drop down Menu select CA-V, CA-I and CB-V for display. From the Trigger drop down menu select CA-V and Auto Level. Adjust the time base until you have at approximately two cycles of the square wave on the display grid.

.. image:: alm-cir-lab6-screen1.png

<WRAP centeralign>Figure 5: Oscilloscope Configuration.</WRAP>

This configuration allows the oscilloscope to look at the input voltage of the circuit and the current through the inductor on channel A and the output voltage of the circuit on channel B. Make sure you have checked the Sync AWG selector.

5. The V<sub>R</sub> waveform has the same shape as I<sub>L</sub>(t) waveform. From V<sub>R</sub> waveform measure time constant t and compare with the one that you calculated from L/Rtotal.  (Hint: Find the time that corresponds to 0.63V<sub>R</sub> value). See Background section for details. 

6. Observe the response of the circuit and record the results again for tp = 25t, and tp = 0.5t. 

Questions
_________

• Include plots of I<sub>L</sub> and V<sub>R</sub> for different tp values given above in Procedure 4.
 
• A Capacitor stores charge. What do you think an Inductor stores? 
Answer in brief. 
