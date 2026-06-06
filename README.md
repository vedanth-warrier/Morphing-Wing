# Morphing Wing Aerodynamic Prototype

Designed, fabricated, and tested a scale morphing wing prototype capable 
of dynamically altering its aerodynamic profile across simulated flight 
conditions.

## Overview

Traditional fixed-wing aircraft use discrete control surfaces that are 
aerodynamically suboptimal across different flight phases. This project 
developed a continuously morphing wing section using a compliant 
mechanism — eliminating traditional hinges in favour of elastic 
deformation of the structure itself.

**Key result:** ~13% improvement in lift-to-drag ratio (L/D from 5.00 
to 5.68) validated through wind tunnel testing.

## Design

- **Airfoil:** NACA 0012
- **Mechanism:** Chevron-based compliant structure — selected after 
  iterative testing of zig-zag and rectangular alternatives
- **Material:** PLA (3D printed) — chosen for balance of flexibility 
  and stiffness; acrylic laser-cut versions used for failure analysis 
  to identify stress concentration points
- **CAD & Simulation:** SolidWorks — stress simulation used to identify 
  and eliminate sharp-corner stress concentrations via filleting

![CAD Model](images/cad-model.png)

## Embedded Control System

- **Microcontroller:** Arduino Uno
- **Actuation:** 2x servo motors embedded in the leading-edge housing
- **Control:** Open-loop direct-mapping — potentiometer analog input 
  mapped to servo position via Arduino, enabling real-time wing profile 
  adaptation
- **Morphing range:** 43° angular displacement (10 cm linear), 
  exceeding the 7 cm design requirement

![Circuit Diagram](images/circuit-diagram.png)

## Wind Tunnel Testing

Three tests conducted at varying angles of attack and morphing 
configurations:

| Test | Angle of Attack | Morphing | Lift (mN) | Drag (mN) | L/D  |
|------|----------------|----------|-----------|-----------|------|
| 1    | 2°             | 10° down | 300       | 60        | 5.00 |
| 2    | 5°             | 10° down | 341       | 60        | 5.68 |
| 3    | 10°            | 20° down | 542       | 130       | 4.17 |

Tests 1→2 demonstrate that moderate morphing combined with increased 
angle of attack improves L/D without drag penalty. Test 3 shows the 
tradeoff — greater morphing increases lift but induces drag, reducing 
L/D. This highlights the importance of morphing strategy optimisation 
for each flight phase.

![Wind Tunnel Setup](images/wind-tunnel.png)

## Skills Demonstrated

- SolidWorks CAD and stress simulation
- Compliant mechanism design and iterative prototyping
- 3D printing and laser cutting
- Embedded systems (Arduino Uno, C/C++)
- Aerodynamic testing and data analysis
