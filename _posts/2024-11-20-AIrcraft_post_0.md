---
title: 'A record of my work on data driven control: Coordinate Conventions'
date: 2024-11-20
permalink: /posts/2024/11/AIrcraft_post_0/
tags:
  - control
  - AIrcraft
---

AIrcraft
===
This is the first in a series of posts about the data driven control of an aircraft. This post will be about coordinate conventions.

Coordinate Systems
------
There are many coordinate systems used in aerospace engineering. The most common ones are the inertial frame, the body frame, and the wind (or stability) frame. In the further work of this project I will assume the inertial frame to be defined relative to a stationary point on the surface of the earth. I will align the x-direction with north, the y-direction with east, and the z-direction with the gravity vector. I neglect the effects of the earth's rotation and curvature due to the small size of the aircraft and the short time scales and distances of the flight.

The body frame is centered at the centre of mass of the aircraft, the x-axis of the body frame runs through the nose of the aircraft, the y-axis runs through the right wing, and the z-axis is perpendicular to these in a right-handed manner (pointing down).

The stability frame is rotated relative to the body frame around the y-axis by the angle of attack. This coordinate frame is often used to treat aerodynamic forces and moments. This frame is not currently used in this project as the forces are calculated directly in the body frame.

Coordinate transformations between these frames will be addressed following the definition of the state vector.