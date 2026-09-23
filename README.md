# 2.-Design-implement-and-simulatioin-of-Integrator-and-Differentiator
**AIM:**
To design , implement and simulate  an integrator and differentiator circuits

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range	Quantity
1.	Signal Generator	3 MHz	1
2.	DSO	30 MHz	1
3.	Dual RPS	(0 – 30) V	1
4.	Op-Amp	µA741	1
5.	Bread Board		1
6.	Resistors	1K,10K,100K,	2
7.	Capacitors	0.1µF,0.01µF	1
8.	Connecting wires and probes	As required	
9.  LT SPICE software

**THEORY:**

**INTEGRATOR**
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf

The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.

**DESIGN:**
 <img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/dc17cb19-2dcd-4c5a-baab-4948409c83fe" />

To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	

**DIFFEERENTIATOR:**

The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.

The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
 
**DESIGN (DIFFERENTIATOR):**
<img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/22e2089b-42c9-4651-91c2-f2a859e5a433" />

Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


**PROCEDURE:**
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

 
**INTEGRATOR:**
  **CIRCUIT DIAGRAM**
<img width="1599" height="1200" alt="image" src="https://github.com/user-attachments/assets/f9f57de0-1b15-4a63-8271-3a756dda90ed" />


  **MODEL GRAPH:**

<img width="1599" height="1200" alt="image" src="https://github.com/user-attachments/assets/70062222-047a-4b08-b8d9-30139ac27066" />
<img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/c601ad07-902c-4a19-80b2-afde1732eda6" />

  **TABULATION:**
 <img width="1599" height="1200" alt="image" src="https://github.com/user-attachments/assets/51305228-29ca-4177-8b17-84944003f5c8" />


**MODEL CALCULATION:**

**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**
<img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/5c1d4eba-eda3-42f5-9844-2375a48d687d" />


  **MODEL GRAPH:**
<img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/97ef8a8f-881d-45ce-8619-248b46d24396" />

<img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/16c7cba7-afa1-4589-bbad-f48dfa590566" />

  **TABULATION:**
<img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/12c9cc9f-e900-4b6d-a097-ebc6f13a963a" />

 

**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  <img width="1200" height="1599" alt="image" src="https://github.com/user-attachments/assets/994f5a09-b9cb-4601-bae4-15962317a6e0" />

<img width="1599" height="1200" alt="image" src="https://github.com/user-attachments/assets/838ec4c3-dbaf-4f6a-bf42-f054dd5e2015" />

**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
