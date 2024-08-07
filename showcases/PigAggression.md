# Pig-Aggression-Detector-using-CNN-and-Image-Differentials
![image](https://github.com/HarryAricibasi/HarryAricibasi/blob/e56d7bdeeabec9cf474d4e7a39558fc9d664b2ca/images/pigpggressionexample1.png)

#### Background
Pig aggression poses a significant challenge in the swine industry, affecting both animal welfare and productivity. This project aims to develop an automated system for detecting aggressive behaviors in pigs using video footage and deep learning techniques. By employing convolutional neural networks (CNN) and image differentials, we strive to improve the welfare of group-housed pigs and enhance overall farm efficiency.

#### Project Objective
To design and implement a deep learning model capable of identifying and classifying aggressive behaviors in pigs from video recordings. The goal is to provide a real-time, efficient solution for monitoring and managing pig behavior.

#### Methodology
1. **Data Collection**:
   - **Setup**: 32 pairs of unfamiliar piglets were observed in two separate pens over a period of 3 days.
   - **Footage**: Each pair was video recorded for 1 hour daily, totaling 16 hours of footage.
   - **Selection**: 1.25 hours of video data were selected for the modeling process.

2. **Approach**:
   - **Datasets**: Four datasets were created:
     - **Diff1**: Frames skipped every 1 frame.
     - **Diff5**: Frames skipped every 5 frames.
     - **Diff10**: Frames skipped every 10 frames.
     - **Blended**: Multiple image differences combined into a single dataset.
   - **CNN Models**:
     - **Model 1**: Standard VGG-16 architecture with convolutional, max-pooling, dense, and dropout layers.
     - **Model 2**: Enhanced VGG-16 with additional stacked convolutional layers.

3. **Evaluation**:
   - **Activation Function**: Nine sigmoid activation thresholds between 0.1 and 1.0 were tested, with 0.5 selected for final evaluation.
   - **Metrics**: Accuracy, precision, recall, and area under the curve (AUC) were calculated.
   - **Performance**: The stacked CNN model achieved:
     - **Accuracy**: 0.80
     - **Precision**: 0.80
     - **Recall**: 0.78
     - **AUC**: 0.80
   - **Behavior Classification**:
     - **Easy to Classify**: Head biting, immobile, and parallel pressing (recall: 0.95, 0.94, 0.91).
     - **Challenging**: Mounting and mobile non-aggressive behaviors (recall: 0.63, 0.75).

4. **Efficiency**:
   - **Training Time**: The blended dataset reduced training and validation time by up to 75% compared to Diff1, Diff5, and Diff10 datasets.
   - **Preprocessing Time**: Reduced by up to 2.3 times in the blended dataset, making it suitable for real-time applications.

#### Tools
- **Programming Language**: Python
- **Libraries**: TensorFlow/Keras for deep learning, OpenCV for image processing
- **Environment**: Jupyter Notebooks, Google Colab, or local Python environment

![image](https://github.com/HarryAricibasi/HarryAricibasi/blob/e56d7bdeeabec9cf474d4e7a39558fc9d664b2ca/images/PARTscreenshot.PNG)

#### Results
The use of CNNs combined with image differentials has proven to be an effective and computationally efficient method for detecting aggressive behaviors in pigs. The proposed system can be integrated into real-time monitoring systems to improve animal welfare and productivity in swine farming operations.
Developed Pig Aggression Recognition Tool (PART) for end users. Through a simple and easy interface, anyone can classify Pig Aggression reliably for research purposes.

#### Future Work
- **Dataset Expansion**: Incorporate more varied datasets with different pig breeds and environments.
- **Model Enhancement**: Experiment with other CNN architectures and fine-tuning techniques.
- **Real-time Deployment**: Develop and deploy a user-friendly application for farm integration.

#### Links
- [A computer vision image differential approach for automatic detection of aggressive behavior in pigs using deep learning](https://doi.org/10.1093/jas/skad347)
