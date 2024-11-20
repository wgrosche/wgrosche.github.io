---
title: 'A record of my work on data driven control: State definition'
date: 2024-11-20
permalink: /posts/2024/11/AIrcraft_post_1/
tags:
  - control
  - AIrcraft
---

AIrcraft
===
This post will be about the state definition.

State
------

Taken from the book "Aircraft Control and Simulation" by Stevens and Lewis, the state is defined as:
$$
\begin{bmatrix}
\vec{x}_i \\
\vec{v}_i \\
\bar{q}_i^b \\
\vec{\omega}_b
\end{bmatrix}
$$

Where $\vec{x}_i$ is the position of the aircraft in the inertial frame, $\vec{v}_i$ is the velocity of the aircraft in the inertial frame, $\bar{q}_i^b$ is the attitude of the aircraft in the inertial frame, and $\vec{\omega}_b$ is the angular velocity of the aircraft in the body frame.
