
# Deep Learning for Brain Tumor Segmentation : Medical Imaging projects
## Medical Imaging & Big Data Analysis | Data Science Master's Degree

**Authors:**  
Induni Sandapiumi Nawarathna Pitiyage (ID: 906451)  
Sara Campolattano (ID: 906453)  

**Course:** Medical Imaging & Big Data  
Master’s Degree in Data Science, 2024–2025

---

## Project Overview

This project investigates deep learning techniques for semantic segmentation of brain tumors from MRI scans using the BRATS dataset. Starting from a baseline U-Net architecture, the project progressively integrates dropout regularization, data augmentation, and residual connections to assess their individual and combined impact on segmentation performance.

---

## Dataset

- Source: BRATS dataset (pre-operative 3D brain MRI volumes)
- Modalities: T1, T1c, T2, FLAIR
- Labels: Whole Tumor, Tumor Core, Enhancing Tumor
- Preprocessing:
  - All volumes resized to 120×120×77
  - Voxel intensities normalized
  - Masks one-hot encoded into 4-class binary channels
- Data split:
  - 67% Training (46 patients)
  - 33% Testing (24 patients)
  - Each patient contributes 77 2D slices

---

## Project Phases

### Phase 1 – Baseline U-Net with Dropout (`final_4_dropout.ipynb`)
- 2D U-Net architecture with dropout increasing by depth (0.2 to 0.4)
- Evaluated using a custom Dice accuracy metric

### Phase 2 – Data Augmentation (`final_12_dropout_aug.ipynb`)
- Introduced spatial and intensity-based augmentations
- Augmentation applied to 50% of training data

### Phase 3 – Residual U-Net (`final_9_residual.ipynb`)
- Incorporated residual blocks within the U-Net architecture
- No augmentation applied

### Phase 4 – Combined Enhancements (`final_13_dropout_aug_residual.ipynb`)
- Combined residual blocks, dropout, and data augmentation

---

## Included Files

- `final_4_dropout.ipynb`: Phase 1 – Baseline U-Net
- `final_12_dropout_aug.ipynb`: Phase 2 – Data Augmentation
- `final_9_residual.ipynb`: Phase 3 – Residual U-Net
- `final_13_dropout_aug_residual.ipynb`: Phase 4 – Combined Model
- `Medical Imaging & Big Data - Pitiyage Campolattano - June 18.pptx.pdf`: Final presentation slides

---

## Presentation

Please refer to the accompanying PDF for:
- Architectural diagrams and model summaries
- Training and validation performance plots
- Dice score distributions per region
- Qualitative segmentation comparisons across all four phases
