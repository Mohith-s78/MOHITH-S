# Experiment-3
## AIM :
To Design and analyze the mos amplifier circuit for the given specification 
### Theory 
#### Differential Amplifier
The differential-pair or differential-amplifier configuration is the most widely used building block in analog integrated-circuit design.
It consist of two transistors M1 and M2, whose sources are joined together.
If two transistor are connected to the different voltage input then there current across M1 and M2 are different due to gate voltage.If in case the voltage supply at gate terminal is same then the current through the M1 and M2 are same (Im1=Im2).This configuration is called "Common Mode input voltage differential Amplifier".WHatever may be the load resistor, the MOSFET M1 and M2 should not go to the Triode region. It should be verified that MOSFET should be in Saturation Region 
!image[https://github.com/Mohith-s78/MOHITH-S/blob/4329d33e100d371479d1140794f655a55945704d/418371927-bd20bd4e-aab5-4fa4-825d-394bbb6e2b30.png]
This Expereiment is Based on Common Mode Input voltage Differential Amplifier.

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
Finially by solving we get

Iss=P/VDD=2.2mW/1.8V=1mA
Id1=Id2=Iss/2=0.611mA
rd=(vdd-vocm)/id=1.14566kohm
rss=vp/iss=0.32787kohm
Using these  data we can design the circuit for the given power rating 
## 1)Circuit 1 (Common Source terminal is connected to resistor)
 In this circuit the Load Resistor is coonected to the Drain terminal of MOSFET.Source terminal is connected resistor and 
 another terminal is connected to ground this is called source degenration resistor.





The resistor applied at the common source terminal leads to change in the voltage gain ,input impedence in the circuit and 
the lineraity.So the linearity increases and the impedence.
As this is closed loop amplifier this leads to causes a feedbakback amplifier for all elements connecting to the common 
source terminal.
### DC analysis


### Transient Analysis:


Voltage Gain of this circuit is given by= Vout/Vin
Av=VO/VI=0.145/0.1=1.45
Higher The resistor value reduces gain but increases bandwidth and more the  transient response.

## AC Analysis


Gain =20*log(Av)

### 2)Circuit 2 (Common Source terminal is connected to current source)
Same  as the ciruit in the resistor circuit we need to replace resistor by current source
### DC Analysis

### Transient Analysis:

 Voltage gain= vout/vin

### AC Analysis



### 3)Circuit 3 (Connecting MOSFET to source terminal)


### DC Analysis


### Transient Anlysis:

### AC Analysis:


## INFERENCE:

In this experiment, we have seen the behaviour and working principles of a differential amplifier by using three different configurations thet is with resistor , current source , and an NMOS .
All the implements work on different ways that results into the cahnge in Voltage gain and stabillity of a mosfet.










