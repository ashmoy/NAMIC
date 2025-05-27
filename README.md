---
layout: pw43-project
permalink: /:path/
project_title: "Root Resorption Severity Classification in Impacted Canine Cases Using CLIC and Universal Tooth Labeling"
category: Segmentation / Classification / Landmarking
key_investigators:
- name: Enzo Tulissi
  affiliation: University of Michigan
  country: USA

- name: Lucia Cevidanes
  affiliation: University of Michigan
  country: USA
---

# Project Description

This project aims to integrate and build upon two existing 3D Slicer modules — **CLIC** and **Universal Labeling** — to support the automated detection and classification of impacted canines and the severity of root resorption in adjacent teeth.
The **CLIC** module uses a Mask R-CNN segmentation model to localize and classify impacted canines from CBCT scans. It is fully developed and operational.
The **Universal Labeling** module, use nnUNet to automatically labels all teeth (including primary teeth), is still in development. It currently produces mirrored labeling errors in some cases (e.g., labeling both left and rightcanines as "right canine").
The overarching goal of this project is to combine outputs from both modules to develop and train a new model capable of **automatically classifying the severity of root resorption** in teeth adjacent to impacted canines.

# Objective

1. **Integrate modules**: Use **CLIC** to segment and classify impacted canines, and **Universal Labeling** to identify and isolate adjacent teeth.
2. **Curate training dataset**: Generate a dataset of segmented and labeled teeth adjacent to impacted canines with root resorption severity annotated by clinicians.
3. **Develop new model**: Train a supervised model to classify root resorption severity from segmented teeth.
4. **Visualize results**: Display interpretable outputs (segmentation + severity classification) directly in 3D Slicer.

# Approach and Plan

1. Evaluate and refine Universal Labeling output to correct mirroring/side-labeling errors.
2. Apply CLIC on CBCT scans to isolate impacted canines.
3. Combine the segmentation output from both modules to extract adjacent teeth.
4. Annotate root resorption severity on adjacent teeth for training (using clinician-provided scores).
5. Train a new model using geometric and morphological features of adjacent roots.
6. Integrate the trained model into a third Slicer module or extend CLIC to include severity classification.
7. Validate performance and visualize predictions in 3D with segmentation overlays.

# Progress and Next Steps

**Completed:**
- CLIC module is finalized and tested on multiple datasets.
- Basic Universal Labeling module is functional.

**Next steps:**
- Fix mislabeling bugs in Universal Labeling (e.g., side symmetry confusion).
- Start building annotated dataset of resorption severity.
- Design training pipeline for classification model.
- Plan Slicer module UI for final output visualization.

# Illustrations
![image](https://github.com/user-attachments/assets/28abe255-b5ab-427e-9ef9-d2210e95dca0)


*Figure 1 : Segmentation of impacted canines using CLIC*

![image](https://github.com/user-attachments/assets/8b28c37e-53e0-4799-a18e-a7ec3777b6f2)

*Figure 2 : output of Universal Labeling*

# Background and References

- [CLIC Source Code](https://github.com/DCBIA-OrthoLab/SlicerAutomatedDentalTools/tree/main/CLIC)
- [Universal Labeling (in progress)](https://github.com/DCBIA-OrthoLab/SlicerAutomatedDentalTools/tree/main/CLIC/BATCHDENTALSEG)


