# Engineering Documentation: Actuator Disk Momentum Theory
## Mathematical Foundations and Aerodynamic Formulation for Distributed Propulsive Matrices
**Author:** Juho Artturi Hemminki
**License:** Apache License, Version 2.0
**Configuration:** Application to 18-Engine Coaxial Distributed Core Matrix (9 x Twin-Supercharged HEMI V12 per Wing)

---

## 1. Legal Notice and License

Copyright 2026 Juho Artturi Hemminki

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://apache.org

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

---

## 2. Executive Summary

This engineering document provides the summarized mathematical, thermodynamic, and fluid dynamic framework for the **Actuator Disk Momentum Theory** (Rankine-Froude Momentum Theory) as applied to the **Boeing 737 NFOF-HEMI V12 Edition**, replacing conventional turbofans with a high-solidity Distributed Propulsion (DP) matrix of 18 twin-supercharged reciprocating engines. For the complete, unabridged derivation, equations, and numerical validations, please refer to the full documentation under the Apache 2.0 license.

---

## 3. Core Principles and Governing Relations

The Rankine-Froude model abstracts individual blade geometries into an infinitely thin, homogeneous force-generating disk under incompressible, one-dimensional, and inviscid flow assumptions.

### 3.1. Continuity and Momentum
Across the upstream (0), disk (s), and downstream wake (3) stations, the mass flow rate is:
$$\dot{m} = \rho A_0 V_0 = \rho A_s V_s = \rho A_3 V_3$$
The net thrust $T$ relates to the momentum change in the streamtube:
$$T = \dot{m}(V_3 - V_0) = A_s(P_2 - P_1) = A_s \Delta P$$

### 3.2. Induced Velocity and Bernoulli's Principle
By applying Bernoulli's energy equation across the upstream and downstream control volumes, the local velocity at the disk $V_s$ is proven to be the arithmetic mean of free-stream and far-wake velocities:
$$V_s = \frac{V_0 + V_3}{2} = V_0 + v$$
where $v$ is the axial induced velocity, yielding a far-field wake velocity $V_3 = V_0 + 2v$.

### 3.3. Propulsive Efficiency
The ideal Froude propulsive efficiency $\eta_p$ is defined by:
$$\eta_p = \frac{V_0}{V_0 + v} = \frac{2 V_0}{V_0 + V_3}$$
Scaling this across the 18-engine matrix ($\sum T_{idx} \approx 312.4\text{ kN}$ static thrust, and $44.19\text{ kW}$ per engine at cruise altitude) ensures reduced induced losses and optimized high-altitude performance.

---

**Author: Juho Artturi Hemminki**
