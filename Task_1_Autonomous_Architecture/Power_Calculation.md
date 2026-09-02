# Power Calculation

## Selected Architecture

Intel RealSense D435i + NVIDIA Jetson Orin Nano


## Power Calculation Method

Electrical power is calculated using:

P = V × I

where:

P = Power consumption in Watts

V = Voltage

I = Current


## Component Power Consumption


|Component|Voltage|Current|Power|
|-|-|-|-|
|Intel RealSense D435i|5V|0.5A|2.5W|
|NVIDIA Jetson Orin Nano|5V|2A|10W|
|Pixhawk 6C Mini|5V|0.25A|1.25W|


## Total Power Consumption

Total power:

Ptotal = 2.5W + 10W + 1.25W

Ptotal = 13.75W


## Total Current Draw

Itotal = 0.5A + 2A + 0.25A

Itotal = 2.75A


## Conclusion

The selected autonomous architecture consumes approximately:

Power:
13.75W

Current:
2.75A at 5V

This power requirement must be considered while selecting the final battery because the autonomous system reduces overall flight endurance.
