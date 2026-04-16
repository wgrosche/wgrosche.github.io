---
title: "AIrcraft"
excerpt: "Control for deformable, fixed-wing aircraft<br/><img src='/images/aircraft_trajectory.png'>"
collection: portfolio
category: research
---

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
