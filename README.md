# Simulating CAN bus wiring with LTspice and iCircuit

#### The primary motivation was to explain the overshooting and ringing I see from time to time when troubleshooting CAN bus networks


#### To anticipate it, the preferred tool is LTspice due to significantly better accuracy.

## Simulation with LTspice

### Basic Setup

Assumptions:
- 250 kBaud
- 120 Ohms impedance
- 2x 120 Ohms termination resistors
- 2x20m CAN bus wires going from the transceiver to each terminating resistor
- Signal speed 200'000 km/s -> 5ns/m 
  - Signal delay time 0.1&mu;s for 20m (used in tline)

The CAN transceiver is modelled as two square wave generators. One for CAN high and one for CAN low
![png](LTspice/can_bus_wiring.png)

### "Good" CAN Bus

![png](LTspice/good/can_bus_wiring_good.png)

### A few disturbances

![png](LTspice/some_disturbances/can_bus_wiring_some_C_and_L.png)

### Strong disturbances

![png](LTspice/strong_disturbances/can_bus_wiring_strong_disturbances.png)

The appropriate FFT

![png](LTspice/strong_disturbances/can_bus_wiring_strong_disturbances.fft.png)

## Simulation with iCircuit

### The Tool [iCircuit](http://icircuitapp.com/) is available for Mac/iOS, Windows and Android

![png](iCircuit/can_bus_simple.png)

#### This simulation should be taken with a grain of salt as the accuracy of iCircuit seems to be very limited at higher frequencies!
#### I was also not able to figure out how to improve the simulation accuracy or decrease Tstep
