
# Digit Recognition System

This project is about recognizing handwritten digits using the MNIST dataset. The project has two parts:
1.   Model Training  : We use a Convolutional Neural Network (CNN) to train the system to recognize handwritten numbers.
2.   GUI (Graphical User Interface)  : This lets users draw numbers, and the system will try to guess the digit.

## Files in This Project

- `train_digit_recognizer.py`: This file contains the code to train the CNN model using the MNIST dataset.
- `gui_digit_recognizer.py`: This file runs the user interface where you can draw a digit, and the model predicts it.
- `mnist.h5`: This file is the trained model, saved after training.

## Requirements

You need to install some software before running this project. The most important ones are:

- `tensorflow`
- `keras`
- `numpy`
- `pillow`
- `tkinter`
- `pywin32`

To install them, open your terminal or command prompt and type:
```bash
pip install tensorflow keras numpy pillow pywin32
```

## Training the Model

To train the model, you just need to run the `train_digit_recognizer.py` file:
```bash
python train_digit_recognizer.py
```
This will train the model using the MNIST dataset and save it as `mnist.h5` for later use.

## Running the GUI

After you have the model, you can run the graphical interface to start recognizing handwritten digits. Use this command to start the GUI:
```bash
python gui_digit_recognizer.py
```

### How to Use the Program:
1. Draw a number between 0 and 9 in the box.
2. Click the   Recognize   button to get the model’s guess.
3. The result (the predicted digit and the confidence level) will appear on the screen.
4. If you want to clear the drawing, press   Clear   to start again.

## Model Information

The model is a Convolutional Neural Network (CNN) with the following structure:
-   First Layer  : 32 filters, kernel size 5x5, ReLU activation.
-   Pooling Layer  : 2x2 pooling.
-   Second Layer  : 64 filters, kernel size 3x3, ReLU activation.
-   Pooling Layer  : 2x2 pooling.
-   Flatten Layer  : Flattens the input for the Dense layers.
-   Dense Layer  : 128 units, ReLU activation.
-   Dropout Layers  : To avoid overfitting, dropout is applied.
-   Dense Layer  : 64 units, ReLU activation.
-   Output Layer  : 10 units (one for each digit), softmax activation.

## Dataset Used

We trained the model using the [MNIST dataset](http://yann.lecun.com/exdb/mnist/), which has 60,000 training images and 10,000 test images of handwritten digits (0-9).

## Improvements

Some improvements that can be made to this project include:
- Trying new CNN architectures for better accuracy.
- Experimenting with different optimizers or hyperparameters.
- Adding more features to the GUI, like the ability to save the drawn images.
