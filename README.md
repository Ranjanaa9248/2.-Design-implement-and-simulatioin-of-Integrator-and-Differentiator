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
<img width="673" height="342" alt="image" src="https://github.com/user-attachments/assets/83dd1372-31fa-41ea-8682-3439d6322501" />


  **MODEL GRAPH:**
<img width="587" height="360" alt="image" src="https://github.com/user-attachments/assets/a3629093-aff0-4ac1-8660-94323a28164c" />
<img width="762" height="472" alt="image" src="https://github.com/user-attachments/assets/e8a38213-b233-4548-8ded-1840469735b1" />


  **TABULATION:**
 
<img width="1600" height="560" alt="image" src="https://github.com/user-attachments/assets/14561348-f400-4c30-8ef1-68a5bf8dd8e6" />

  **GRAPH:**
<img width="1600" height="700" alt="image" src="https://github.com/user-attachments/assets/1a2de2c7-2cba-44cd-97ad-5a6b711d1330" />


**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**
<img width="636" height="367" alt="image" src="https://github.com/user-attachments/assets/4bb8bd2e-7211-41e9-8559-dfa393873abd" />



  **MODEL GRAPH:**

<img width="451" height="552" alt="image" src="https://github.com/user-attachments/assets/0dee0e4d-42f1-4d0d-9a9f-b574bd4075e9" />
<img width="451" height="552" alt="image" src="https://github.com/user-attachments/assets/5224149f-c410-4ae9-8ff5-86875d590561" />

  **TABULATION:**
<img width="975" height="1600" alt="image" src="https://github.com/user-attachments/assets/d38df19b-d17f-44f8-8dc7-47d8e569d2ed" />


   **GRAPH:**
<img width="1253" height="1599" alt="image" src="https://github.com/user-attachments/assets/4f3c5ce7-738a-4542-bdb4-ac5d5792e479" />

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

  **INTEGRATOR SINE WAVE:**

  <img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/0232eb88-44df-4f25-8c6f-da19836601b1" />

  **SQUARE WAVE:**

<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/70f03ad8-0786-465b-b756-25610b7a1c91" />

**DIFFERENTIATOR SINE WAVE:**

<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/b47a5528-a73b-456e-bdcc-8cf95e3be6d5" />
 **SQUARE WAVE:**
 <img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/3686f14d-2827-4861-a750-dbd1e3f6bef4" />

**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
