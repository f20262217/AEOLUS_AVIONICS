# Component Selection

## Overview

This document explains the selection of communication components for the
autonomous drone platform.

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

## PWM

PWM receivers provide individual outputs for each channel.

Example:

-   Channel 1 → Roll
-   Channel 2 → Pitch
-   Channel 3 → Throttle
-   Channel 4 → Yaw

Advantages:

-   Simple concept
-   Compatible with older flight controllers

Disadvantages:

-   Requires many wires
-   Limited scalability
-   Higher wiring complexity

------------------------------------------------------------------------

## PPM

PPM combines multiple channels into a single signal.

Advantages:

-   Reduced wiring compared to PWM

Disadvantages:

-   Older technology
-   Lower performance compared to modern digital protocols

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
