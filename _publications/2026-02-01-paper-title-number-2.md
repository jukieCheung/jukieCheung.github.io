---
title: "Med-PU: Point Cloud Upsampling for High-Fidelity 3D Medical Shape Reconstruction"
collection: publications
category: conferences
#permalink: 'https://doi.org/10.1007/978-3-031-44213-1_29'
excerpt: ' PUSSM: Point Cloud Upsampling for Medical Shape Reconstruction.'
date: 2026-01-29
venue: '2025 IEEE International Conference on Bioinformatics and Biomedicine (BIBM)'
paperurl: 'https://ieeexplore.ieee.org/document/11356411'
#citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---

High-fidelity 3D anatomical reconstruction is essential for clinical applications, yet converting voxel-based segmentation into smooth and watertight meshes remains challenging due to noise, incompleteness, and shape variability. We propose Med-PU, a knowledge-driven framework that integrates volumetric segmentation with deep point cloud upsampling to reconstruct high-quality anatomical surfaces. Instead of manual landmarking or PCA-based statistical models, Med-PU learns an implicit anatomical prior from large-scale 3D medical shapes, enabling dense and topology-consistent reconstruction from sparse segmentation outputs. Experiments on pelvic CT datasets (Med-ShapePelvic for training and Pelvic1k for validation) show that Med-PU consistently improves geometric accuracy and surface fidelity over state-of-the-art upsampling methods, demonstrating robustness across input densities and potential generalization to other anatomical regions.
![PUSSM](/images/publications/PUSSM_math.png)

