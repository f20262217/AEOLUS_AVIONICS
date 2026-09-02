# Component Selection

## Overview

The communication architecture consists of:

-   RC system for pilot control
-   Telemetry system for drone-to-ground communication
-   Video transmitter system for live video transmission

The selection is based on:

-   Reliability
-   Range
-   Latency
-   Compatibility with Pixhawk 6C Mini
-   Power consumption
-   Digital versus analog communication advantages

------------------------------------------------------------------------

# 1. RC System Selection

## Purpose of RC System

The RC system provides direct manual control of the drone.

It is responsible for transmitting:

-   Roll commands
-   Pitch commands
-   Yaw commands
-   Throttle commands
-   Flight mode changes
-   Emergency control commands

------------------------------------------------------------------------

# Communication Technologies Comparison

## PWM (Pulse Width Modulation)

PWM represents information by changing the width of an electrical pulse while keeping the signal cycle constant.

In RC systems, the pulse width represents the command value for a channel.

Typical RC PWM values:

- 1000µs pulse width → Minimum command
- 1500µs pulse width → Neutral position
- 2000µs pulse width → Maximum command


Example:

Throttle control:

1000µs → Motor off

1500µs → Mid throttle

2000µs → Full throttle


Advantages:

- Simple and easy to decode
- Compatible with many older RC systems
- Direct control of individual channels


Disadvantages:

- Requires a separate signal wire for every channel
- Increases wiring complexity
- Limited scalability for systems requiring many channels


Example PWM receiver output:

Channel 1 → Roll

Channel 2 → Pitch

Channel 3 → Throttle

Channel 4 → Yaw


---

## PPM (Pulse Position Modulation)

PPM represents information by changing the position of pulses in time while keeping the pulse width approximately constant.

Instead of sending each channel through a separate wire, multiple channels are combined into a single signal.

Example:

Channel 1 | gap | Channel 2 | gap | Channel 3 | gap | Channel 4


The timing position of each pulse represents the value of that channel.


Advantages:

- Requires only one signal wire for multiple channels
- Reduces wiring compared to PWM
- Simpler than multiple PWM connections


Disadvantages:

- Older technology compared to modern digital protocols
- More sensitive to timing errors
- Lower update rates compared to modern serial protocols


---

## PWM/PPM Compatibility Issue

Modern flight controllers such as Pixhawk 6C Mini generally prefer digital communication protocols such as:

- CRSF
- SBUS
- MAVLink
- CAN


PWM and PPM are older signal formats and cannot directly communicate with UART-based digital ports.

For example:

PWM/PPM receiver output:

Analog timing signals

↓

Requires conversion

↓

Pixhawk digital UART input


Therefore, the selected ExpressLRS receiver uses CRSF UART instead of PWM or PPM because it provides:

- Higher update rate
- Lower latency
- Bidirectional communication
- Direct Pixhawk compatibility

------------------------------------------------------------------------

## SBUS

SBUS is a digital serial communication protocol.

Advantages:

-   Single-wire communication
-   Lower latency than PWM/PPM

Disadvantages:

-   Less flexible compared to newer protocols

------------------------------------------------------------------------

## CRSF (ExpressLRS)

CRSF is a modern digital UART protocol used by ExpressLRS.

Advantages:

-   Very low latency
-   High refresh rate
-   Long range
-   Supports telemetry communication
-   Requires only UART connection

------------------------------------------------------------------------

# Selected RC System

## Transmitter

RadioMaster TX16S Mark II

## Receiver

RadioMaster RP3 ExpressLRS Receiver

------------------------------------------------------------------------

# Reason for Selection

ExpressLRS was selected because it provides:

-   Low latency control
-   Reliable long-range communication
-   Digital communication with Pixhawk
-   Better performance compared to PWM and PPM systems

The RadioMaster RP3 receiver communicates using CRSF over UART, making
it compatible with modern flight controllers.

------------------------------------------------------------------------

# RC Communication

Architecture:

RadioMaster TX16S

↓

2.4GHz ExpressLRS Link

↓

RP3 ExpressLRS Receiver

↓

CRSF UART

↓

Pixhawk 6C Mini

------------------------------------------------------------------------

# 2. Telemetry System Selection

## Purpose of Telemetry

Telemetry provides two-way communication between the drone and ground
station.

It allows monitoring of:

-   GPS position
-   Battery voltage
-   Current consumption
-   Altitude
-   Flight mode
-   Sensor data

It also allows:

-   Mission uploading
-   Parameter configuration
-   Flight analysis

------------------------------------------------------------------------

# Telemetry Options Comparison

## WiFi Telemetry

Advantages:

-   High data rate
-   Easy integration

Disadvantages:

