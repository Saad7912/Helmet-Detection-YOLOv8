# YOLOv8 Helmet Detection

This project involves detecting whether a bike rider is wearing a helmet using YOLOv8, a state-of-the-art object detection algorithm. The project demonstrates the process of converting annotations into YOLO format, training the YOLOv8 model, and running object detection on video files to visualize the results.

## Project Overview

The goal of this project is to use YOLOv8 for helmet detection in video footage. The project encompasses several stages, including data preparation, model training, and evaluation of detection results on video files.

## YOLO Format

YOLO (You Only Look Once) uses a specific format for annotations that is crucial for training the model:

- **Label File Format**: Each image has a corresponding `.txt` file with the same name, where each line represents an object in the format:
-  **`<class> <x_center> <y_center> <width> <height>`**. Coordinates are normalized to the image dimensions.
  
- **Classes and Annotations**: The class labels and bounding box coordinates must be provided in the YOLO format for the model to learn and make predictions correctly.

## Data Preparation

### Converting Annotations

Annotations in formats like XML (from LabelImg) need to be converted to YOLO format. This involves transforming bounding box coordinates and class labels into the YOLO annotation format.

### Splitting Data

The dataset should be divided into training and validation sets to ensure the model can generalize well. This split can be done manually or through automated scripts to maintain a balanced representation of classes in both sets.

## Training

Training the YOLOv8 model involves specifying the path to the dataset configuration file (YAML format), which includes details about training and validation image directories, the number of classes, and class names. The model is then trained over several epochs to learn from the dataset.

## Evaluation

After training, the model can be used to detect objects in video files. This involves reading the video, running the detection algorithm frame by frame, and visualizing the results by drawing bounding boxes and labels on detected objects.

## Important Libraries

- **OpenCV**: Used for video processing and visualization tasks, such as drawing bounding boxes and labels.
- **Ultralytics YOLO**: Provides the YOLOv8 model and functionality for object detection tasks.





