# Motor and Propeller Analysis

## 1. Selected Propulsion Components

The drone uses the following propulsion system:

| Component | Specification |
|---|---|
| Motor | Holybro S500 V2 Motor 2216-920KV-CCW |
| Propeller | 1045 (10×4.5 inch) |
| Number of Motors | 4 (Quadcopter configuration) |

The selected motor-propeller combination is designed for 10 inch quadcopters and is compatible with a 4S LiPo battery setup.

---

# 2. Thrust Requirement Calculation

The maximum allowed drone weight is:

**Maximum weight = 2.5 kg**

For stable flight and good maneuverability, the target thrust-to-weight ratio is considered as:

**Thrust-to-weight ratio = 2:1**

Therefore, required total thrust:

```
Required thrust = Drone weight × Safety factor

Required thrust = 2.5 × 2

Required thrust = 5 kg
```

Since the drone has four motors:

```
Required thrust per motor = Total thrust ÷ Number of motors

Required thrust per motor = 5 ÷ 4

Required thrust per motor = 1.25 kg
```

Therefore, each motor should provide at least:

**Required thrust per motor = 1.25 kg**

---

# 3. Motor Thrust Performance

For the Holybro 2216-920KV motor with a 1045 propeller:

Maximum thrust per motor:

**≈ 1.37 kg**

Total available thrust:

```
Total thrust = Single motor thrust × Number of motors

Total thrust = 1.37 × 4

Total thrust = 5.48 kg
```

Therefore:

**Available thrust = 5.48 kg**

---

# 4. Thrust Margin Check

Required thrust:

**5 kg**

Available thrust:

**5.48 kg**

Extra thrust available:

```
Thrust margin = Available thrust - Required thrust

Thrust margin = 5.48 - 5

Thrust margin = 0.48 kg
```

The thrust-to-weight ratio is:

```
Thrust-to-weight ratio = Total thrust ÷ Drone weight

Thrust-to-weight ratio = 5.48 ÷ 2.5

Thrust-to-weight ratio = 2.19:1
```

A ratio above 2:1 provides:

- Stable hovering
- Better control response
- Ability to handle additional payload
- Safer operation during wind disturbances

---

# 5. Motor Current Requirement

The maximum current drawn by one motor with the 1045 propeller is approximately:

**Motor current = 17.4A**

For four motors:

```
Total motor current = Current per motor × Number of motors

Total motor current = 17.4 × 4

Total motor current = 69.6A
```

Maximum propulsion current:

**≈ 70A**

This value is used later for ESC and battery selection.

---

# 6. Final Motor and Propeller Selection

The Holybro 2216-920KV motor with 1045 propellers is selected because:

- It provides 5.48 kg total thrust
- It satisfies the 2:1 thrust requirement
- It is compatible with a 4S LiPo battery
- It provides enough margin for autonomous drone payloads
- It is the recommended propulsion combination for the S500 V2 platform

## Final Selection:

**Motor:** Holybro S500 V2 2216-920KV  
**Propeller:** 1045 (10×4.5 inch)  
**Configuration:** 4 motor quadcopter
