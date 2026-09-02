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

# 5. Average Power Consumption

The S500 V2 platform with a 5000mAh battery has an expected hover time of approximately 18 minutes under normal conditions.

Average power consumption:

```
Power = Energy ÷ Time
```

Convert flight time:

```
18 minutes = 18 ÷ 60

18 minutes = 0.3 hours
```

Therefore:

```
Power = 74 ÷ 0.3

Power = 246.6W
```

Average hover power:

**≈247W**

---

# 6. Average Current Calculation

Using:

```
Power = Voltage × Current
```

Rearranging:

```
Current = Power ÷ Voltage
```

Therefore:

```
Current = 246.6 ÷ 14.8

Current = 16.7A
```

Average flight current:

**≈16.7A**

---

# 7. Flight Time Calculation

Using usable battery energy:

```
Flight time = Usable energy ÷ Average power
```

```
Flight time = 59.2 ÷ 246.6

Flight time = 0.24 hours
```

Convert to minutes:

```
Flight time = 0.24 × 60

Flight time = 14.4 minutes
```

Therefore:

**Estimated endurance = 14.4 minutes**

---

# 8. Requirement Check

| Requirement | Result |
|---|---|
| Required endurance | >12 minutes |
| Calculated endurance | 14.4 minutes |
| Status | PASS |

The selected battery satisfies the endurance requirement.

---

# 9. Battery Current Capability Check

Battery maximum current capability:

```
Maximum current = Capacity × C rating

Maximum current = 5 × 30

Maximum current = 150A
```

Maximum propulsion current:

```
Motor current = 17.4 × 4

Motor current = 69.6A
```

Comparison:

```
Battery capability = 150A

Required current = 69.6A
```

Since:

```
150A > 69.6A
```

The battery can safely supply the required current.

---

# 10. Final Battery Selection

Selected battery:

**4S 5000mAh 30C LiPo**

Reasons:

- Compatible voltage with the motor system
- Provides more than 12 minutes endurance
- Enough current capability for all motors
- Suitable weight for the 2.5kg drone limit
- Commonly used with 10 inch quadcopters
