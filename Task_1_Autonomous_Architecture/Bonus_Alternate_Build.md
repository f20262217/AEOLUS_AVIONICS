# Bonus: Alternate Build Suggestion


## Proposed Alternative Architecture

A more advanced autonomous architecture would combine:

- Stereo Camera
- LiDAR sensor
- NVIDIA Jetson Orin Nano


## Concept

The stereo camera provides visual information such as object recognition and scene understanding.

The LiDAR provides accurate distance measurements and reliable obstacle detection.

The Jetson Orin Nano performs sensor fusion and runs autonomous navigation algorithms.


## Advantages

### Improved Reliability

LiDAR provides distance information even in low visibility conditions where cameras may perform poorly.

### Better Mapping

Combining camera and LiDAR data improves 3D mapping and localization.

### Improved Autonomous Navigation

Sensor fusion allows better obstacle avoidance and path planning.


## Disadvantages

- Increased cost
- Increased weight
- Higher power consumption
- More complex software


## Comparison With Selected Architecture

The selected Intel RealSense D435i + Jetson Orin Nano architecture provides an excellent balance between cost, weight, and performance.

The LiDAR + Stereo Camera + Jetson architecture would provide better performance but would be more suitable for professional applications where reliability is more important than cost.
