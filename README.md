# Linear Integrated Circuits (LIC)

# Experiment-1
## Aim 
To obtain the DC analysis ,AC analysis , Trancient analysis of a Common Source(CS)amplifier and also obtain gain and other parameters using LT Spice.

## Theory
A MOSFET is a type of transistor used for amplifying or switching electronic signals. It is widely used in digital and analog circuits due to its high efficiency and fast switching speed.

In saturation mode, an NMOS transistor operates under the conditions:
- *Vgs > Vth* (Gate-to-Source Voltage greater than Threshold Voltage)
- *Vds ≥ Vov* (Drain-to-Source Voltage greater than Overdrive Voltage)

The current equation in saturation mode is given by
*Id = (1/2) kn Vov²*, where:
- *Vov = Vgs - Vth*

The voltage gain is given by:
*Av = -gm Rd*or*Av = Vout/Vin*

A MOSFET in saturation and acts as a *constant current source*, making it useful for amplifier circuits.

- *Drain current equation:*
  *Id = (1/2) kn Vov², where **Vov = Vgs - Vth*.
- The amplifier gain follows *Av = -gm Rd*.



### CS amplifier analysis with resistive load

#### Components required
- **NMOS Transistors**: M1 (nmos-4).
- **Resistors**: R1 (1K ohm).
- **Power Supply**: Vdd (1.8V) for DC supply.
- **Input Signal Source**: Vin (0.9V) signal input.


#### Circuit diagram overview
![image alt](https://github.com/Mohith-s78/MOHITH-S/blob/2f2a3fc399b1af64bfbd4d79736028fb80e57308/Circuit%20Diagram.png)
## Procedure:

1. *Create a New Project*

2. *Set Up the values for MOSFET*
   - Configure the *NMOS transistor (CMOSN)* with:
     - Length: *500nm*
     - Width: *487nm*
3. *Perform DC Analysis*
   - Connect all circuit components properly.
   - Apply:
     - *Vdd = 1.8V*
     - *Vin = 0.9V*
   - Run *DC analysis* to obtain:
     - *Vout*
     - *Id*

4. *Run Transient Analysis*
   - Apply a *sine wave input*:
     - *Vin = 0.9V*
     - *Amplitude = 50mV*
     - *Frequency = 1kHz*
   - Run *transient analysis*
   - 
5. *Run AC Analysis*
   - Include all required library files.
   - Run *AC analysis* with:
     -Start and end frequency: *0.1Hz to 1THz*
## Results:
## DC analysis
The required current for the given power values to operate mosfet in satuturation region is 27.772 micro ampers, since only w and l can be varied to get the desired current so their values are 

- **W**=487nm
- **L**=500nm
- **Vdd**=1.8V
- **Vin**=0.9V
- **Id(M1)**=27.772uA

![image alt](https://github.com/Mohith-s78/MOHITH-S/blob/ab67f8b84c687072d5748d947145072219a16f87/Dc%20Analysis.png)


## Transient analysis
A sinusoidal input signal of 0.9V peak-to-peak is applied to the gate, and the output voltage is observed at the drain and it has a *180-degree phase shift* between input and output
- **Vout**=1.77223
![image alt](https://github.com/Mohith-s78/MOHITH-S/blob/8113823477753ba0baf632b34b50bc3020587a45/Trancient.png)


## AC analysis
This AC analysis evaluates the frequency response of a common-source NMOS amplifier. The gain is plotted over a wide frequency range to observe how the circuit amplifies signals at different frequencies and determine its bandwidth limitations.
![image alt](https://github.com/Mohith-s78/MOHITH-S/blob/2937182c543bfc28fc1e5f92ceceaba824800906/Ac%20Analysis.png)

## Gain:

*Av = -gm Rd*
*gm = 1/lamda*Id*
Practical result: *Gain =30.54064471dB* at 1KHz frequency.

![Image](https://github.com/Mohith-s78/MOHITH-S/blob/9fee2a95b4ba9d08aee72f0f80f91ec28d9b6944/Gain.png)

## Inference:
1. The MOSFET's *current (Id) is directly proportional to its width*, affecting overall circuit performance.
2. Operating in saturation region.
3. Transient analysis helps in evaluating the circuit’s response to time-varying signals, crucial for high-speed applications.
4. AC analysis aids in designing amplifiers with desired gain and understanding frequency behavior.
5. The overall analysis ensures proper design, optimization, and stability of the amplifier circuit.

## CS Amplifier with Diode-Connected MOSFET

## Components Required:
- NMOS (nmos4) and PMOS(pmos4)
- Voltage sources ()
- Bias DC source ()

## Circuit diagram:

![Image](https://github.com/Mohith-s78/MOHITH-S/blob/97556605043c0d76ca1d2dcad4951e017be9cfa5/circuit%20diagram.png)
### Procedure:
1. Set the PMOS transistor (CMOSP) with a length of ** and width of **.

2. *DC Analysis:*
   - Apply *Vdd = 1.8V* , *Vin = 0.9V* 
   - As the MOSFET should be in saturation region,
     Here Vb is connected to gate , so for us both the mosfet should be in saturation so for that Vgs>Vt 
    |Vg-Vs|>|Vt|
    here Vg is unknown so I calculated Vg ie Vg =Vb
    Vb=-2V
   - Run DC analysis to determine *Vout* and *Id*.

3. *Transient Analysis:*
   - Apply a sine wave input and observe the response.

4. *AC Analysis:*
   - Run AC analysis to measure gain and frequency response.
## Results:


### DC Analysis:
- *DC Operating Point:*
  - *Id1 =*
  - *Id2 =*
  - *Vout =*
  - *Width = * (NMOS)
  - *length =* (NMOS)
  -  *Width =* (PMOS)
  - *length =* (PMOS)
  - *Q-Point:* (1,79981V, 27.7uA)


![Image]()
### Transient Analysis:
- The output shows a *180-degree phase shift* between input and output.
- *Vout = * 


![Image](https://github.com/Mohith-s78/MOHITH-S/blob/ee0e15003dc777e459fde3f5f0dcd11671051852/trancient.png)
### AC Analysis:

![Image](https://github.com/Mohith-s78/MOHITH-S/blob/9b04796e1ba9cb7b424affb2f5042618c9bd19e0/ac.png)
## Gain:

*Av = -gm Rd*
*gm = 1/lamda*Id*

Practical result: *Gain = * at 1KHz frequency.

![Image]()
## Inference

1. The MOSFET's **drain current (Id) is directly proportional to its width (W)**, influencing circuit performance and power consumption.  
2. The MOSFET operates in the **saturation region** for amplification, ensuring a stable output.  
3. **Transient analysis** evaluates the circuit’s response to time-varying signals, which is crucial for high-speed applications and switching performance.  
4. **AC analysis** helps in designing amplifiers by determining gain, bandwidth, and frequency response.  
5. A comprehensive analysis ensures **optimal design, performance, and stability** of the amplifier circuit.








