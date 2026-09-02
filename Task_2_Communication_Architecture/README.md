# Task 2: Communication Architecture

## Objective

The objective of this task is to design the communication architecture of an autonomous drone.

The system must support:

- Manual RC control
- Telemetry communication
- Live video transmission


## Communication Systems

The drone communication architecture consists of three independent systems:

1. RC transmitter and receiver
2. Telemetry module
3. Video transmitter (VTX)


## Selected Components

The proposed architecture uses:

- RadioMaster TX16S with ExpressLRS receiver for RC control
- Holybro SiK Telemetry Radio for MAVLink communication
- DJI O3 Air Unit for digital video transmission


## Main Controller

The Pixhawk 6C Mini acts as the central flight controller connecting the communication systems with the propulsion system.
