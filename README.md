# Handwritten Character Recognition

## Overview
This project involves building a Machine Learning pipeline to recognize handwritten digits using a Convolutional Neural Network (CNN). The project is built for the CodeAlpha internship Task 3.

## Dataset
This project uses the **MNIST** dataset.
- 60,000 training images
- 10,000 test images
- 28x28 grayscale images
- 10 classes corresponding to handwritten digits 0-9

## Technologies
- Python
- TensorFlow/Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Model
The CNN architecture used consists of the following structure:
- 2D Convolution (32 filters, 3x3) + ReLU
- Max Pooling (2x2)
- 2D Convolution (64 filters, 3x3) + ReLU
- Max Pooling (2x2)
- Flatten
- Dense (128 units) + ReLU
- Dropout (0.3)
- Dense (10 units) + Softmax (Output)

## Preprocessing
- The pixel values are normalized from the range `0-255` to `0.0-1.0`.
- Images are reshaped to add a channel dimension, becoming `(28, 28, 1)`, as required by the 2D Convolutional layers.

## Evaluation
The model was evaluated on the untouched MNIST test set of 10,000 images, yielding the following results:
- **Test Accuracy**: 0.9933
- **Weighted Precision**: 0.9933
- **Weighted Recall**: 0.9933
- **Weighted F1 Score**: 0.9933

## Results
The trained CNN model, along with visualization graphs, is stored in the corresponding folders:
- **Training History**: `results/training_history.png`
- **Confusion Matrix**: `results/confusion_matrix.png`
- **Sample Predictions**: `results/sample_predictions.png`
- **Final Trained Model**: `models/best_handwritten_character_model.keras`
- **Actual Final Metrics**: `results/metrics.txt`

## How to Run
1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the Jupyter Notebook to train and evaluate the CNN model:
   - Open `Handwritten_Character_Recognition.ipynb` in a Jupyter environment.
   - Run all cells.

## Conclusion
The project successfully developed a Deep Learning solution to identify handwritten digits from the MNIST dataset using a simple yet powerful Convolutional Neural Network architecture, achieving a robust final test accuracy of 99.33%. The model generalizes well and can be reliably loaded for inference on new images.

