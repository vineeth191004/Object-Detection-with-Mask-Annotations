## OBJECT-DETECTION WITH MASK ANNOTATIONS

# Overview

This project demonstrates an object detection pipeline using TensorFlow and Keras. It covers data preparation, model training, and visualization of results. The repository includes:

- **Data Preparation**: Parsing XML annotations and loading images.
- **Model Training**: Implementing and training a custom CNN and a VGG16-based object detection model.
- **Visualization**: Displaying images with bounding boxes for both ground truth and predictions.

# Dataset
The dataset can be found [here](https://www.kaggle.com/datasets/andrewmvd/face-mask-detection) and it consists of :- 

- **Images**: A collection of images where objects are annotated with bounding boxes.
- **Annotations**: XML files containing bounding box coordinates for each object in the images. The coordinates are normalized to the image dimensions.

# Data Preparation
The data preparation involves:

**Parsing XML Files:** Extracting normalized bounding box coordinates from XML annotations.
**Loading Images and Annotations:** Resizing images and preparing bounding box data for training.

# Model Training
**Custom CNN Model**
A custom CNN is built and trained to predict bounding box coordinates. This model is designed from scratch and uses dropout and learning rate reduction strategies to improve performance and prevent overfitting.

**VGG16-Based Model**
The VGG16 model, pretrained on ImageNet, is adapted for object detection. The base model is frozen, and custom dense layers are added to predict bounding boxes. This transfer learning approach leverages the pretrained features of VGG16 to enhance model performance.

# Visualization
The results are visualized to compare predictions with ground truth:

Images with Bounding Boxes: A subset of validation images is displayed with true(blue color) and predicted bounding boxes(red) overlaid for visual inspection.
