---
title: "MARMOT"
excerpt: "Multi-View people tracking<br/><img src='/images/marmotsample.png'>"
collection: portfolio
category: research
---

## Overview

Multi-view pedestrian tracking in the ground plane, with automated camera calibration and ground plane estimation via structure from motion.

## Problem

Tracking people across multiple camera views requires solving several interconnected problems: calibrating cameras with potentially varying intrinsic and extrinsic parameters, establishing a common ground plane, and associating detections across views to produce consistent tracks.

## Approach

- **Camera calibration**: Automated intrinsic and extrinsic calibration for multi-camera setups
- **Ground plane estimation**: Structure from motion to establish a shared ground plane across views
- **Multi-view tracking**: Pedestrian detection and tracking projected into the ground plane, fusing information from all available camera views

## Technical Details

The pipeline takes raw multi-camera video feeds and produces calibrated camera models and ground-plane pedestrian trajectories. The structure-from-motion component handles the geometric setup, while the tracking module operates in the estimated ground plane for robust multi-view association.

## Links

- [GitHub Repository](https://github.com/cvlab-epfl/MARMOT)
