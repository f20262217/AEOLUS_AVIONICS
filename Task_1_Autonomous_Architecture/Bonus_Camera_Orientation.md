# Bonus: Camera Orientation


## Camera Placement

For autonomous navigation, the Intel RealSense D435i should be mounted on the front side of the drone facing the direction of motion.

This allows the drone to detect obstacles before reaching them and enables path planning.


## Camera Angle

The camera should be tilted slightly downward by approximately 10-15 degrees.

Advantages:

- Maintains obstacle visibility
- Provides information about terrain
- Helps with landing area detection
- Improves depth perception near the drone


## Stereo Camera Alignment

For stereo vision systems, both cameras must remain:

- Parallel
- Fixed distance apart
- Horizontally aligned

This ensures accurate depth estimation using disparity.


## Vibration Isolation

The camera should be mounted away from high vibration sources such as motors.

A vibration-isolated mount improves:

- Image quality
- Depth accuracy
- IMU performance


## Final Orientation

The recommended configuration is:

Front-mounted RealSense D435i

+

10-15 degree downward tilt

+

Vibration-isolated mounting
