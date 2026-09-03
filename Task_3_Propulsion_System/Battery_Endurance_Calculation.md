# Battery Selection and Endurance Calculation

# 1. Battery Requirement

The battery must satisfy:

- Compatibility with the Holybro 2216-920KV motors
- Enough energy for more than 12 minutes of flight time
- Weight must keep the drone below 2.5 kg

The selected battery is:

| Parameter | Value |
|---|---|
| Battery Type | LiPo |
| Configuration | 4S |
| Voltage | 14.8V |
| Capacity | 6750mAh |
| Capacity in Ah | 6.75Ah |
| C Rating | 30C |

---

# 2. Battery Voltage Calculation

A LiPo cell has a nominal voltage of approximately:

**3.7V per cell**

For a 4S battery:

```
Battery voltage = Number of cells × Cell voltage

Battery voltage = 4 × 3.7

Battery voltage = 14.8V
```

Therefore:

**Battery voltage = 14.8V**

This voltage is suitable for the 2216-920KV motor and 1045 propeller combination.

---

# 3. Battery Energy Calculation

Battery energy is calculated using:

```
Energy = Voltage × Capacity
```

The battery capacity is:

```
6750mAh = 6.75Ah
```

Therefore:

```
Energy = 14.8 × 6.75

Energy = 99.9Wh
```

Total battery energy:

**99.9Wh**

---

# 4. Usable Battery Energy

LiPo batteries should not be completely discharged.

A safe usable capacity of 80% is considered.

```
Usable energy = Total energy × 0.8

Usable energy = 99.9 × 0.8

Usable energy = 79.9Wh
```

Available flight energy:

**79.9Wh**

---

# 5. Hover Power Estimation Using Motor Data

The motor produces:

Maximum thrust per motor:

1.37kg

For a 4 motor quadcopter with maximum thrust:

Total maximum thrust:

Total thrust = 1.37 × 4

Total thrust = 5.48kg


For a maximum takeoff weight of 2.5kg:

Required thrust per motor:

Required thrust = 2.5 / 4

Required thrust = 0.625kg per motor


The operating thrust percentage is:

Thrust ratio = 0.625 / 1.37

Thrust ratio = 0.456

Therefore, each motor operates at approximately:

45.6% of maximum thrust.


Using the propeller affinity relationship:

Power ∝ RPM³

and

RPM ∝ √Thrust


The estimated hover power is approximately:

Total hover power ≈ 316W

---

# 6. Flight Time Calculation

Using usable battery energy:

Usable energy = 79.9Wh


Flight time = Usable energy / Average power


Flight time = 79.9 / 316


Flight time = 0.253 hours


Flight time = 0.253 × 60


Flight time ≈ 15.2 minutes

---

# 7. Requirement Check

| Requirement | Result |
|---|---|
| Required endurance | >12 minutes |
| Calculated endurance | 15.2 |
| Status | Pass |

The selected battery cannot satisfy the endurance requirement.

---

# 8. Revised Battery Pick

Trying a 4S 6750mAh 30C pack:

Total energy = 14.8 × 6.75 = 99.9Wh
Usable energy (80%) = 79.9Wh
Flight time = 79.9/375 = 0.213 h = 15.2 minutes

**Added pack weight vs the 5000mAh version is roughly +180g, which the S500 V2's rated 1500g payload capacity easily absorbs.**

---

# 9. Final Battery Selection

Selected battery:

**4S 6750mAh 30C LiPo**
Reasons-
Compatible voltage for the motor/ESC system
15.2 min estimated hover endurance (>12 min requirement, with margin)
Far more current capacity than the motors will ever draw
Weight increase over the original 5000mAh pick is negligible against the 2.5kg budget
