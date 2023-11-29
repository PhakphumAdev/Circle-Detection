# Overview
This project is developed as a solution for the Circle Detection ML Challenge and focuses on developing a machine learning model capable of detecting circles in noisy images. Using deep learning techniques, specifically Convolutional Neural Networks (CNNs), the model identifies the location and size of circles embedded in images with various noise levels.

# Project Structure
The Jupyter notebook contains the following key components:

1. Helper Functions
CircleParams: A named tuple used to represent the parameters of a circle (row, col, radius).
draw_circle: Function to draw a circle on a numpy array.
noisy_circle: Generates an image with a single circle and added normal noise.
show_circle: Displays an image with a circle, useful for visualization.
generate_examples: Provides an infinite generator of example images with circles and corresponding parameters.
2. Circle Detection Model
A deep learning model built using TensorFlow and Keras.
The model architecture includes convolutional layers for feature extraction and dense layers for output prediction.
The final layer predicts three values representing the x, y coordinates of the center, and the radius of the detected circle.
3. Intersection Over Union (IOU) Metric
Custom iou function to calculate the Intersection Over Union for two circles.
This function serves as a metric to evaluate the accuracy of the model.
4. Training and Evaluation
The model is trained on a dataset generated using generate_examples.
Includes a function to evaluate the model using various IOU thresholds.
Installation and Setup
To run this project, ensure you have the following:

Python 3.x
Libraries: NumPy, Matplotlib, scikit-image, TensorFlow
Install the required libraries using pip:
```
pip install numpy matplotlib scikit-image tensorflow
```
Running the Project
Data Generation: Use generate_examples to create a training dataset.
Model Training: Run the section in the notebook that defines and trains the CNN model.
Evaluation: Use the provided evaluation function to assess the model's performance on a test dataset.
Model Metrics
After training, the model's performance is evaluated using the IOU metric at different thresholds (0.5, 0.75, 0.9, 0.95). The results are printed at the end of the notebook.

# Conclusion
This project demonstrates the application of CNNs in a practical computer vision task, showcasing the ability to detect geometric shapes in noisy environments. The modular design allows for easy experimentation with different model architectures and parameters.

