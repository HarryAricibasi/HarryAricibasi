# Automatic Detection of Mounting Behavior in Boars Using Deep Learning
![image](https://github.com/HarryAricibasi/HarryAricibasi/blob/b05a6f94d837f4b8ecf934fb227f183c74fedc87/images/livestockmountingexample1.png)

## Project Overview

This project presents a novel approach for the automatic detection of mounting behavior in boars using deep learning-based object detection. We developed a hybrid model combining Mask R-CNN for instance segmentation and a Support Vector Machine (SVM) for behavior classification. The system was tested on video data collected from boars housed at the University of Guelph's Ontario Swine Research Centre.

## Key Features

- Utilizes Mask R-CNN with Inception ResNet V2 backbone for pig detection and segmentation
- Employs SVM for binary classification of mounting behavior
- Achieves high accuracy, precision, and recall in detecting mounting events
- Addresses challenges of occlusion and complex pig interactions in confined spaces

## Methodology

1. **Data Collection**: Video data from 8 Landrace × Yorkshire × Duroc crossbred boars, aged 4-5 months and weighing 60-90 kg.
2. **Data Preparation**: 612 2-second video clips (349 mounting, 263 non-mounting) processed into individual frames.
3. **Object Detection**: Mask R-CNN trained on 68 labeled frames for pig detection and segmentation.
4. **Feature Engineering**: Extraction of 9 features including mask count, total pixels, IoU, and distance measures.
5. **Binary Classification**: SVM trained on engineered features for mounting behavior classification.

## Results

Our hybrid model achieved impressive performance metrics:

- Accuracy: 96.65%
- Precision: 94%
- Recall: 99%
- F1 Score: 97.05%

## Significance

This project demonstrates the potential for improving animal welfare and production efficiency in the swine industry through automated behavior monitoring. The high recall rate ensures that most mounting events are detected, which is crucial for preventing injuries and stress in group-housed pigs.

## Future Work

- Expand the model to detect other important behaviors in pigs
- Implement real-time processing for immediate intervention
- Investigate the application of this technology to other livestock species

## Technologies Used

- Python 3.9
- TensorFlow Object Detection API
- OpenCV
- Mask R-CNN
- Support Vector Machine (SVM)

## Acknowledgements

This research was conducted at the University of Guelph's Ontario Swine Research Centre. We thank the staff and researchers for their support and expertise throughout the project.
