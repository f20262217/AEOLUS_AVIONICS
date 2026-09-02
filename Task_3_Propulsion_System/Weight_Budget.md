# Drone Weight Budget

## 1. Weight Requirement

The maximum allowed weight of the drone is:

**Maximum allowed weight = 2.5 kg**

The selected propulsion system, electronics, battery, and additional hardware must remain below this limit while maintaining sufficient payload capacity.

---

# 2. Estimated Component Weight

| Component | Quantity | Approximate Weight |
|---|---:|---:|
| S500 V2 Frame + Landing Gear | 1 | 300g |
| Holybro 2216-920KV Motors | 4 | 320g |
| 20A ESCs | 4 | 80g |
| 1045 Propellers | 4 | 40g |
| Pixhawk 6C Mini Flight Controller | 1 | 50g |
| GPS Module | 1 | 30g |
| Telemetry Module | 1 | 20g |
| RC Receiver | 1 | 5g |
| Power Module + Wiring | - | 80g |
| 4S 6750mAh 30C LiPo Battery | 1 | 730g |
| Miscellaneous Hardware | - | 100g |

---

# 3. Total Weight Calculation

The total estimated drone weight is calculated as:

```
Total weight = Frame + Motors + ESCs + Propellers + Electronics + Battery + Hardware
```

Substituting the values:

```
Total weight = 300 + 320 + 80 + 40 + 185 + 730 + 100

Total weight = 1755g
```

Therefore:

**Estimated drone weight = 1.76 kg**

---

# 4. Weight Limit Check

Maximum allowed weight:

```
2500g
```

Estimated drone weight:

```
1755g
```

Remaining payload capacity:

```
Payload margin = Maximum weight - Drone weight

Payload margin = 2500 - 1755

Payload margin = 745g
```

Therefore:

**Remaining payload capacity ≈ 745g**

The drone remains within the required 2.5kg weight limit.

---

# 5. Thrust-to-Weight Ratio Check

The selected motor and propeller combination provides:

**Total available thrust = 5.48 kg**

The drone weight is:

**1.76 kg**

The thrust-to-weight ratio is calculated as:

```
Thrust-to-weight ratio = Total thrust ÷ Drone weight

Thrust-to-weight ratio = 5.48 ÷ 1.755

Thrust-to-weight ratio = 3.12:1
```

---

# 6. Performance Evaluation

A thrust-to-weight ratio above 3:1 provides:

- Stable hovering
- Better maneuverability
- Ability to carry additional payload
- Improved performance during wind disturbances
- Safety margin during aggressive flight conditions

The selected propulsion system provides sufficient thrust for the drone while keeping the total weight significantly below the 2.5kg limit.

---

# 7. Final Weight Summary

| Parameter | Value |
|---|---:|
| Maximum Allowed Weight | 2.5 kg |
| Estimated Drone Weight | 1.76 kg |
| Remaining Payload Capacity | 745g |
| Total Available Thrust | 5.48 kg |
| Thrust-to-Weight Ratio | 3.12:1 |

---

# Conclusion

The proposed drone design satisfies the weight requirement.

The final build:

- Remains below the 2.5kg maximum limit
- Provides approximately 745g additional payload capacity
- Maintains a high thrust-to-weight ratio
- Supports autonomous payload integration in future upgrades
