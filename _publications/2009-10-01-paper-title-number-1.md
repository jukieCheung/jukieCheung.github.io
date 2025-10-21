---
title: "Representation learning of point cloud upsampling in global and local inputs"
collection: publications
category: manuscripts
#permalink: 'https://doi.org/10.1016/j.cviu.2025.104467'
excerpt: 'ReLPU: a new framework with parallel encoders for local and global features.'
date: 2025-08-21
venue: 'Computer Vision and Image Understanding'
#slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://doi.org/10.1016/j.cviu.2025.104467'
#bibtexurl: 'http://academicpages.github.io/files/bibtex1.bib'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
image: /images/publications/relpu.png
---
In recent years, point cloud upsampling has been widely applied in fields such as 3D reconstruction. Our study investigates the factors influencing point cloud upsampling on both global and local levels through representation learning. Specifically, the paper inputs global and local information of the same point cloud model object into two encoders to extract these features, fuses them, and then feeds the combined features into an upsampling decoder. The goal is to address issues of sparsity and noise in point clouds by leveraging prior knowledge from both global and local inputs. And the proposed framework can be applied to any state-of-the-art point cloud upsampling neural network. Experiments were conducted on a series of autoencoder-based models utilizing deep learning, yielding interpretability for both global and local inputs, and it has been proven in the results that our proposed framework can further improve the upsampling effect in previous SOTA works. At the same time, the Saliency Map reflects the differences between global and local feature inputs, as well as the effectiveness of training with both inputs in parallel.(/images/publications/relpu.png)
