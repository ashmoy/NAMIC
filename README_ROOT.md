---
layout: pw43-project
permalink: /clic-root-resorption-classification/
project_title: "Root Resorption Severity Classification in Impacted Canine Cases Using CLIC"
category: Segmentation / Classification
key_investigators:
- name: Enzo Tulissi
  affiliation: University of Michigan
  country: USA
- name: Lucia Cevidanes
  affiliation: University of Michigan
  country: USA
---

# Project Description

The **CLIC** module uses a Mask R-CNN segmentation model to locate and classify impacted canines in CBCT scans.  
This project extends CLIC by developing a supervised model to automatically classify the severity of root resorption in teeth adjacent to impacted canines.

# Objective

1. **Segment impacted canines** using the existing CLIC module.  
2. **Extract adjacent teeth** volumes for analysis.  
3. **Assemble an annotated dataset** of adjacent teeth with clinician‐provided resorption severity scores.  
4. **Train a classification model** to predict root resorption severity from segmented volumes.  
5. **Integrate and visualize** segmentation plus severity scores within 3D Slicer.

# Approach and Plan

1. Run CLIC across the CBCT dataset to isolate impacted canines.  
2. Combine CLIC masks to extract volumes of adjacent teeth.  
3. Annotate each extracted tooth volume with a severity label (mild, moderate, severe).  
4. Extract geometric and morphological feature sets from each volume.  
5. Train a classifier on these features.  
6. Extend CLIC or create a new Slicer module for real‐time severity classification.  
7. Validate model performance (accuracy, recall, precision) and integrate into the 3D visualization workflow.

# Progress and Next Steps

**Completed:**
- CLIC module validated.  
- Prototype pipeline for adjacent tooth extraction established.

**Next Steps:**
- Clinician annotation of extracted tooth volumes.  
- Feature engineering and model training.  
- UI design for severity score display in Slicer.  
- Performance evaluation and final documentation.

# Illustrations

![image](https://github.com/user-attachments/assets/6f588a90-3e77-440c-b5c9-9ef0c9550150)

*Figure 1: Impacted canine segmentation results from CLIC*

# Background and References

- [CLIC Source Code](https://github.com/DCBIA-OrthoLab/SlicerAutomatedDentalTools/tree/main/CLIC)

