# Face Detection and Recognition with(out) Neural Networks
This project uses a Convolutional Neural Network (CNN) to perform improvement of face detection and recognition, inspired by the classical Viola-Jones algorithm. The system replaces traditional Haar-like features and AdaBoost classifiers with CNN layers to improve accuracy and adaptability. That's project is done solely for educational experience 

## without ML
this is the 1st directory created in 2022 and editing during the years with using of algorithmic approaches in CV, except DL,ML,NN and others
## with ML
this is the 2nd directory created in 2024 and implied to show the difference between the latest ML approaches and out-of-ML approaches by advanced db, preprocessing, correction of architecture of the model and other ML approaches in CV

# Table of Contents
### Installation
### Project structure
### Dataset structure
### Training process
### Trained Model
### Additional Files


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Installation

[Installation Trained model](https://github.com/kozgunov/Viola_Jones_alg_faces/blob/main/V-J_2_with_ML/interactive_inference)

[Installation Untrained model](https://github.com/kozgunov/Viola_Jones_alg_faces/blob/main/V-J_2_with_ML/interactive_inference)

[Install dependencies](https://github.com/opencv/opencv/tree/master/data/haarcascades)

Install the technology stack for usage:
pip install opencv-python opencv-contrib-python tensorflow numpy





------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Project Structure

Face-Detection-Recognition/
│

├── dataset/                    # Folder containing face images

│   ├── person1/                # Subfolder for person 1

│   │   ├── img1.jpg

│   │   └── img2.jpg

│   ├── person2/                # Subfolder for person 2

│   │   └── img1.jpg

│   └── ...

│

├── haarcascade_frontalface_default.xml  # Haar cascade for face detection (required for preprocessing)

├── cnn_face_recognizer.h5      # Trained CNN model (after training)

├── Viola-Jones-face-detection.py   # Script to detect and recognize faces using the trained model

├── Viola-Jones-too.py          # Script for training the CNN model

├── README.md                   # Project description and installation guide (this file)

├── features.npy                # (Optional) Pre-saved face features after training

├── labels.npy                  # (Optional) Pre-saved labels after training

└── ...


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Dataset structure
Recomended to have at least 2'500-10'000 photo in jpg with/without marked faces

**Structure**

├── person1 ├── img1.jpg ; img2.jpg

├── person2 ├── img1.jpg ; img2.jpg

...

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Training process
[Trained by](https://github.com/kozgunov/Viola_Jones_alg_faces/edit/main/)

This script will:
- Load the dataset and detect faces using the Haar cascade.
- Preprocess the images by resizing them to 64x64 pixels.
- Train a CNN model on the detected faces.
- Save the trained model to a file (cnn_face_recognizer.h5).

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Trained Model
[Installation Trained model](https://github.com/kozgunov/Viola_Jones_alg_faces/edit/main/)

This script will:
- Load the trained model (cnn_face_recognizer.h5).
- Detect faces in new images using the same Haar cascade (haarcascade_frontalface_default.xml). Download from the link below.
- Preprocess the detected face(s) and pass them through the CNN to predict the person's identity.
- Display the image with a bounding box around the detected face(s) and the predicted person's name.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Additional Files
1. haarcascade_frontalface_default.xml:
This file is required for face detection using the Haar cascade. It is used during the preprocessing step to detect faces before resizing them for CNN input.
Download the Haar cascade from OpenCV's official repository [here](https://github.com/opencv/opencv/tree/master/data/haarcascades).

3. features.npy and 3. labels.npy (Optional):
These files contain the preprocessed face features and labels, respectively. They are saved during the training process and can be reused to avoid preprocessing the dataset again.

4. face_recognizer_model.yml (Optional):
The trained CNN model. This file is generated after training and is used for inference (face recognition).

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
If you encounter any issues or have questions, feel free to reach out through GitHub issues or contact the project owner.



