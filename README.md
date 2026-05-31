# Carotid Artery Tortuosity and Turning Angle Analysis

This repository provides an automated pipeline for analyzing the geometric properties, tortuosity, and precise turning angles (kink points) of the Left Common Carotid Artery (LCCA) and Right Common Carotid Artery (RCCA). Using advanced medical image processing and skeletonization techniques, the project quantifies vascular dynamics to assist in clinical assessments of arterial kinking and tortuosity.
![Example]<img width="434" height="430" alt="image" src="https://github.com/user-attachments/assets/95320f4e-0156-4d79-a10b-bc719aa5e177" />


## Features

- **3D Skeletonization & Refinement**: Extraction of precise centerline coordinates from refined binary masks of vascular structures.
- **Vascular Coordinate Sorting**: Spatial sorting and Savitzky-Golay smoothing of discontinuous pixel arrays into ordered polylines using physical millimeter spacing.
- **Turning Angle Computation**: Implementation of localized segment vectors to compute explicit mathematical turning angles and angle differences (wrapped to (-pi, pi]) at specific regions of interest (ROI).
- **Kink Detection**: Automated estimation of incoming and outgoing arm directions around user-defined or peak-based tortuosity points to calculate the exact angle of vessel curvature.

## Visualizations

Below is the graphical representation of the detected vessels, centerlines, and calculated turning angles for the LCCA and RCCA regions:

![Carotid Artery Turning Angle Analysis]<img width="1389" height="761" alt="image" src="https://github.com/user-attachments/assets/c5668728-4f4d-47b9-b101-21bfd1283159" />


## Future Roadmap

- [x] Extract 3D centerlines using skeletonization and morphological filters (Remove Small Holes).
- [x] Implement coordinate sorting algorithms to convert pixel clusters into continuous physical paths.
- [x] Compute signed turning angles, segment lengths, and localized vector angles for specific arterial regions (LCCA/RCCA).
- [ ] Implement fully automated peak detection for kink points across entire 3D volumes without manual ROI initialization.
- [ ] Integrate 3D center-line tortuosity metrics such as Distance Metric (DM) and Inflection Count Metric (ICM).
- [ ] Build a robust batch-processing pipeline to evaluate large clinical datasets automatically.
- [ ] Export quantified geometric metrics into structured formats (CSV/JSON) for downstream statistical or machine learning analysis.
