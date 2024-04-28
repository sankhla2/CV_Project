# CV_Project
# Human Face Detection

This repository contains the code and report for a computer vision project focused on human face detection. The project aims to develop a robust and efficient system capable of accurately locating and identifying human faces in given input images or video streams.

## Problem Statement

The main objective of this project is to develop a human face detection system that can handle various challenges, such as variations in lighting conditions, facial expressions, occlusions, and different orientations of the face. Face detection is a fundamental task in computer vision and image processing, with numerous applications in areas such as security, biometrics, human-computer interaction, and multimedia.

## Dataset

For this project, two types of datasets were used:

1. **Training and Validation Dataset**: A combination of the Celeb dataset and the ImageNet dataset. The Celeb dataset images were used as face images, while the ImageNet dataset images were used as non-face images.

2. **Testing Dataset**: The Face Detection Dataset, which contains images with the coordinates of the bounding boxes for the faces.

## Methodology

Three different algorithms were employed for face detection:

1. **Face Detection using Haar Features**: Haar filters were used to extract 5D features from the Celeb-ImageNet combination dataset. These features were then used to train classical Support Vector Machine (SVM) and AdaBoost models.

2. **Face Detection using ResNet Features**: Instead of using handcrafted Haar features, a neural network was trained on the same dataset as above. This approach achieved a classification accuracy of 80%.

3. **Face Detection Evaluation Using MTCNN**: The pretrained Multi-Task Cascaded Convolutional Networks (MTCNN) method was employed for accurate and efficient human face detection. MTCNN is a deep learning-based approach that combines multiple convolutional neural networks (CNNs) in a cascaded framework.

## Results

1. **ResNet + Sliding Window Detector**: The ResNet model trained on face crops from the CelebA dataset did not generalize well to real-world images.

2. **MTCNN**: The face detection performance was evaluated using the Intersection over Union (IoU) metric on the first five images of the testing dataset. The detected bounding boxes were compared with the ground truth bounding boxes, and the IoU was calculated for each pair. The mean IoU across all detected and ground truth bounding boxes was reported as a quantitative measure of the system's performance on the evaluated subset. The achieved mean IoU was 0.007939509197251175.

## Conclusion

The project demonstrated that classical approaches, such as Haar features and sliding window detectors, can only achieve limited performance compared to end-to-end trainable pipelines like MTCNN. Neural network-based methods, leveraging deep learning techniques, prove to be more effective for complex tasks like face detection.

## References

- MTCNN: [Arxiv](https://arxiv.org/abs/1604.02878)
- Haar Features: [IEEE](https://ieeexplore.ieee.org/document/990517)
- ResNet: [IOP Science](https://iopscience.iop.org/article/10.1088/1757-899X/1228/1/012005/pdf)
