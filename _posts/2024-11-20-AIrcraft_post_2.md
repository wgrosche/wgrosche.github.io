---
title: 'A record of my work on data driven control: Coordinate Transformations'
date: 2024-11-20
permalink: /posts/2024/11/AIrcraft_post_2/
tags:
  - control
  - AIrcraft
---

AIrcraft
===
In this post I will be discussing the coordinate transformations between the inertial frame, the body frame, and the wind (or stability) frame.

Body to Inertial
------

The conversion from the body frame to the inertial frame is done using the following transformation:
$$
\vec{v}_i = q_i^b \otimes \vec{v}_b \otimes q_b^i
$$
 whereby  $\otimes$ is the quaternion multiplication and $q_b^i = (q_i^b)^{-1}$ is the attitude quaternion that represents the rotation from the inertial frame to the body frame.