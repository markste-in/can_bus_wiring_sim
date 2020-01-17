# Simulating CAN Bus Wiring with LTspice and iCircuit

#### The primary motivation was to explain the overshooting I see from time to time when troubleshooting CAN Bus networks


#### To anticipate it, the preferred tool is LTspice due to significantly better accuracy.

## Simulation with LTspice

### Basic Setup

![png](LTspice/can_bus_wiring.png)

### "Good" CAN Bus

![png](LTspice/good/can_bus_wiring_good.png)

### A few disturbances

![png](LTspice/some_disturbances/can_bus_wiring_some_C_and_L.png)

### Strong disturbances

![png](LTspice/strong_disturbances/can_bus_wiring_strong_disturbances.png)

The appropriate FFT

![png](/Users/markstein/prj/can_bus_sim/LTspice/strong_disturbances/can_bus_wiring_strong_disturbances.fft.png)

## Simulation with iCircuit

### The Tool [iCircuit](http://icircuitapp.com/) is available for Mac/iOS, Windows and Android

![png](iCircuit/can_bus_simple.png)

#### This simulation should be taken with a grain of salt as the accuracy of iCircuit seems to be limited at higher frequencies!
#### I was also not able to figure out how to improve the simulation accuracy or decrease Tstep
