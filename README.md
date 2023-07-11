# Hand-Gesture-Recognition
## Problem Statement & Background
The objective is to accurately identify and interpret hand gestures in real-time video sequences, following American Sign Language (ASL). <br>
<br>
NAD estimates that there are around 18 million deaf individuals. They can communicate among themselves using sign language but having a conversation with others is a difficult task. Significant progress has been made in the study of American Sign Language (ASL). Our project aims to build upon this work by developing a system that can translate ASL into text and sound. This will greatly enhance the conversational experience for deaf individuals, enabling them to communicate effectively. 

## Demo

Here is the demo of Hand Gesture Recognition <br>
<br>
<br>
<p align="center"> 
  <img src="https://github.com/Nikhil27-sudo/Hand-Gesture-Recognition/blob/master/demo.gif">
</p>
<br>

## Data Preparation / Processing
Created own dataset by following the American Sign Language (ASL) for alphabets, special characters, and additional custom gestures such as "YOLO" and "All the best". The dataset can be expanded to include more Sign Language vocabulary in the future. The process begins by extracting grayscale images of the hand using the absolute Background Subtraction Technique, which utilizes running averages from a sequence of video frames. After extracting the hand region, we apply thresholding for this image. Each gesture corresponds to a threshold image, and all these images are pre-processed using Keras preprocessing and image augmentation models. These models handle necessary tasks such as resizing, shifts, flips, and orientation adjustments within certain degrees. This process ultimately results in the creation of the final dataset.

<br>
<br>
<p align="center">
  <img src="https://github.com/Nikhil27-sudo/Hand-Gesture-Recognition/blob/master/data.png" width="600" height="500">
</p>
<br>

## Modeling and Architecture

The model architecture consists of a Deep Convolutional Neural Network (CNN) that includes 7 hidden convolution layers with the Rectified Linear Unit (ReLU) activation function, followed by a single fully connected layer. The network is trained over 50 iterations, using a batch size of 64. After analyzing the validation accuracy, it is observed that there is no significant improvement beyond these 50 iterations, indicating that the model is sufficiently trained. Therefore, the chosen number of iterations is deemed appropriate.


## Results

This model is designed to identify hand gestures in real-time video sequences. It achieves an impressive overall accuracy of 92% in predicting a wide range of signs and gestures. Additionally, it offers the capability to translate these hand gestures into both text and speech using the Python gTTS (Google Text-to-Speech) library. The model is dynamic, allowing users to create and train their own custom gestures. This flexibility enables users to incorporate personalized gestures into the system and utilize them effectively.
