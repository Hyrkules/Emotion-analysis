# Emotion Detection from Facial Expressions

![Live Demo](/main image.png)

## Project Overview
The goal of this project is to classify a person's emotion based on their facial expression. The dataset used contains 35,887 images categorized into seven emotions: neutral, angry, happy, disgusted, fearful, sad, and surprised. The dataset is divided into two folders: training and validation.

## Dataset
The dataset consists of 35,887 images categorized into the following seven classes:
- Neutral
- Angry
- Happy
- Disgusted
- Fearful
- Sad
- Surprised

It is split into two folders:
- **Train**: For training the model.
- **Validation**: For validating model performance during training.

## Model Architecture
The model used for training is a convolutional neural network (CNN) designed from scratch. It consists of 10 layers:
- Rescaling layer to normalize pixel values (0-255) to (0-1).
- Convolutional layers to extract features from the images.
- Pooling layers to reduce image dimensions.
- A flatten layer to transition from convolutional to dense layers.
- Dense layers to interpret image features and facilitate classification.

The layers are designed to efficiently capture the important features of facial expressions and classify them into the respective emotion categories.

## Training and Results
The model was trained using a batch size of 32, with images resized to 180x180 pixels. TensorFlow and Keras were used to build and train the model, and the training process utilized data augmentation and preprocessing techniques to improve generalization.

The results showed that with a relatively simple model, reasonable accuracy was achieved in classifying the emotions. It is expected that a more complex model with additional layers and fine-tuning would further improve the accuracy.

![Live Demo](/metric study.png)

## Live Demo
In this project, a live demo can be performed using the webcam of a computer. The model will detect the emotion of a face seen by the webcam in real-time.

The demo consists of:
1. Activating the computer's camera.
2. Capturing live frames and resizing them to match the model's input dimensions (180x180 pixels).
3. Preprocessing the input image as required by the ResNet50 model.
4. Passing the preprocessed frame to the model for emotion prediction.
5. Displaying the predicted emotion on the screen in real-time.
