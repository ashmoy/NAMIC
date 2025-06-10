---
layout: pw43-project
permalink: /universal-tooth-labeling/
project_title: "Universal Tooth Labeling Module"
category: Segmentation / Landmarking
key_investigators:
- name: Enzo Tulissi
  affiliation: University of Michigan
  country: USA
- name: Lucia Cevidanes
  affiliation: University of Michigan
  country: USA
---

# Project Description

The **Universal Tooth Labeling** module employs nnUNet to automatically label all teeth (including primary dentition) from CBCT scans.  
It aims to deliver robust, anatomically correct labels for each tooth.

Currently, some outputs exhibit left/right mirroring errors (e.g., both canines labeled as “right canine”).

# Objective

1. **Resolve mirroring errors** in the labeling output.  
2. **Optimize nnUNet training** (patch size, batch size, learning rate) and augmentations.  
3. **Implement post‐processing checks** to verify and correct side‐specific labels.

# Approach and Plan

1. Analyze cases with mirroring errors and identify their characteristics.  
2. Expand the training dataset with side‐specific augmentations.  
3. Tune nnUNet hyperparameters for optimal label accuracy.  
4. Develop a post‐processing module to enforce correct left/right assignment.  
5. Evaluate performance (DSC, IoU) on a dedicated test set.  
6. Deploy the improved module in 3D Slicer and gather clinician feedback.

# Progress and Next Steps

**Completed:**
- Initial nnUNet pipeline and label export implemented.  
- Prototype output integrated into 3D Slicer.

**Next Steps:**
- Fix mirroring bugs in output labels.  
- Retrain model on augmented dataset.  
- Build and test side‐verification post‐processing.  
- Conduct clinical validation and benchmarking.

# Illustrations

![image](https://github.com/user-attachments/assets/5632a488-8b6d-45b3-946c-567c8d40b613)

*Figure 1: Example output from Universal Tooth Labeling*

# Background and References

- [Universal Tooth Labeling (in progress)](https://github.com/DCBIA-OrthoLab/SlicerAutomatedDentalTools/tree/main/CLIC/BATCHDENTALSEG)
