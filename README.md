This repository contains implementations of various image processing techniques to segment tumors from liver CT images using the Insight Segmentation and Registration Toolkit (ITK). The project is divided into two main sections, each focusing on different segmentation approaches and validation methods.

Section 1: Fast Marching Segmentation Algorithm
Overview
In this section, we implement the fast marching segmentation algorithm to segment liver tumors from CT scans of four different patients. Each patient's scan is analyzed separately, with the algorithm's parameters (alpha, beta, and sigma) varied systematically. We explore four different values for each parameter, resulting in a total of 64 segmentations per patient (4x4x4).

Validation
Validation is performed by comparing the segmented results with a reference segmentation. The reference is obtained through a majority vote among segments provided by three radiologists for each patient. The segments produced by the fast marching algorithm are evaluated against the reference segment using the Jaccard and Dice metrics.

Visualization
The best results, based on the Jaccard and Dice metrics, are visualized using inline images in a Jupyter Notebook. The algorithmically derived segments are visually compared with the reference segment to highlight any differences.

Section 2: Comparison of Different Segmentation Algorithms
Overview
This section focuses on the segmentation of the scan from Patient 1 using multiple algorithms:

Region Growing (Connected Threshold, Confidence Connected, Neighborhood Connected)
Fast Marching (as detailed in Section 1)
Level Sets
Watershed
Validation and Comparison
Each algorithm's results are visually compared with the reference segment. The performance of these algorithms is evaluated using several metrics:

Jaccard Index
Dice Coefficient
Volume Similarity
False Positives
False Negatives
