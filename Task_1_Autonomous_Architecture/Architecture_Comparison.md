# Architecture Comparison

## Introduction

An autonomous drone requires two major components:

1. Sensors to perceive the environment.
2. A companion computer to process sensor data and make decisions.

Five possible sensor-computer architectures were evaluated based on their ability to support autonomous navigation, obstacle avoidance, power consumption, weight, and cost.


---

# Architecture 1: Stereo Camera + NVIDIA Jetson Orin Nano


## Working Principle

A stereo camera uses two cameras separated by a fixed distance. Similar to human vision, the two images have a slight difference called disparity. This disparity is processed to estimate depth information.

The Jetson Orin Nano acts as the processing unit and performs:

- Computer vision
- Object detection
- SLAM
- Autonomous navigation algorithms


## Advantages

- High processing capability
- Suitable for advanced AI applications
- Can run neural networks
- Provides 3D environmental information


## Disadvantages

- Higher power consumption
- Higher cost
- Requires more computational resources


## Suitable Applications

- Search and rescue drones
- Autonomous delivery drones
- Industrial inspection


---

# Architecture 2: Depth Camera + Raspberry Pi 5


## Working Principle

A depth camera provides RGB images along with depth information. Unlike a normal camera, each pixel contains distance information.

The Raspberry Pi 5 processes the sensor data and runs basic autonomy algorithms.


## Advantages

- Lower cost
- Low power consumption
- Lightweight
- Easier development


## Disadvantages

- Limited AI processing capability
- Cannot handle very complex autonomous algorithms
- Lower performance compared to Jetson


## Suitable Applications

- Educational drones
- Indoor navigation
- Basic obstacle avoidance


---

# Architecture 3: LiDAR + Raspberry Pi 5


## Working Principle

LiDAR uses laser pulses to measure distance. The time taken for the laser to return after hitting an object is used to calculate distance.


## Advantages

- Very accurate distance measurements
- Works in low light conditions
- Reliable for mapping


## Disadvantages

- Does not provide colour or object information
- Higher sensor cost
- Limited understanding of the environment


## Suitable Applications

- Mapping drones
- Terrain following
- Industrial environments


---

# Architecture 4: Stereo Camera + Raspberry Pi 5


## Working Principle

A stereo camera generates depth information by comparing images from two cameras. Raspberry Pi 5 performs image processing and navigation calculations.


## Advantages

- Low cost
- Lightweight
- Provides depth information


## Disadvantages

- Limited processing capability
- Difficult to run advanced AI models
- Stereo processing requires high computation


## Suitable Applications

- Small autonomous drones
- Research projects
- Basic navigation


---

# Architecture 5: Intel RealSense D435i + NVIDIA Jetson Orin Nano


## Working Principle

The Intel RealSense D435i combines:

- RGB camera
- Stereo infrared depth cameras
- IMU sensor

The Jetson Orin Nano processes this information for:

- Mapping
- Localization
- Obstacle avoidance
- AI-based decision making


## Advantages

- Complete perception system
- Depth + RGB + IMU in one sensor
- Excellent for autonomous navigation
- High AI processing capability


## Disadvantages

- Higher cost
- Higher power consumption
- More complex software requirements


## Suitable Applications

- Autonomous drones
- Robotics
- Advanced navigation systems


---

# Summary

The architectures provide different trade-offs between cost, power, weight, and autonomy.

Low-cost systems based on Raspberry Pi are suitable for simple autonomous tasks, while Jetson-based systems provide the processing power required for advanced autonomous operation.

A weighted decision matrix will be used to select the final architecture.
