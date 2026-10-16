# Depth-Supervised 3D Gaussian Splatting

**3D Reconstruction · Confidence-Weighted Depth Supervision · Geometric Consistency**  
*Research Project | Field Robotics Laboratory, Kyoto University*

## Project Overview

3D Gaussian Splatting (3DGS) enables photorealistic, efficient novel-view rendering, but visual quality does not guarantee reliable geometry. I explored **confidence-weighted D435 depth supervision** to improve agreement with measured depth while preserving rendering quality.

## 1. Background and Motivation

Point clouds, meshes, and voxels have different trade-offs in surface representation and efficiency. 3DGS produces visually detailed scenes using explicit Gaussians, yet RGB-only photometric optimization may leave depth and surface geometry inaccurate.

### Photometric Optimization — L1 and SSIM

Standard 3DGS combines pixel-wise **L1 loss** and local **SSIM**. In the illustration, white boxes indicate L1 pixel comparison regions, while green markings highlight local structural comparison for SSIM. Neither loss directly guarantees metric geometry.

<p align="center">
  <img src="images/photometric-inconsistency.png" alt="Illustration of view-dependent appearance inconsistency" width="78%">
</p>

<p align="center"><em>Illustration of L1 (white) and SSIM (green) photometric supervision.</em></p>

<p align="center">
  <img src="images/gaussian-artifacts.png" alt="Illustration of Gaussian reconstruction artifacts" width="72%">
</p>

<p align="center"><em>Illustrative Gaussian artifacts; not a quantitative overfitting experiment.</em></p>

## 2. Reconstruction Pipeline

The workflow uses RGB images, calibrated **Intel RealSense D435** depth, and COLMAP-initialized camera poses. Because monocular SfM has an arbitrary scale, **metric scale recovery** is necessary before comparing rendered depth with D435 depth in meters.

<p align="center">
  <img src="images/depth-supervised-pipeline.png" alt="Depth-supervised 3DGS workflow" width="82%">
</p>

<p align="center"><em>Overall RGB-D and depth-supervision pipeline.</em></p>

### Depth Mask and Confidence

Invalid depth pixels are filtered out. Valid observations receive confidence weights based on **edges, texture, depth gradients, and distance**.

<p align="center">
  <img src="images/depth-valid-mask.png" alt="RGB input, filtered depth, and valid-pixel mask" width="78%">
</p>

<p align="center"><em>RGB input, D435 depth, and valid-depth mask.</em></p>

<p align="center">
  <img src="images/single-view-confidence.png" alt="Edge, texture, depth-gradient, and distance confidence" width="82%">
</p>

<p align="center"><em>Single-view reliability cues.</em></p>

Single-view confidence (V7) is combined with multi-view geometric consistency (V8): **Final Confidence = V7 × V8**.

<p align="center">
  <img src="images/multi-view-confidence.png" alt="Single-view confidence, multi-view confidence, and coverage support" width="82%">
</p>

<p align="center"><em>Single-view confidence, multi-view confidence, and support coverage.</em></p>

<p align="center">
  <img src="images/final-confidence.png" alt="Final confidence map" width="46%">
</p>

<p align="center"><em>Final confidence map used to weight the depth constraint.</em></p>

## 3. Scale Recovery and Visual Demonstrations

Scale recovery puts COLMAP/3DGS depth and D435 observations into a common **metric scale** for depth supervision and evaluation.

<p align="center">
  <img src="images/scale-recovery-comparison.png" alt="Rendering views before and after scale recovery" width="84%">
</p>

<p align="center"><em>Views before and after scale recovery; this is not a depth-supervision ablation.</em></p>

**RGB-only:** [Watch reconstruction video](videos/rgb-only.mp4)  
**Depth-supervised:** [Watch reconstruction video](videos/depth-supervised.mp4)

## 4. Rendering Quality Evaluation

<p align="center">
  <img src="images/rendering-metrics.png" alt="Rendering-quality metrics" width="62%">
</p>

<p align="center"><em>PSNR, SSIM, and LPIPS over training iterations.</em></p>

At 30k steps, depth supervision preserved **comparable rendering quality** (PSNR 28.660 → 28.628 dB; SSIM 0.8414 → 0.8418).

## 5. Depth Consistency Evaluation

Rendered depth from both models was compared against **D435 observed depth**, using RMSE (meters; lower is better).

<p align="center">
  <img src="images/depth-rmse-results.png" alt="Depth RMSE across three evaluation ranges" width="62%">
</p>

<p align="center"><em>Depth RMSE relative to D435 measurements; improvement decreases with distance. This demonstrates **sensor-depth consistency**, not independent ground-truth 3D accuracy.</em></p>

## 6. Future Work — SLAM-Based Initialization

I am extending the workflow toward **LiDAR–Inertial–Visual Odometry (LIVO)**, aiming to replace offline COLMAP initialization with continuous metric camera poses and LiDAR geometry for future 3DGS mapping.

<p align="center">
  <img src="images/future-livo-3dgs-pipeline.png" alt="Proposed LIVO-to-3DGS pipeline" width="84%">
</p>

<p align="center"><em>Planned SLAM-based initialization for 3DGS; ongoing work.</em></p>
