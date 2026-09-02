# Motor and Propeller Analysis

## Given Components

The propulsion system is based on:

Motor:

Holybro S500 V2 Motor 2216-920KV-CCW

Propeller:

1045 Propeller (10×4.5 inch)


---

# Design Requirement

The drone maximum allowed weight:

\[
2.5kg
\]

For a stable quadcopter design, a thrust-to-weight ratio of approximately 2:1 is targeted.

Required total thrust:

\[
2.5 \times 2
\]

\[
=5kg
\]

Therefore, each motor should provide:

\[
\frac{5}{4}
\]

\[
=1.25kg
\]

Minimum required thrust per motor:

\[
\boxed{1250g}
\]


---

# Motor Performance

The 2216-920KV motor with a 1045 propeller provides approximately:

Maximum thrust per motor:

\[
1367g
\]


Total available thrust:

\[
1367 \times 4
\]

\[
=5468g
\]


Total thrust:

\[
\boxed{5.47kg}
\]


---

# Thrust Margin

Required thrust:

\[
5kg
\]


Available thrust:

\[
5.47kg
\]


Margin:

\[
5.47-5
\]


\[
=0.47kg
\]


Thrust-to-weight ratio:

\[
\frac{5.47}{2.5}
\]


\[
=2.18:1
\]


Therefore, the selected motor and propeller combination satisfies the thrust requirement.


---

# Conclusion

The Holybro 2216-920KV motor with 1045 propellers is suitable for the 10 inch quadcopter because:

- It provides sufficient thrust margin
- It supports the required drone weight
- It is compatible with a 4S LiPo battery
- It is the recommended propulsion combination for the S500 V2 platform
