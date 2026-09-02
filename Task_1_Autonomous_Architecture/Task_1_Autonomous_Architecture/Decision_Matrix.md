# Decision Matrix

## Evaluation Method

Each architecture is rated from 1 to 5.

1 = Poor

5 = Excellent


## Criteria Weightage

|Parameter|Weight|
|-|-:|
|Autonomous capability|30%|
|Processing capability|25%|
|Power consumption|15%|
|Weight|10%|
|Reliability|10%|
|Cost|10%|


## Architecture Rating

|Architecture|Autonomy|Processing|Power|Weight|Reliability|Cost|
|-|-:|-:|-:|-:|-:|-:|
|Stereo Camera + Jetson Orin Nano|5|5|2|4|4|3|
|Depth Camera + Raspberry Pi 5|3|3|5|5|3|5|
|LiDAR + Raspberry Pi 5|4|3|4|4|5|3|
|Stereo Camera + Raspberry Pi 5|3|3|5|5|3|5|
|RealSense D435i + Jetson Orin Nano|5|5|3|4|5|3|


## Result

The Intel RealSense D435i with NVIDIA Jetson Orin Nano provides the best balance between autonomous capability, processing power, reliability, and practical implementation.

Although it has higher power consumption and cost, these disadvantages are acceptable because autonomous performance is the primary requirement.
