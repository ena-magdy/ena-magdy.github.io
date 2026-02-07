---
title: Design and Analysis of a Cold Gas Rocket Engine
date: 2026-01-01 13:32:20 +0300
categories: [Propulsion, Rocket-Engines]
tags: [rocket, propulsion, gas-dynamics]
math: true
image: /assets/img/Projects/Rocket/Flowchart.png
media_subpath: /assets/img/Projects/Rocket/
---

## Abstract

Cold gas propulsion systems are widely used in small spacecraft and attitude control applications due to their simplicity, reliability, and safety. This project focuses on the **design, analysis, and simulation of a cold gas rocket engine**, covering thermodynamic modeling, nozzle design, thrust estimation, and MATLAB-based performance simulation.

---

## System Overview

A cold gas rocket engine operates by expanding a stored pressurized gas through a converging–diverging nozzle to generate thrust. Unlike chemical propulsion, no combustion occurs, making the system ideal for precise control maneuvers.

![Rocket Diagram](/assets/img/Projects/Rocket/RocketDiagram.png){: .shadow w="85%" }

---

## Design Flowchart

The following flowchart illustrates the overall design and analysis workflow:

![Flowchart](/assets/img/Projects/Rocket/Flowchart.png){: .shadow w="85%" }

---

## Governing Equations

### 1. Mass Flow Rate

The mass flow rate through a choked nozzle is given by:


\[
\dot{m} = A_t P_0 \sqrt{ \frac{\gamma}{R T_0} }
\left( \frac{2}{\gamma + 1} \right)^{\frac{\gamma + 1}{2(\gamma - 1)}}
\]

Where:
- \( A_t \) : Throat area  
- \( P_0 \) : Chamber pressure  
- \( T_0 \) : Chamber temperature  
- \( \gamma \) : Specific heat ratio  
- \( R \) : Gas constant  

---

### 2. Exit Velocity

\[
V_e = \sqrt{
\frac{2 \gamma}{\gamma - 1} R T_0
\left( 1 - \left( \frac{P_e}{P_0} \right)^{\frac{\gamma - 1}{\gamma}} \right)
}
\]

---

### 3. Thrust Equation

\[
F = \dot{m} V_e + (P_e - P_a) A_e
\]

Where:
- \( P_e \) : Exit pressure  
- \( P_a \) : Ambient pressure  
- \( A_e \) : Exit area  

---

## Nozzle Design

The nozzle was designed as a **converging–diverging (De Laval) nozzle** to ensure choked flow at the throat and supersonic expansion at the exit.

Key design parameters:
- Expansion ratio
- Throat diameter
- Exit Mach number

---

## MATLAB Simulation

A MATLAB script was developed to:
- Compute thrust vs chamber pressure
- Analyze mass flow rate variation
- Evaluate nozzle performance

![MATLAB Results](/assets/img/Projects/Rocket/MatlabRocket.png){: .shadow w="85%" }

---

## Results and Discussion

The simulation results show that:
- Thrust increases linearly with chamber pressure
- Cold gas systems produce relatively low thrust
- Efficiency is strongly affected by nozzle expansion ratio

Despite the low thrust, the system offers **high reliability and precise controllability**, making it suitable for attitude control systems (ACS).

---

## Conclusion

This project successfully demonstrated the complete design and analysis cycle of a cold gas rocket engine. The analytical model was validated through simulation, and the results align with expected theoretical behavior. Future work may include experimental validation or optimization for different propellants.

---

## References

1. Sutton, G. P., & Biblarz, O. *Rocket Propulsion Elements*
2. Humble, R. W., Henry, G. N., & Larson, W. J. *Space Propulsion Analysis and Design*
3. NASA Glenn Research Center – Cold Gas Propulsion Systems
