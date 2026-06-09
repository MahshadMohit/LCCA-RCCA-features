# Carotid Artery Tortuosity and Turning Angle Analysis

This repository provides an automated pipeline for analyzing the geometric properties, tortuosity, and precise turning angles (kink points) of the Left Common Carotid Artery (LCCA) and Right Common Carotid Artery (RCCA). Using advanced medical image processing and skeletonization techniques, the project quantifies vascular dynamics to assist in clinical assessments of arterial kinking and tortuosity.

<p align="center">
  <img src="https://github.com/user-attachments/assets/95320f4e-0156-4d79-a10b-bc719aa5e177" width="300"/>
</p>

---

## Features

- **3D Skeletonization & Refinement**: Extraction of precise centerline coordinates from refined binary masks of vascular structures.
- **Vascular Coordinate Sorting**: Spatial sorting and Savitzky-Golay smoothing of discontinuous pixel arrays into ordered polylines using physical millimeter spacing.
- **Turning Angle Computation**: Implementation of localized segment vectors to compute explicit mathematical turning angles and angle differences (wrapped to (-pi, pi]) at specific regions of interest (ROI).
- **Kink Detection**: Automated estimation of incoming and outgoing arm directions around user-defined or peak-based tortuosity points to calculate the exact angle of vessel curvature.

---

## Visualizations

Below is the graphical representation of the detected vessels, centerlines, and calculated turning angles for the LCCA and RCCA regions:

<p align="center">
  <img src="https://github.com/user-attachments/assets/c5668728-4f4d-47b9-b101-21bfd1283159" width="500"/>
</p>

<p align="center">
  <b>Figure 1.</b> Turning angle analysis and centerline extraction for carotid artery segments.
</p>

### Measuring the RL of Both Arteries

<p align="center">
  <img src="https://github.com/user-attachments/assets/c432ec7f-6f2f-447e-a615-c7ff918e491a" height="400"/>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/4c8c0fd5-82d6-41f8-b861-f70699d8b0f6" height="400"/>
</p>

<p align="center">
  <b>Figure 2.</b> RL measurements for the left and right common carotid arteries.
</p>
