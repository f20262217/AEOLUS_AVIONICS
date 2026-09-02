# ESC Selection and Analysis

## 1. Selected Motor Configuration

The ESC must be selected according to the motor and propeller combination.

Selected propulsion system:

| Component | Specification |
|---|---|
| Motor | Holybro S500 V2 2216-920KV |
| Propeller | 1045 (10×4.5 inch) |
| Battery | 4S LiPo |
| Number of Motors | 4 |

---

# 2. Motor Current Requirement

The maximum current drawn by one motor using the 1045 propeller is approximately:

**Maximum motor current = 17.4A**

For a quadcopter with four motors:

```
Total current = Current per motor × Number of motors

Total current = 17.4 × 4

Total current = 69.6A
```

Therefore, the complete propulsion system can draw:

**Maximum propulsion current ≈ 70A**

---

# 3. ESC Current Rating Calculation

An ESC should not operate continuously at its maximum rating.

A safety margin of 25% is considered:

```
Required ESC current = Motor current × Safety factor

Required ESC current = 17.4 × 1.25

Required ESC current = 21.75A
```

Therefore, the minimum suitable ESC rating is:

**Required ESC rating ≈ 22A**

---

# 4. Selected ESC

## Holybro BLHeli S 20A ESC

The S500 V2 platform uses a 20A ESC with the 2216-920KV motor and 1045 propeller combination.

Although the calculated requirement is approximately 22A, the 20A ESC is selected because:

- It is the manufacturer recommended ESC for this motor-propeller setup
- The maximum current value occurs at full throttle, which is not the normal flight condition
- It reduces overall drone weight
- It provides sufficient performance for the intended 10 inch quadcopter design

---

# 5. ESC Current Capability Check

Total ESC current capability:

```
Total ESC capacity = ESC rating × Number of ESCs

Total ESC capacity = 20 × 4

Total ESC capacity = 80A
```

Maximum motor demand:

```
Maximum motor demand = 69.6A
```

Current margin:

```
Margin = ESC capacity - Motor demand

Margin = 80 - 69.6

Margin = 10.4A
```

Therefore:

**Available current margin = 10.4A**

---

# 6. ESC Features

The selected ESC provides:

- BLHeli-S firmware support
- Compatibility with 4S LiPo batteries
- Efficient motor control
- Suitable current handling for 2216 motors
- Lightweight design suitable for a 10 inch drone

---

# 7. Final ESC Selection

| Parameter | Value |
|---|---|
| ESC Model | Holybro BLHeli S 20A ESC |
| Number of ESCs | 4 |
| Battery Compatibility | 4S LiPo |
| Total Current Capacity | 80A |
| Maximum Motor Demand | 69.6A |

The selected ESC provides a suitable balance between:

- Safety
- Weight
- Efficiency
- Compatibility with the selected propulsion system
