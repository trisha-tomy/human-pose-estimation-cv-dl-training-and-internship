# Human Pose Estimation CV DL Training And Internship

## Introduction
- The Human Pose Detection Project is an advanced computer vision application that aims to automatically detect and analyze the human body's pose from images.
- The project utilizes state-of-the-art deep learning techniques to accurately estimate the positions of key body joints and limbs, providing a comprehensive understanding of the human body's posture.
- Our Dataset contains train as well as test data, but our test data is unlabelled.
- So we used train data by splitting it into 2 parts i.e. train and test.

## Implementation
### 1. Loading And Sorting Data
- Downloaded a pre-trained model from TF Hub and obtained inference code from GitHub.
- Used predefined functions to test the model on a sample image.
- Acquired the AII2022 Conference Competition Dataset for Yoga Poses.
- Sorted the train data based on the PoseLabel column and recombined the folders to have the required file structure for the MoveNet model.
- Split the sorted train data into Train and Test sets in an 80:20 ratio.

### 2. Preprocessing Train And Test Data
- Due to RAM constraints on Kaggle, we divided the train data into three parts and processed them separately.
- Utilized the MoveNet preprocessor to generate keypoints on the images and stored this keypoint information in a CSV file.

### 3. Model Training And Evaluation
- Concatenated the separate train CSV files to create a combined file of all the train data.
- Utilized predefined functions to convert the pose landmarks to pose classes for classification.
- Trained a neural network using Keras to classify images into their respective yoga poses based on detected pose landmarks.
- The model calculates pose embeddings from the landmarks and predicts the pose class.
- Evaluated the model using a confusion matrix to understand its strengths and weaknesses.





- We observed that where there was a lack of training data/images in certain classes, there was a dramatic drop in model accuracy.

