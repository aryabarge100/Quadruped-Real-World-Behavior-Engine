# System Overview
This project demonstrates a quadruped walking system developed in SOLIDWORKS using motion analysis, gait sequencing, terrain interaction, 
and load behavior analysis. The objective of the system is to simulate realistic quadruped walking while considering real-world conditions
such as load shifting, uneven terrain, instability, and control interaction.
The quadruped uses a crawl gait mechanism in which only one leg enters swing phase at a time while the remaining three legs support the body.
Motion sequencing was implemented using time-based motion control and rotary motors.

 # Design Specifications

Body Type-	Quadruped Walking Platform
Body Material	-Copper 
Terrain Type- Flat + Uneven Terrain
Motion Method-	Crawl Gait
Simulation Tool-	SOLIDWORKS Motion Analysis
Gait Type-	3-Leg Support Crawl Gait
Motion Control-	Rotary Motors + Path Motion
Terrain Features-	Slope + Pothole

# Phase 1 — Gait + Time-Based Motion

Crawl Gait Sequence

0–1 s=	Front Left
1–2 s=	Rear Right
2–3 s=	Front Right
3–4 s=	Rear Left

Motion Logic
The quadruped gait was implemented using:

Rotary motors attached to crank disks
Time sequencing in Motion Analysis
Data-point based displacement control
Sequential leg lifting

Each leg was controlled independently using:

Motion timelines
Rotary displacement
Time-varying angular motion
Gait Behavior

During each gait phase:

One leg enters swing phase
Remaining three legs create support polygon
Body slightly tilts toward support side
Load redistributes dynamically

# Phase 2 — Dynamic Load Shift + CoM Movement
Objective-To observe how load shifts during walking and determine which support legs carry maximum load.

Center of Mass Analysis
Mass Properties tool was used to observe CoM movement during different gait phases.

Initial CoM
Coordinate	Value
X	101.88 mm
Y	-1.47 mm
Z	74.36 mm

Shifted CoM During Terrain Interaction
Coordinate	Value
X	183.80 mm
Y	47.54 mm
Z	-4.63 mm

Load Redistribution Behavior
When one leg lifts:

Body tilts toward opposite support side
CoM shifts toward support polygon
Remaining legs carry redistributed load


During Front Left swing:
Rear Right support leg carries highest load
Body tilts toward right side
Maximum Load Leg Identification

# Phase 3 — Terrain Interaction + Instability
Objective-To evaluate quadruped behavior on uneven terrain.

The terrain included:

Uneven slope
Pothole/depression
Height variation
Observed Instability

During terrain traversal:

One side of body tilted downward
Leg support became uneven
Stability reduced near pothole edge
CoM shifted outside ideal support region
Instability Origin

Instability begins when:

Support polygon becomes narrow
One leg loses proper ground contact
CoM moves outside support triangle
First Component Under Stress

Primary stressed components:

Upper leg joints
Crank linkage
Support-side leg

These components experience increased load during imbalance.

# Phase 4 — Failure Propagation

 understand how failure propagates through the quadruped system.

1 Failure Case 1 — One Leg Failure
Sequence
Leg failure → support reduction → CoM shift → overload on remaining legs → body tilt → instability

2 Failure Case 2 — Joint Overload
Sequence

High terrain load → crank overload → excessive angular motion → linkage stress → gait instability

Observed Effects
Uneven posture
Increased tilt angle
Reduced stability
Support imbalance

# Phase 5 — Control Interaction Layer
Inputs
IMU Sensor

Measures:

tilt angle
acceleration
body orientation
Contact Sensors

Detect:

foot-ground contact
slip condition
terrain loss
Outputs

# Phase 6 — Reality Gap Analysis
Simulation Assumptions


In real-world conditions:

gait becomes unstable on irregular terrain
delayed motor response affects balance
slipping changes support polygon
payload inertia increases tilt risk


# Conclusion

This project successfully converted a quadruped assembly into a behavior-driven walking system capable of demonstrating realistic gait motion, 
load redistribution, terrain interaction, and instability analysis.
The system not only represents motion generation but also explains how the quadruped behaves under real-world conditions including imbalance,
uneven terrain, support reduction, and shifting center of mass.
