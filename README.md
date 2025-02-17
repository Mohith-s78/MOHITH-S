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

1. **Transistor Setup**:
- **M1** (NMOS) as the main amplifying transistor.
- Gate of **M1** is connected to the input node **Vin**.
- Source of **M1** connected to the ground.
- Drain of **M1** connected to the resistor.

2. **Biasing**:
- **Vin** provides the input signal.

3. **Load resistor**:
- one terminal of resistor is connected to the drain of M1 and the other to Vdd.

## DC analysis
The required current for the given power values to operate mosfet in satuturation region is 27.772 micro ampers, since only w and l can be varied to get the desired current so their values are 

- **W**=487nm

- **L**=500nm

#### Results

- **Vdd**=1.8V


- **Vin**=0.9V


- **Vout**=1.77223V


- **Id(M1)**=27.772uA


- **Ig(M1)**=0A





## Transient analysis
A sinusoidal input signal of 0.9V peak-to-peak is applied to the gate, and the output voltage is observed at the drain


### Results
An interveting output curve was obtained when Vin and Vout was plotted against voltage and time with 1ms cycle.
here we can observe a rough 180 degree phase shift between input and output.



## AC analysis
This AC analysis evaluates the frequency response of a common-source NMOS amplifier. The gain is plotted over a wide frequency range to observe how the circuit amplifies signals at different frequencies and determine its bandwidth limitations.

#### Results

The gain remains stable at lower frequencies.

The amplifier’s bandwidth and highlights its frequency-dependent performance.



### Experiment 2

### CS amplifier analyisis with PMOS replced by resistor

#### Components
