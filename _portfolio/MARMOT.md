---
title: "MARMOT"
excerpt: "Multi-view camera localisation and tracking<br/><img src='/images/marmotsample.png'>"
collection: portfolio
category: research
---

## Overview

Multi-camera localisation, calibration, and ground-plane pedestrian tracking system with automated axis-alignment. (1 year)

## Problem

Deploying a multi-view tracking system requires robust camera localisation and calibration that can recover reliable world-frame geometry — including consistent axis orientation — from diverse camera setups with minimal manual intervention.

## Approach

- **Camera localisation and calibration**: Led development of a multi-camera localisation and calibration suite for the multi-view tracking system
- **Automated axis-alignment**: Developed an automated axis-alignment method for OpenSFM reconstructions using RANSAC plane fitting on keypoint-dense regions combined with camera height priors to recover z-axis orientation
- **Ground-plane tracking**: Adapted ByteTrack and YOLOX for ground-plane operation by projecting detections onto the floor to enable meaningful cross-view correspondence

## Technical Details

The system handles the full pipeline from raw multi-camera video to calibrated camera models and ground-plane pedestrian trajectories. The RANSAC-based axis alignment removes the need for manual ground-plane annotation, and the projected-detection approach enables robust cross-view association for tracking.

## Links

- [GitHub Repository](https://github.com/cvlab-epfl/MARMOT)
