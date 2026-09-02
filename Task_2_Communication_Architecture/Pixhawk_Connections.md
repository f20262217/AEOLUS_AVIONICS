# Pixhawk 6C Mini Communication Connections

## Overview

The Pixhawk 6C Mini acts as the central flight controller of the drone
communication architecture.

It connects: - RC receiver for manual pilot control - Telemetry module
for drone-to-ground communication - Video transmitter for live video
transmission

The architecture uses digital communication protocols wherever possible
because they provide better reliability, lower latency, and reduced
wiring complexity compared to older PWM/PPM systems.

------------------------------------------------------------------------

# 1. RC Receiver Connection

## Selected Component

RadioMaster RP3 ExpressLRS Receiver

## Purpose

The RC receiver receives commands from the pilot transmitter and sends
them to the Pixhawk flight controller.

Commands include: - Roll - Pitch - Yaw - Throttle - Flight mode
selection - Arm/disarm commands

## Communication Protocol

CRSF (Crossfire Serial Protocol)

CRSF is a digital UART-based communication protocol used by ExpressLRS
receivers.

Advantages: - Low latency - High reliability - Long range - Supports
telemetry feedback

## Pixhawk Connection

The receiver connects to a Pixhawk UART port.

  ExpressLRS Receiver   Pixhawk 6C Mini
  --------------------- -----------------
  TX                    RX
  RX                    TX
  5V                    5V
  GND                   GND

## Power Source

Powered from Pixhawk 5V supply rail.

Voltage = 5V Current = 100mA

Power: P = V × I P = 5 × 0.1 P = 0.5W

------------------------------------------------------------------------

# 2. Telemetry Module Connection

## Selected Component

Holybro SiK Telemetry Radio V3

## Purpose

Provides two-way communication between drone and ground station.

Transmits: - GPS position - Altitude - Battery voltage - Current
consumption - Flight mode - Sensor information - Mission status

## Communication Protocol

MAVLink

MAVLink is the standard communication protocol between Pixhawk flight
controllers and ground stations.

## Pixhawk Connection

Connected to TELEM1 UART port.

  SiK Telemetry Radio   Pixhawk TELEM1
  --------------------- ----------------
  TX                    RX
  RX                    TX
  5V                    5V
  GND                   GND

## Power Source

Voltage = 5V Current = 150mA

Power: P = V × I P = 5 × 0.15 P = 0.75W

------------------------------------------------------------------------

# 3. Video Transmitter (VTX) Connection

## Selected Component

DJI O3 Air Unit

## Purpose

Transmits live camera footage to pilot goggles.

Applications: - FPV flying - Manual inspection - Autonomous testing -
Emergency override

## Communication Type

Digital video transmission using 5.8GHz wireless communication.

## Connection

Camera → DJI O3 Air Unit → DJI Goggles

## Power Source

Powered separately from battery through voltage regulator/BEC.

Battery → Voltage Regulator/BEC → DJI O3 Air Unit

## Optional Pixhawk Connection

Pixhawk UART/MSP → DJI Air Unit

Can display: - Battery voltage - Flight mode - GPS information

------------------------------------------------------------------------

# Communication Summary

  --------------------------------------------------------------------------
  System         Component      Protocol       Connection     Power
  -------------- -------------- -------------- -------------- --------------
  RC Control     ExpressLRS     CRSF UART      UART Port      Pixhawk 5V
                 Receiver                                     

  Telemetry      Holyro SiK     MAVLink UART   TELEM1         Pixhawk 5V
                 Telemetry                                    
                 Radio V3                                     

  Video          DJI O3 Air     Digital Video  Camera/UART    Battery + BEC
                 Unit           Link                          
  --------------------------------------------------------------------------

------------------------------------------------------------------------

# Final Architecture

The final architecture uses: - ExpressLRS for low-latency pilot
control - SiK Telemetry Radio for MAVLink communication - DJI O3 Digital
VTX for video transmission
