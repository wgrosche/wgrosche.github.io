---
title: "MultiCam-GT"
excerpt: "Multi-view annotation pipeline<br/><img src='/images/multicam-gt.png'>"
collection: portfolio
category: research
---

## Overview

Annotation pipeline for multi-view people tracking datasets, used in the construction of the public [SCOUT dataset](https://scout.epfl.ch/). Automated tracklet merging reduced manual annotation time by ~90%. (8 months)

## Problem

Annotating multi-view pedestrian detection datasets with contiguous overlapping fields of view across 25 cameras requires spatially consistent labelling, temporal coherence of tracks at ~10-minute timescales, and efficient tooling to make the annotation volume tractable.

## Features

- **Multi-view annotation**: Web-based tool for spatially-aware annotation with cross-view consistency across 25 cameras
- **Automated tracklet merging**: Proximity-based tracklet merging and cross-view correspondence to minimise manual effort
- **Trajectory analysis**: Support for trajectory analysis at ~10-minute timescales
- **Elevation modelling**: Mesh-based ground plane representation for varying terrain
- **Database integration**: All transformation and tracking data stored in PostgreSQL

## Technical Details

Built with Django and PostgreSQL on the backend, with a JavaScript frontend for interactive annotation. The automated tracklet merging pipeline was the key contribution, reducing the manual annotation burden by approximately 90% and making the construction of the SCOUT dataset feasible.

## Links

- [GitHub Repository](https://github.com/cvlab-epfl/multicam-gt)
- [SCOUT Dataset](https://scout.epfl.ch/)