-   Limited range
-   Higher power consumption
-   Less reliable for long-distance drone operation

------------------------------------------------------------------------

## LoRa Telemetry

Advantages:

-   Extremely long range
-   Low power consumption

Disadvantages:

-   Lower data rate

------------------------------------------------------------------------

## SiK Telemetry

Advantages:

-   Designed for Pixhawk systems
-   MAVLink compatible
-   Reliable communication
-   Low power consumption

------------------------------------------------------------------------

# Selected Telemetry System

Holybro SiK Telemetry Radio V3

------------------------------------------------------------------------

# Reason for Selection

The Holybro SiK Telemetry Radio was selected because:

-   It directly supports Pixhawk flight controllers
-   It uses MAVLink protocol
-   It integrates easily through UART TELEM ports
-   It provides reliable communication with ground stations

------------------------------------------------------------------------

# Telemetry Communication

Architecture:

Pixhawk 6C Mini

↓

MAVLink UART

↓

SiK Telemetry Radio

↓

Ground Station

------------------------------------------------------------------------

# 3. Video Transmitter Selection

## Purpose of VTX

The video transmitter provides a live video feed from the drone camera
to the pilot.

Applications:

-   Manual flight
-   Autonomous testing
-   Drone inspection
-   Emergency override

------------------------------------------------------------------------

# Analog vs Digital VTX Comparison

## Analog VTX

Advantages:

-   Low latency
-   Low cost
-   Simple technology

Disadvantages:

-   Lower image quality
-   More interference
-   Signal degradation appears as noise

------------------------------------------------------------------------

## Digital VTX

Advantages:

-   High-definition video
-   Better image quality
-   Improved signal handling
-   Better user experience

Disadvantages:

-   Higher cost
-   Higher power consumption

------------------------------------------------------------------------

# Selected VTX System

DJI O3 Air Unit

------------------------------------------------------------------------

# Reason for Selection

The DJI O3 Air Unit was selected because:

-   It provides high-quality digital video
-   It improves visual feedback during autonomous testing
-   It provides reliable video transmission
-   It is suitable for professional drone platforms

------------------------------------------------------------------------

# Communication Range Comparison


## RC System Range

Selected system:

RadioMaster TX16S + RP3 ExpressLRS Receiver


Protocol:

2.4GHz ExpressLRS using CRSF


Typical range:

Approximately 10-30 km depending on:

- Antenna orientation
- Transmitter power
- Environment
- Interference


For autonomous drone operation, this provides sufficient range for reliable manual override and emergency control.



---

## Telemetry Range

Selected system:

Holybro SiK Telemetry Radio V3


Protocol:

MAVLink over 915MHz/433MHz radio link


Typical range:

Approximately 1-3 km for standard modules.

Higher power versions and improved antennas can extend the range further.


The range is suitable because telemetry is mainly required for:

- Mission monitoring
- Parameter updates
- Flight data transmission



---

## Video Transmission Range

Selected system:

DJI O3 Air Unit


Protocol:

5.8GHz Digital Video Transmission


Typical range:

Approximately 10 km maximum under ideal conditions with compatible DJI goggles.


Actual range depends on:

- Antenna placement
- Obstacles
- Signal interference
- Regulatory limits


The digital video system was selected because HD video quality is more important than extremely low cost for autonomous testing.



---

# Final Communication Comparison

|System|Component|Protocol|Approximate Range|Purpose|
|-|-|-|-|-|
|RC Control|RadioMaster TX16S + RP3 ExpressLRS|CRSF|10-30 km|Pilot control and emergency override|
|Telemetry|Holybro SiK Telemetry V3|MAVLink|1-3 km|Drone monitoring and mission communication|
|Video|DJI O3 Air Unit|Digital 5.8GHz Link|Up to 10 km|Live FPV video|

# Final Communication Component Selection

  -----------------------------------------------------------------------
  System            Selected          Protocol          Reason
                    Component                           
  ----------------- ----------------- ----------------- -----------------
  RC Control        RadioMaster       CRSF UART         Low latency,
                    TX16S + RP3                         reliable, long
                    ExpressLRS                          range
                    Receiver                            

  Telemetry         Holybro SiK       MAVLink UART      Pixhawk
                    Telemetry Radio                     compatibility and
                    V3                                  reliable ground
                                                        communication

  Video             DJI O3 Air Unit   Digital Video     High-quality
                                      Link              video
                                                        transmission
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Conclusion

The selected communication architecture provides reliable control,
monitoring, and video transmission.

The combination of ExpressLRS, SiK telemetry, and DJI O3 provides:

-   Low latency control
-   Reliable telemetry communication
-   High-quality video feedback
-   Compatibility with the Pixhawk 6C Mini flight controller
