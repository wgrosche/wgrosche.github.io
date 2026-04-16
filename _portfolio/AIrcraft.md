---
title: "AIrcraft"
excerpt: "Time-optimal MPC for fixed-wing drones<br/><img src='/images/aircraft_trajectory.png'>"
collection: portfolio
category: research
---

## Overview

Time-optimal Model Predictive Control and trajectory optimisation for a fixed-wing drone targeting the F5B competition (up to 100 m/s, ~50 laps of 300 m in 3 min). Collaboration with the Swiss Joint Research Centre. (2.5 years)

## Problem

The F5B competition demands precise, time-optimal control of an unmotorised fixed-wing aircraft at extreme speeds. Traditional aerodynamic force evaluation via CFD takes ~8 hours per evaluation, making it impractical for real-time control or trajectory optimisation loops.

## Approach

- **Differentiable surrogate model**: Built a differentiable aerodynamic surrogate integrating wind tunnel data, CFD results, and first-principles physical models, reducing force evaluation from ~8 hours (CFD) to ~1 ms
- **Time-optimal MPC**: Developed trajectory optimisation and time-optimal MPC using CasADi to interface with the Ipopt solver
- **Aerodynamic system identification**: Combined data from wind tunnel, CFD, and in-flight measurements to identify the aerodynamic model
- **Angular-rate correction**: Independently derived an angular-rate correction to account for dynamic effects absent in static CFD, resolving time-integration instability in trajectory rollout

## Technical Details

The system performs 6DOF aerodynamics simulation with full state representation (position, quaternion orientation, angular velocity). The differentiable surrogate enables gradient-based optimisation through the dynamics, making real-time MPC feasible at competition speeds.

For technical deep-dives into the coordinate conventions, state definitions, and frame transformations, see the [Technical Notes series](/notes/).

## Links

- [GitHub Repository](https://github.com/wgrosche/AIrcraft)
