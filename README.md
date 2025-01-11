# Facial Expression to Emoji Converter

This project is a machine learning-based application that detects facial expressions from a webcam feed and maps them to corresponding emojis or avatars in real time. It includes a trained Convolutional Neural Network (CNN) model for emotion recognition and a graphical user interface for displaying results.

## Features
- Detects seven emotions: 
  - Angry
  - Disgusted
  - Fearful
  - Happy
  - Neutral
  - Sad
  - Surprised
- Real-time webcam-based facial expression detection.
- Maps detected emotions to emojis/avatars.
- Provides a graphical user interface built with Tkinter.

## Folder Structure
. ├── emoji.py # Main script for real-time emotion detection and emoji display 
  ├── model.h5 # Pre-trained model weights 
  ├── train.py # Script for training the emotion detection model 
  └── emojis/ # Folder containing emoji images for each emotion


## Prerequisites
- Python 3.x
- Virtual environment (recommended)

### Required Libraries
- numpy
- tensorflow/keras
- opencv-python
- Pillow (PIL)

Install the dependencies using:

pip install numpy tensorflow opencv-python pillow
Usage
Step 1: Train the Model (Optional)
If you wish to train the model from scratch, use the train.py script:

Organize your dataset into the following structure:

data/
├── train/
│   ├── Angry/
│   ├── Disgusted/
│   ├── Fearful/
│   ├── Happy/
│   ├── Neutral/
│   ├── Sad/
│   └── Surprised/
└── test/
    ├── Angry/
    ├── Disgusted/
    ├── Fearful/
    ├── Happy/
    ├── Neutral/
    ├── Sad/
    └── Surprised/
Run the training script:

python train.py
The model weights will be saved to model.h5.
Step 2: Run the Application
Place your emoji images in the emojis/ directory. Ensure the filenames match the keys in the emoji_dist dictionary in emoji.py.
Start the application:

python emoji.py
The GUI will open, showing a live feed from your webcam and the corresponding emoji for the detected emotion.
Step 3: Quit the Application
Press the Quit button in the GUI to exit the application.
Notes
The project uses Haar Cascade for face detection. Ensure the correct path to the haarcascade_frontalface_default.xml file is set in emoji.py.
The model recognizes only grayscale images of size 48x48. Make sure your input conforms to these specifications during training and inference.
Troubleshooting
If the webcam feed does not open, ensure that your webcam drivers are properly installed and accessible.
If emotion detection does not work as expected, verify the paths to emoji images and the model.h5 file.
Credits
Libraries Used: Keras, TensorFlow, OpenCV, Pillow
Dataset: FER-2013 Emotion Dataset (or any other similar dataset for training).
License
This project is licensed under the MIT License. Feel free to use and modify it for educational purposes.


This `README.md` provides a clear and concise overview of the project, its setup, and usage instructions. Let me know if you'd like any further customizations!





