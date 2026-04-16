---
title: "AIrcraft"
excerpt: "Control for deformable, fixed-wing aircraft<br/><img src='/images/aircraft_trajectory.png'>"
collection: portfolio
category: research
---

<<<<<<< Updated upstream

As part of my work at EPFL I am working on control policies for fixed wing drones with a goal of extending to deformable wings and/or shape optimisation of the aircraft. This page is a summary of that work, the problems I have faced and my solutions to those problems. The repository belonging to this work is available [here](https://github.com/wgrosche/AIrcraft).

Problem Definition
===

Variables


State
===

- Position $\vec{p}_{I} \in \mathbb{R}^3$ Inertial Position
- Velocity $\vec{v_{I}} \in \mathbb{R}^3$ 
- Orientation $q_{B}^{I} \in SU(2)$
- Angular Velocity $\vec{\omega_{B}^{I}} \in \mathbb{R}^3$


Reference Frames
------

We are working with a 6 degree of freedom (6DOF) model, these being the position and orientation of the aircraft. 

We define two reference frames, an inertial $R_I = NED$ and a body frame $R_B = FRD$. Both frames are right handed and denoted NED (North-East-Down) and FRD (Front-Right-Down) in accordance with their axis orientations. 

Conversions between reference frames are performed: $v_{I} = q_{B}^{I} (v_{B}^T, 0)^T \left(q_{B}^{I}\right)^{-1}$

This model makes the simplifying assumption of a non-rotating earth. Extension to this introduces the coriolis force but is not otherwise a problem. We disregard it here as it is not relevant to the problem at hand.

Useful Additions
------

- Relative Airspeed
- Dynamic Pressure
- Angle of Attack: $\alpha = \arctan \left(\frac{v_{B}^{I} \cdot e_{B}^{Z}}{v_{B}^{I} \cdot e_{B}^{X}}\right)$
- Angle of Sideslip
- Angle of Roll
    - Derivative of Angle of Roll
- Angle of Pitch
    - Derivative of Angle of Pitch
- Angle of Yaw
    - Derivative of Angle of Yaw


Controls
===

Surfaces
-----

- Aileron
- Elevator
- Rudder

Power
-----

- Thrust

Problem Extensions
-----

- External Wind
- Rotating Earth

Dynamics
===

Intertia Tensor and Mass
-----

Aerodynamics
-----


Forces and Moments
-----

Damping
-----


The system as described above, derived from purely static simulations displays unstable behaviour
=======
## Overview

Minimum-time control for deformable, fixed-wing aircraft using neural network surrogate dynamics models.

## Problem

Controlling deformable aircraft presents challenges beyond rigid-body flight dynamics. The deformation of the wing structure couples with aerodynamic forces, creating a high-dimensional, nonlinear control problem where traditional model-based approaches become impractical.

## Approach

- **Surrogate dynamics**: Neural network models trained on simulation data to approximate the full deformable-body dynamics at a fraction of the computational cost
- **Minimum-time control**: Optimisation of control trajectories to achieve target states in minimum time, leveraging the differentiable surrogate model
- **Coordinate framework**: Rigorous treatment of inertial, body, and wind reference frames with quaternion-based attitude representation

## Technical Details

The project involves defining the full state space (position, orientation via quaternions, angular velocity), establishing coordinate transformations between reference frames, and training neural networks to serve as fast surrogates for the underlying physics simulation.

For technical deep-dives into the coordinate conventions, state definitions, and frame transformations, see the [Technical Notes series](/notes/).

## Links

- [GitHub Repository](https://github.com/wgrosche/AIrcraft)
>>>>>>> Stashed changes
