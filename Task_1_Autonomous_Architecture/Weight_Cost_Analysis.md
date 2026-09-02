# Weight and Cost Analysis


## Selected Architecture

Intel RealSense D435i + NVIDIA Jetson Orin Nano


# Weight Calculation


|Component|Weight|
|-|-:|
|Intel RealSense D435i|72g|
|NVIDIA Jetson Orin Nano|90g|
|MicroSD Storage|5g|
|DC-DC Power Regulator|20g|


## Total Weight

Total weight:

72g + 90g + 5g + 20g

= 187g


The autonomous architecture adds approximately 187g to the drone.


Considering the maximum drone weight limit of 2.5kg:

Remaining payload capacity:

2500g - 187g

= 2313g


The selected architecture satisfies the weight requirement.



# Cost Calculation


|Component|Approximate Cost|
|-|-:|
|Intel RealSense D435i|₹25,000|
|NVIDIA Jetson Orin Nano|₹25,000|
|Accessories|₹2,000|


## Total Cost

Total estimated cost:

₹25,000 + ₹25,000 + ₹2,000

= ₹52,000


## Cost Justification

Although this architecture has a higher cost compared to Raspberry Pi based systems, it provides significantly better processing capability required for autonomous navigation, computer vision, and obstacle avoidance.
