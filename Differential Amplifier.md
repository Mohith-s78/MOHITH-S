# Experiment-3
## AIM :
To Design and analyze the MOS Differential amplifier circuit for the given specification 
Vdd=1.8v , P<=2.2mW , Vicm=0.95v , Vocm=1.1v,Vp=0.4v
## Components  Required
N channel MOSFET(nmos4),Resistors-1.145kohm(2) ,327.8kohm, Power supply , Connecting wires.
### Theory 
#### Differential Amplifier
A differential amplifier is an electronic circuit that amplifies the difference between two input voltages while rejecting any common signals. It is a fundamental part of many analog circuits, particularly operational amplifiers and instrumentation amplifiers.

![418371927-bd20bd4e-aab5-4fa4-825d-394bbb6e2b30](https://github.com/user-attachments/assets/ad572fd3-c9f0-41f9-aba5-d2134b910c2b)

This Expereiment is Based on Common Mode Input voltage Differential Amplifier.that is  the difference between two input signals (V₁ and V₂) while rejecting common signals (noise).

This Experiement is conducted in 3 stages.Where common source terminal is connected with
1.Resistor
2.Current source
3.MOSFET

For all this circuit we need find out the AC analysis ,Transient analysis And Frequency Response.
The given specification of the circuit is 
P=2.2mW
vdd=1.8v
vicm=0.95v
vocm=1.1v
vp=0.4v
Finally by solving we get

Iss=P/VDD=2.2mW/1.8V=1mA
Id1=Id2=Iss/2=0.611mA
rd=(vdd-vocm)/id=1.14566kohm
rss=vp/iss=0.32787kohm
Using these  data we can design the circuit for the given power rating 
## 1)Circuit 1 (Common Source terminal is connected to resistor)
 In this circuit the Load Resistor is coonected to the Drain terminal of MOSFET.Source terminal is connected resistor and 
 another terminal is connected to ground this is called source degenration resistor.
<img width="758" alt="CIR_RESISTOR" src="https://github.com/user-attachments/assets/c8a50c53-a763-4cc8-aeaf-703d6f834b7b" />

### DC analysis
<img width="959" alt="dc" src="https://github.com/user-attachments/assets/2fc4281b-b9e5-4a21-9f1a-a993ad5f5157" />
Operating point of NMOSFETS = (1.1 V, 0.611mA)


### Transient Analysis:

<img width="955" alt="trancient" src="https://github.com/user-attachments/assets/0372f31a-c5ed-43f6-9469-e181adf5e219" />

Voltage Gain of this circuit is given by= Vout/Vin
Av=VO/VI=0.145/0.1=1.45

Higher The resistor value reduces gain but increases bandwidth and more the  transient response.

## AC Analysis

<img width="956" alt="ac" src="https://github.com/user-attachments/assets/797de86f-f8c0-4ade-b66b-4481fc94ba7a" />


Av=1.203 
Gain =20*log(Av)
  =20 log(1.203)
    =1.605

### 2)Circuit 2 (Common Source terminal is connected to current source)

Same  as the ciruit in the resistor circuit we need to replace resistor by current source

<img width="706" alt="image" src="https://github.com/user-attachments/assets/b33e5ab7-68c4-4ef6-af0e-bc95e50b56c3" />

### DC Analysis
<img width="956" alt="dc_cs" src="https://github.com/user-attachments/assets/34f9fe42-306b-42fd-ade6-5687c2ff94c6" />


Operating point of NMOSFETS = (1.1 V, 0.611mA)

### Transient Analysis:
<img width="960" alt="image" src="https://github.com/user-attachments/assets/afee2c0d-89d5-41a6-8505-281c364db5c5" />

 Voltage gain= vout/vin=884.7/112=7.899
Gain in dB=20*log(7.899)=17.95

### AC Analysis
<img width="957" alt="image" src="https://github.com/user-attachments/assets/89cb009a-18f1-4bb7-aa78-65b41f9be4e4" />

Av=2.877

Gain=20log(Av)=9.178

### 3)Circuit 3 (Connecting MOSFET to source terminal)
<img width="728" alt="image" src="https://github.com/user-attachments/assets/dbaea011-b483-4284-bc3d-ad1f0862b696" />



### DC Analysis
<img width="948" alt="image" src="https://github.com/user-attachments/assets/4adecadc-377b-4870-b55b-d49f905708d7" />

operating point (1.10005,0.00061098)


### Transient Anlysis:
<img width="956" alt="image" src="https://github.com/user-attachments/assets/c9c9ebcc-9a57-4311-881d-dea9d4979ef8" />

Voltage gain= vout/vin=888.2/112.3=7.909
Gain in dB=20*log(7.909)=17.962


### AC Analysis:
<img width="960" alt="image" src="https://github.com/user-attachments/assets/a3a248ea-bdc2-4670-b8f0-25a3733b0184" />

gain =3.445
gain in db = 20log(3.445)=10.743

## INFERENCE:

In this experiment, we have seen the behaviour and working principles of a differential amplifier by using three different configurations thet is with resistor , current source , and an NMOS .
All the implements work on different ways that results into the cahnge in Voltage gain and stabillity of a mosfet.
DC Analysis: All three circuits have nearly identical operating points (around 1.1V, 0.611mA), indicating that the NMOSFETs are biased similarly, ensuring they operate in the saturation region for amplification.
Transient Analysis :Circuit 1 has the lowest gain, which means it cannot effectively provide amplification. Circuit 2 has moderate gain, but the huge difference between AC values and transient indicates very strong frequency-dependent... Circuit 3 has the highest gain; hence, it is the best amplifier of the three.
AC analysis: The first circuit is found to have the lowest gain, confirming it to be a poor amplifier. A large reduction in gain, compared with the transient analysis, is seen in circuit two. this indicates frequency-dependent losses. Circuit three exhibits a consistently higher gain, attributable to a suitable design that involves minimal frequency-dependent degradation.
As the drain resistance increases, the gain generally increases because a higher drain resistance allows more voltage to develop across it for a given current, leading to a stronger output signal








