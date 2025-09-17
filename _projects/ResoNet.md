---
title: Physics Informed Off-Resonance Correction
description: |
  <span style="text-align: justify; display: block;">
    Our research focuses on a physics-informed deep learning framework that corrects off-resonance artifacts in non-Cartesian MRI trajectories by training exclusively on synthetic noise-like data, enabling efficient spiral imaging without the blurring effects caused by magnetic field inhomogeneities.
  </span>
people:
  - Alfredo De Goyeneche
  - Shreya Ramachandran
  - Ke Wang
  - Michael (Miki) Lustig
layout: project
category: Advanced Reconstruction Methods
images:
  - "/images/publications/Off_resonet.png"
  - "/images/research/Resonet_1.png"
last-updated: 2025-09-03
---

<p style="text-align: justify;">
Magnetic Resonance Imaging (MRI) is a powerful medical imaging modality that offers diagnostic information without harmful ionizing radiation. Unlike optical imaging, MRI sequentially samples the spatial Fourier domain (k-space) of the image through multiple shots with smooth trajectory sampling. Conventional MRI data acquisition relies on slow, inefficient row-by-row k-space sampling, while more efficient non-Cartesian trajectories like spirals use longer readout intervals but are susceptible to magnetic field inhomogeneities that cause off-resonance artifacts. Spiral trajectories create off-resonance blurring where magnetic field variation corresponds to depth and readout duration to aperture size, similar to optical blurring. We present a physics-informed deep learning framework for off-resonance correction that trains exclusively on synthetic, noise-like data with representative marginal statistics. Our approach enables fat/water separation and parallel imaging acceleration through end-to-end training using synthetic randomized data (noise-like images, coil sensitivities, field maps), allowing the network to reverse off-resonance effects across diverse anatomies and contrasts without retraining. This work has the potential to facilitate clinical adoption of non-Cartesian sampling trajectories, enabling efficient, rapid, and motion-robust MRI scans.</p>


## Key Contributions

- **Synthetic data training**: Training the network end-to-end using exclusively synthetic, noise-like data with randomized field maps, coil sensitivities, fat/water partial volumes, and noise, eliminating the need for large real MRI datasets
- **Physics-informed forward model**: Developing a multi-frequency bin forward model that represents a resonance spectrum per voxel, enabling accurate handling of off-resonance and partial volume effects
- **Fat/water separation**: Enabling explicit separation of fat and water signals within each voxel, while also producing combined artifact-corrected images
- **Generalizability across anatomies**: Demonstrating robust correction of off-resonance artifacts on phantom, brain, knee, and abdominal in-vivo data, without retraining for specific anatomies or contrasts
- **Trajectory compatibility**: Showing applicability to Spiral acquisitions and extensibility to other non-Cartesian trajectories, supporting efficient and motion-robust MRI scans