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
| Capacity | 5000mAh |
| Capacity in Ah | 5Ah |
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
5000mAh = 5Ah
```

Therefore:

```
Energy = 14.8 × 5

Energy = 74Wh
```

Total battery energy:

**74Wh**

---

# 4. Usable Battery Energy

LiPo batteries should not be completely discharged.

A safe usable capacity of 80% is considered.

```
Usable energy = Total energy × 0.8

Usable energy = 74 × 0.8

Usable energy = 59.2Wh
```

Available flight energy:

**59.2Wh**

---

# 5. Hover Power Estimation from AUW
920KV motor + 10×4.5 prop on 4S
=commonly around 150 W/kg at hover for this size drone
Holybro's own spec states the S500 V2 (915g) sustains a 1500g payload (2415g total) at ~70% throttle — consistent with this loading range.
A separate owner report of the same 2216-920KV motor set on a ~2.6kg quad with a 4S 5000mAh battery logged ~11 minutes of flight, which back-calculates to a similar power loading.
Hover power = 150 W/kg × 2.5 kg = 375W
Hover current = Power/Voltage = 375/14.8 = 25.3A total

---

# 6. Flight Time Calculation

Using usable battery energy:

```
Flight time = Usable energy ÷ Average power
```

```
Flight time = 59.2/375 = 0.158 h 

Flight time = 0.158 hours
```

Convert to minutes:

```
Flight time = 0.158 × 60

Flight time = 9.5 minutes
```

Therefore:

**Estimated endurance = 9.5**

---

# 7. Requirement Check

| Requirement | Result |
|---|---|
| Required endurance | >12 minutes |
| Calculated endurance | 9.5 |
| Status | X |

The selected battery cannot satisfy the endurance requirement.

---

# 8. Revised Battery Pick

Trying a 4S 6750mAh 30C pack:

Total energy = 14.8 × 6.75 = 99.9Wh
Usable energy (80%) = 79.9Wh
Flight time = 79.9/375 = 0.213 h = 12.8 minutes

**Added pack weight vs the 5000mAh version is roughly +180g, which the S500 V2's rated 1500g payload capacity easily absorbs.**

---

# 9. Final Battery Selection

Selected battery:

**4S 6750mAh 30C LiPo**
Reasons-
Compatible voltage for the motor/ESC system
≈12.8 min estimated hover endurance (>12 min requirement, with margin)
Far more current capacity than the motors will ever draw
Weight increase over the original 5000mAh pick is negligible against the 2.5kg budget
