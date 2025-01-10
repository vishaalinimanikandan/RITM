# RITM Enhancements for Advanced Image Segmentation

## Introduction
Reviving Iterative Training with Mask Guidance (RITM) is a state-of-the-art tool for interactive image segmentation. However, its current implementation supports only binary segmentation, distinguishing between foreground and background, and outputs black-and-white masks. This repository presents enhancements to the RITM framework to enable advanced segmentation capabilities, including instance and panoptic segmentation with color-coded masks.

## Features
- **Interactive Segmentation**: Enhanced RITM to support semantic, instance, and panoptic segmentation.
- **Advanced Outputs**:
  - JSON files with mask coordinates for reproducibility.
  - Overlapping translucent masks for manual quality checks.
  - Opaque color-coded masks for different instances.
- **Performance Improvements**:
  - Improved inference speed and accuracy using better augmentation and loss functions.
  - Iterative mask refinement inspired by FocalClick.

## Key Results
### Experiment-1
- **Model**: HRNet-32.
- **Changes**:
  - Trained with SUEM augmentation.
  - Implemented Iterloss from CFR-ICL.
- **Outcome**:
  - Results were poorer than expected due to the model being over-complicated by SUEM augmentation.
  - Complex augmentation techniques negatively impacted model differentiation ability.

### Experiment-2
- **Model**: HRNet-W18-C-ssld (converted from PaddlePaddle).
- **Changes**:
  - Removed SUEM augmentation.
- **Outcome**:
  - Achieved better inference speed and accuracy compared to baseline HRNet-18 models.
  - Improved results highlight the potential of lightweight models with optimized configurations.

### Overall Improvement
- **Accuracy**:
  - Improved IoU and NoC (Number of Clicks) for higher-quality segmentation masks.
- **Inference**:
  - Faster and more efficient inference due to simplified augmentations and iterative refinements.
- **Comparison**:
  - Comparable or superior results to baseline RITM models in both accuracy and inference speed.

![image](https://github.com/user-attachments/assets/09bc8c26-43ad-49c9-9564-2abc6435a167)



