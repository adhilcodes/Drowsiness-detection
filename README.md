# Driver Drowsiness Detection System

Drowsiness detection is a safety technology that can prevent accidents that are caused by drivers who fell asleep while driving. Here we built a small scale demo of a drowsiness detection system that will detect that a person’s eyes are closed for a few seconds. This system will alert the driver when drowsiness is detected. We used OpenCV to detect faces and eyes using a haar cascade classifier and then we used a CNN model to predict the status.

## pipeline of the project:

In this Python project, we will be using OpenCV for gathering the images from webcam and feed them into a Deep Learning model which will classify whether the person’s eyes are ‘Open’ or ‘Closed’. The approach we will be using for this Python project is as follows :

Step 1 – Take image as input from a camera.

Step 2 – Detect the face in the image and create a Region of Interest (ROI).

Step 3 – Detect the eyes from ROI and feed it to the classifier.

Step 4 – Classifier will categorize whether eyes are open or closed.

Step 5 – Calculate score to check whether the person is drowsy.

## Dataset we used:

[Data](https://www.kaggle.com/datasets/serenaraju/yawn-eye-dataset-new)

## The Model Architecture
The model we used is built with Keras using Convolutional Neural Networks (CNN). A convolutional neural network is a special type of deep neural network which performs extremely well for image classification purposes. A CNN basically consists of an input layer, an output layer and a hidden layer which can have multiple layers. A convolution operation is performed on these layers using a filter that performs 2D matrix multiplication on the layer and filter.

The CNN model architecture consists of the following layers:

 - Convolutional layer; 32 nodes, kernel size 3
 - Convolutional layer; 32 nodes, kernel size 3
 - Convolutional layer; 64 nodes, kernel size 3
 - Fully connected layer; 128 nodes
 
The final layer is also a fully connected layer with 2 nodes. A Relu activation function is used in all the layers except the output layer in which we used Softmax.


## Project Prerequisites
 - The requirement for this Python project is a webcam through which we will capture images.
 - You need to have Python (3.6+ version recommended) installed on your system
 - Then using pip, you can install the necessary packages:
	`pip intsall -r requirements.txt`
OpenCV – pip install opencv-python (face and eye detection).
TensorFlow – pip install tensorflow (keras uses TensorFlow as backend).
Keras – pip install keras (to build our classification model).
Pygame – pip install pygame (to play alarm sound).

## Directory structure

 - The “haar cascade files” folder consists of the xml files that are needed to detect objects from the image. In our case, we are detecting the face and eyes of the person.
 - The models folder contains our model file “cnnCat2.h5” which was trained on convolutional neural networks.
 - We have an audio clip “alarm.wav” which is played when the person is feeling drowsy.
 - “Model.py” file contains the program through which we built our classification model by training on our dataset. You could see the implementation of convolutional neural network in this file.
 - “Drowsiness detection.py” is the main file of our project. To start the detection procedure, we have to run this file.
 
 ## How to run locally
 
 `pip install -r requirements.txt`
 
 `python3 main.py`
