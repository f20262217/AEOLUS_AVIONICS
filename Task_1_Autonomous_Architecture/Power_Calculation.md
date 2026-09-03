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
|NVIDIA Jetson Orin Nano|5V-12V*|2.5A (approx.)|15W|
|Pixhawk 6C Mini|5V|0.25A|1.25W|


## Total Power Consumption

The total power consumption is estimated as:

Ptotal = Prealsense + Pjetson + Ppixhawk

Ptotal = 2.5W + 15W + 1.25W

Ptotal = 18.75W


## Total Current Draw

Assuming a common 5V power rail for the auxiliary electronics:

Itotal = Ptotal / Voltage

Itotal = 18.75 / 5

Itotal = 3.75A

## Conclusion

The selected autonomous architecture consumes approximately:

Power:

18.75W

Current:

3.75A at 5V equivalent supply

The Jetson Orin Nano power consumption was estimated using a realistic operating value rather than the minimum 10W mode, since actual power depends on the selected performance mode and workload.

The propulsion system remains the dominant power consumer, therefore this correction does not significantly affect the overall battery selection.
This power requirement must be considered while selecting the final battery because the autonomous system reduces overall flight endurance.
