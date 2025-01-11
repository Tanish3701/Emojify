

# Facial Expression to Emoji/Avatar Converter

This project is a machine learning-based application that detects human facial expressions in real-time using a webcam and converts them into corresponding emojis or avatars. It uses a Convolutional Neural Network (CNN) model trained to classify facial expressions into seven categories: Angry, Disgusted, Fearful, Happy, Neutral, Sad, and Surprised.

---

## Folder Structure
```
📂 Project Directory
├── emoji.py          # Application script for real-time emotion detection and emoji display
├── model.h5          # Pre-trained weights for the CNN model
├── train.py          # Script for training the emotion detection model
├── data/             # Directory containing training and testing datasets
│   ├── train/        # Training dataset
│   ├── test/         # Testing dataset
├── emojis/           # Directory containing emoji images for each emotion
```

---

## Features
1. **Real-time Emotion Detection**:
   - Uses OpenCV to capture live video feed.
   - Detects facial expressions using a pre-trained CNN model.

2. **Emoji/Avatar Display**:
   - Maps detected emotions to corresponding emoji images.
   - Displays emojis alongside the live video feed.

3. **Customizable and Extendable**:
   - Add new emojis or train on custom datasets for other tasks.

---

## Getting Started

### Prerequisites
- Python 3.x
- Required Python packages:
  - `numpy`
  - `opencv-python`
  - `keras`
  - `tensorflow`
  - `pillow`

Install all dependencies using:

pip install -r requirements.txt


---

### Training the Model
1. Prepare your dataset:
   - Place training images in `data/train` and testing images in `data/test` directories.
   - Ensure images are grayscale and organized by emotion category.

2. Run the training script:

   python train.py

   - This will train the CNN model and save the weights in `model.h5`.

---

### Running the Application
1. Ensure the `model.h5` file is in the project directory.
2. Add emoji images to the `emojis/` directory with filenames matching the emotions.
3. Run the application script:

   python emoji.py

   - The application will open a GUI displaying the video feed, predicted emotions, and corresponding emojis.

---

## Emotion Categories
The model classifies facial expressions into the following categories:
1. Angry
2. Disgusted
3. Fearful
4. Happy
5. Neutral
6. Sad
7. Surprised

---

## Customization
1. Add more emoji images in the `emojis/` directory.
2. To retrain the model on a different dataset, update the paths in `train.py` and adjust the class labels as needed.

---

## Limitations
- The model relies on the quality of training data. For best results, use a diverse dataset.
- May not perform well in low-light conditions or with partially visible faces.

---

## Future Enhancements
- Add support for more emotions.
- Improve the GUI for better user experience.
- Use a more robust model architecture for better accuracy.

