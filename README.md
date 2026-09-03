# Persian Sign Language Detection Based on Normalized Depth Image Information

Research project on **depth-image normalization, 3D hand-pose compensation, feature extraction, and machine-learning classification** for Persian Sign Language recognition.

This work is based on my M.Sc. research in Electrical Engineering and the publication:

**Shahab Rajabi & A. Mousavinia — “Persian Sign Language Detection Based on Normalized Depth Image Information,” Journal of Control, 2019.**

## Research Motivation

Gesture-recognition systems using Microsoft Kinect often use depth primarily to separate the hand from the RGB image. This work investigates a stronger role for depth information by normalizing the hand directly in 3D space before feature extraction and classification.

## Method Overview

```text
Kinect depth data
      |
Depth-based hand segmentation
      |
3D hand-surface orientation estimation
      |
Rotation compensation / pose normalization
      |
Depth-distance normalization
      |
Wavelet + Circular Descriptor features
      |
MLP / SVM classification
      |
Persian Sign Language recognition
```

## 3D Normalization

The approach first extracts the hand template using a depth threshold. It then estimates a vector perpendicular to the hand surface in three-dimensional space.

A rotation matrix is used to compensate hand rotations around the three axes so that the normalized hand surface is aligned with the camera coordinate system. The resulting 3D hand representation is also translated to a standardized distance from the Kinect sensor.

This normalization step is intended to reduce variation caused by hand orientation and distance before classification.

## Feature Extraction and Classification

The research uses:

- wavelet-based features
- a proposed **Circular Descriptor**
- Multilayer Perceptron (MLP)
- Support Vector Machine (SVM)

The reported empirical evaluation achieved an average recognition accuracy of **96.7%**, with approximately two seconds of delay for online recognition in the evaluated setup.

## Research Themes Demonstrated

- Computer vision
- Depth-image processing
- 3D geometric normalization
- Feature engineering
- MLP neural networks
- Support Vector Machines
- Gesture and sign-language recognition
- Signal / image processing

## Publication

A PDF associated with the work is included in this repository. Please refer to the publication record for definitive citation details.

## Broader Research Connection

This project represents my earlier work in computer vision and machine learning. My more recent research focuses on adaptive learning, time-series modelling, anomaly detection, and AI-assisted wireless-network optimization.

[View my research portfolio](https://github.com/Shahabrjb/About-Me)

## Author

**Shahab Rajabi**  
Machine Learning & RAN Optimization Engineer
