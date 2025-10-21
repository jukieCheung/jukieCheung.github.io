---
title: "Rethinking data input for point cloud upsampling"
collection: publications
category: conferences
#permalink: 'https://doi.org/10.1007/978-3-031-44213-1_29'
excerpt: ' This paper is the preliminary work and experimental report of ReLPU.'
date: 2025-08-28
venue: '17th International Conference on Machine Learning and Computing'
paperurl: '[https://doi.org/10.1007/978-3-031-44213-1_29](https://doi.org/10.1007/978-3-031-94898-5_3)'
#citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---

Point cloud upsampling is crucial for tasks like 3D reconstruction. While existing methods rely on patch-based inputs, and there is no research discussing the differences and principles between point cloud model full input and patch based input. Ergo, we propose a novel approach using whole model inputs i.e. Average Segment input. Our experiments on PU1K and ABC datasets reveal that patch-based inputs consistently outperform whole model inputs. To understand this, we will delve into factors in feature extraction, and network architecture that influence upsampling results.
