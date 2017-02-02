Impedance Measurement - Frequency Effects
#########################################

Objective
_________

The objective of this Lab activity is to:\\
1. Measure component impedance and circuit impedance using the ALICE-VVM Impedance Analyzer software.\\
2. Study the magnitude and phase changes with change in frequency for an RLC  circuit. 

Notes
_____

As in all the ALM labs we use the following terminology when referring to the connections to the M1000 connector and configuring the hardware. The green shaded rectangles indicate connections to the M1000 analog I/O connector. The analog I/O channel pins are referred to as CA and CB. When configured to force voltage / measure current -V is added as in CA-V or when configured to force current  / measure voltage -I is added as in CA-I. When a channel is configured in the high impedance mode to only measure voltage -H is added as CA-H.

Scope traces are similarly referred to by channel and voltage / current. Such as CA-V , CB-V for the voltage waveforms and CA-I , CB-I for the current waveforms.

Background
__________

Impedance is the resistance to the flow of alternating current. It is the total opposition that  a circuit offers to the flow of current at a particular frequency. Impedance (Z) is expressed as a combination of Resistance (R) and Reactance (X) and is measured in ohms (?). It can be expressed as a complex quantity as: 

<m>Z=R+jX</m> 

The impedance is represented on a 2-D polar plot which has x as real axis and y as Imaginary axis. The resistive component is a line along the real axis and the reactive component is a line along the imaginary axis. 

For a resistor, the impedance is the same as the DC resistance and is a line along the x - axis. For a capacitor, the impedance (or more specifically, the reactance) X<sub>C</sub> is imaginary and is represented as a line along the negative y-axis of the 2-D polar plot. The reactance of the capacitor depends upon the frequency and is given as:

<m>X_C = 1/(omega C)</m>

For an inductor, the impedance (or more specifically, the reactance) XL is imaginary and can be represented as a line along the positive y-axis of the 2-D plot. The reactance of the inductor also depends upon the frequency and is given as: 

<m>X_L = omega L</m>

The impedance of a series RLC circuit is the sum of the impedances of respective components. 

<m>Z= R + Z_L + Z_C</m>

( or ) 

<m>Z= R + j X_L - j X_C</m>

This can also be represented as a phasor vector on a polar plot with: 

<m>Magnitude = sqrt{(R^2 + (X_L - X_C)^2)}</m>

<m>Phase  = Tan^-1((X_L - X_C) / R )</m>

.. image::  alm-cir-lab10-fig1.png

<WRAP centeralign>Figure 1: Impedance Measurement of Series RLC circuit.</WRAP>

.. image::  alm-cir-lab10-screen1.png

<WRAP centeralign>Figure 2: Impedance Analyzer - studying the series RLC circuit.</WRAP>

Materials
_________

RedPitaya\\
Resistors (1.0 KΩ, 470 Ω)\\
Capacitor (1.0 µF)\\
Inductor (20 mH) 

Procedure
_________

A. Measurement of Component Impedance: 

1. With a resistor R<sub>EXT</sub> = 1 KΩ connected between CA-V and CB-V, connect a 470 Ω resistor as R<sub>S</sub>between CB-V and the fixed 2.5 V supply. 

2. Run the ALICE-VVM software tool. 

3. Note down the magnitude, phase, resistance and reactance for the resistor in the table shown in figure 3. Note that the default frequency is set to 1000 Hz. Verify that the phasor is along the real axis and the phase is zero. Also the magnitude should be the same as resistance since the reactance is zero. 

4. Replace R<sub>S</sub> with C<sub>S</sub> = 1.0 uF, Similarly note down the magnitude, phase, resistance and reactance values. For the capacitor, the phasor should be along the negative imaginary axis and the phase should be 270 or -90 degrees. 

5. Replace C<sub>S</sub> with L<sub>S</sub> = 20 mH, Similarly note down the magnitude, phase, resistance and reactance values. For the inductor, the phasor should be along the positive imaginary axis and the phase should be 90 degrees. 

B. Measurement of Circuit Impedance and Effects of Frequency on RLC circuit: 

1. Setup the series RLC circuit shown in Figure 1 with the given component values. R<sub>EXT</sub> = 1 K?, R<sub>s</sub> = 470 Ω, C<sub>S</sub> = 1.0 uF and L<sub>S</sub> = 20 mH.

2. Note down the magnitude, phase, reactance and resistances for the RLC circuit at the default frequency of 1000 Hz. Record the values in table shown in figure 3. 

3. Adjust the frequency till the phase becomes zero and note down this frequency. This is a special frequency where the total reactance is zero and the circuit is purely resistive. 

<m>Z= R + j (X_L - X_C)</m> 

If <m>X_L - X_C = 0</m>(1) 

Then <m>Z=R</m>

Thus, the impedance of the RLC circuit is now just the resistance. The frequency at which this occurs is called resonant frequency. It can be mathematically derived using equation (1) to be: 

<m>f_o = 1/(2pi sqrt{LC})</m>(2) 

4. Vary the frequency below f<sub>o</sub> in steps of 100 Hz and take up to three measurement readings from the impedance analyzer. Record the readings in a table as shown in figure 4 ( add more rows to table as necessary). Repeat the same by varying the frequency above f<sub>o</sub> in steps of 100 Hz. Observe carefully, the rotation of the magnitude phasor (orange line ). 

Questions
_________

1. Compute the resonant frequency f<sub>o</sub> for the series RLC using equation (2) and compare it to the measured value. What is the percentage error between the two? 

2. Give your conclusions from the observations made in step (4) of the procedure. 

3. Compute the magnitude and phase for the series RLC circuit, when the reactive component equals the resistive component.
 
Measurements
____________

^Frequency =^
|Component|Magnitude (Ω)|Phase (degrees)|Resistance (Ω)|Reactance (Ω)|
|Resistor|  |  |  |  |
|Capacitor|  |  |  |  |
|Inductor|  |  |  |  |
|RLC Circuit|  |  |  |  |

Figure 3: Measurement of Component and Circuit Impedance

^Frequency (Hz)^Magnitude (Ω)^Phase (degrees)^Resistance (Ω)^Reactance (Ω)^
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

Figure 4: Effects of frequency on RLC circuit.
