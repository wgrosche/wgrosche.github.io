---
title: "MultiCam-GT"
excerpt: "Multi-camera annotation webapp<br/><img src='/images/multicam-gt.png'>"
collection: portfolio
category: research
---

## Overview

Updated version of the EPFL MultiCam-GT Tool — a multi-view object annotation webapp for pedestrian detection datasets.

## Problem

Creating ground-truth annotations for multi-camera pedestrian detection datasets requires spatially consistent labelling across views, accounting for varying terrain elevation and maintaining temporal coherence of object tracks.

## Features

- **Elevation modelling**: Mesh-based ground plane representation to handle varying terrain, improving annotation accuracy in non-flat environments
- **Object transformation**: Full 3D object representation using dimensions and spatial orientation
- **Tracklet merging**: Functionality for combining fragmented tracklets into coherent object tracks
- **Trajectory visualisation**: Tools for visualising and analysing object movement patterns across camera views
- **Database integration**: All transformation and tracking data stored in PostgreSQL for efficient data management and retrieval

## Technical Details

Built with Django and PostgreSQL on the backend, with a JavaScript frontend for interactive annotation. The tool processes multi-camera setups and provides a web interface for spatially-aware annotation with real-time cross-view consistency.

## Links

- [GitHub Repository](https://github.com/cvlab-epfl/multicam-gt)
