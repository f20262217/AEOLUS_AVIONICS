# ESC Selection and Analysis

# 1. Selected Motor Configuration

The ESC must be selected according to the motor and propeller combination, along with the maximum current requirement of the propulsion system.

Selected propulsion system:

| Component | Specification |
|---|---|
| Motor | Holybro S500 V2 2216-920KV |
| Propeller | Pro-Range 1045 (10×4.5 inch) |
| Battery | 4S LiPo (14.8V) |
| Number of Motors | 4 |

---

# 2. Motor Current Requirement

The maximum current drawn by one motor with the 1045 propeller on a 4S LiPo battery is:

**Maximum motor current = 17.4A**

For a quadcopter configuration with four motors:

Total current = Current per motor × Number of motors

Total current = 17.4 × 4

Total current = 69.6A

Therefore:

**Maximum propulsion system current ≈ 70A**

The battery and power distribution system must therefore support a minimum of approximately 70A continuous current for all four motors.

---

# 3. ESC Current Rating Calculation

Each ESC controls one motor, therefore the ESC rating is calculated using the current requirement of a single motor.

A safety margin is added to prevent overheating and handle transient current spikes.

Assuming a 25% safety margin:

Required ESC current = Maximum motor current × Safety factor

Required ESC current = 17.4 × 1.25

Required ESC current = 21.75A

Therefore:

**Minimum required ESC rating ≈ 22A**

---

# 4. Selected ESC

## 25A BLHeli-S ESC

The ESC is selected based on the maximum motor current requirement and the calculated safety margin.

The 2216-920KV motor with a 1045 propeller on a 4S LiPo battery can draw:

Maximum motor current = 17.4A

Including a 25% safety margin:

Required ESC rating:


Required ESC current = 17.4 × 1.25

Required ESC current = 21.75A


Therefore, an ESC rated above 22A is required.

A **25A ESC** is selected because:

- It exceeds the calculated requirement of 21.75A
- Provides additional protection against transient current spikes
- Is compatible with the 4S LiPo power system
- Maintains a good balance between weight, reliability, and efficiency

---

# 5. ESC Current Capability Check

Each motor uses one ESC.

Each ESC is rated for 25A continuous current.

For four motors:

Total ESC current handling capability:

Total ESC capacity = ESC rating × Number of ESCs

Total ESC capacity = 25 × 4

Total ESC capacity = 100A

This represents the combined current handling capability of all ESCs. Each individual ESC provides sufficient capacity for its corresponding motor requirement of 17.4A.

Maximum propulsion current demand:


Maximum motor demand = 17.4 × 4

Maximum motor demand = 69.6A


Current margin:


Margin = Total ESC capacity - Motor demand

Margin = 100 - 69.6

Margin = 30.4A

**Available current margin = 30.4A**

For a single motor:

ESC headroom = ESC rating - Motor current

ESC headroom = 25 - 17.4

ESC headroom = 7.6A

The selected ESC system provides sufficient current headroom for acceleration, manoeuvres, and temporary current spikes.

---

# 6. ESC Features

The selected ESC provides:

- BLHeli-S firmware support
- Compatibility with 4S LiPo batteries
- Efficient brushless motor control
- Adequate current handling for 2216 motors
- Lightweight design suitable for a 10 inch quadcopter

---

# 7. Final ESC Selection

| Parameter | Value |
|-|-|
| ESC Rating | 25A |
| Number of ESCs | 4 |
| Battery Compatibility | 4S LiPo |
| Total Current Capacity | 100A |
| Maximum Motor Demand | 69.6A |


- Safety margin
- Weight
- Efficiency
- Compatibility with the selected propulsion system
