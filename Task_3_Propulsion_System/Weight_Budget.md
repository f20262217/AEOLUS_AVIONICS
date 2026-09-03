# Drone Weight Budget

## 1. Weight Requirement

The maximum allowed weight of the drone is:

**Maximum allowed weight = 2.5 kg**

The selected propulsion system, electronics, battery, autonomous hardware, and communication equipment must remain below this limit while maintaining sufficient payload capacity.

---

# 2. Estimated Component Weight

| Component | Quantity | Approximate Weight |
|-|-:|-:|
| S500 V2 Frame + Landing Gear | 1 | 300g |
| Holybro 2216-920KV Motors | 4 | 320g |
| 25A ESCs | 4 | 100g |
| 1045 Propellers | 4 | 40g |
| Pixhawk 6C Mini Flight Controller | 1 | 50g |
| GPS Module | 1 | 30g |
| Telemetry Module | 1 | 20g |
| RC Receiver | 1 | 5g |
| Power Module + Wiring | - | 80g |
| 4S 6750mAh 30C LiPo Battery | 1 | 730g |
| Autonomous Processing Stack (Jetson Orin Nano + RealSense D435i + SD Card + Regulator) | 1 | 187g |
| DJI O3 Air Unit Video System | 1 | 35g |
| Miscellaneous Hardware | - | 100g |

---

# 3. Total Weight Calculation

The total estimated drone weight is calculated as:

Total weight = Base drone system + Autonomous stack + Video system

The base drone weight from propulsion and core electronics:

Base drone weight = 1755g

Adding the additional systems:

Total weight = 1755 + 187 + 35

Total weight = 1977g


Therefore:

**Estimated final drone weight ≈ 1.98 kg**

---

# 4. Weight Limit Check

Maximum allowed weight: 2500g


Estimated final drone weight: 1977g


Remaining payload capacity:

Payload margin = Maximum weight - Drone weight

Payload margin = 2500 - 1977

Payload margin = 523g

Therefore:

**Remaining payload capacity ≈ 520g**

The complete drone configuration remains within the required 2.5kg weight limit.

---

# 5. Thrust-to-Weight Ratio Check

The selected motor and propeller combination provides:

**Maximum thrust per motor = 1.37kg**

For four motors:

Total thrust = 1.37 × 4
Total thrust = 5.48kg

The final drone weight is = 1.977kg

The thrust-to-weight ratio is = Total thrust ÷ Drone weight

Thrust-to-weight ratio = 5.48 ÷ 1.977

Thrust-to-weight ratio = 2.77:1

---

# 6. Performance Evaluation

A thrust-to-weight ratio above 2:1 provides:

- Stable hovering capability
- Good maneuverability
- Ability to carry additional payload
- Improved performance during wind disturbances
- Adequate safety margin during flight

The updated drone configuration maintains sufficient thrust even after integrating the autonomous computing and video transmission systems.

---

# 7. Final Weight Summary

| Parameter | Value |
|-|-:|
| Maximum Allowed Weight | 2.5 kg |
| Estimated Final Drone Weight | 1.98 kg |
| Remaining Payload Capacity | 520g |
| Total Available Thrust | 5.48 kg |
| Thrust-to-Weight Ratio | 2.77:1 |

---

# Conclusion

The proposed drone design satisfies the weight requirement.

The final integrated build:

- Remains below the 2.5kg maximum limit
- Provides approximately 520g additional payload capacity
- Maintains sufficient thrust-to-weight ratio
- Supports autonomous processing using Jetson Orin Nano and RealSense D435i
- Includes video transmission capability through the DJI O3 Air Unit
