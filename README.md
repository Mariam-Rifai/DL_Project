# DL_Project
# CNN Binary Classification on MNIST (0 vs 1)

## Description
This project implements a simple Convolutional Neural Network (CNN) using PyTorch to classify handwritten digits from the MNIST dataset.

The model is trained as a binary classifier to distinguish between:
- Digit 0
- Digit 1

We also compare the performance of two optimizers:
- Adam
- SGD



## Dataset
We use the MNIST dataset from torchvision and filter it to keep only:
- Class 0
- Class 1

Data is loaded using PyTorch DataLoader with batch size = 32.



## Model Architecture (SimpleCNN)

The CNN consists of:

### Convolutional Layers
- Conv2D: 1 → 16 filters (3x3)
- ReLU
- MaxPooling (2x2)

- Conv2D: 16 → 32 filters (3x3)
- ReLU
- MaxPooling (2x2)

### Fully Connected Layers
- Flatten
- Linear (32×7×7 → 64)
- ReLU
- Dropout (0.5)
- Linear (64 → 1 output)



## Training Details

- Loss Function: BCEWithLogitsLoss
- Epochs: 5
- Batch Size: 32

### Optimizers Compared:
- Adam (lr = 0.001)
- SGD (lr = 0.01)



## Evaluation

The model evaluates:
- Training Loss
- Training Accuracy
- Validation Loss
- Validation Accuracy

Predictions are made using:
sigmoid(output) > 0.5


## Visualization

The project plots:
- Loss curves (Train vs Validation)
- Accuracy curves (Train vs Validation)

using Matplotlib.



## Results

Final accuracy is printed for both optimizers:
- Adam Accuracy:99.95%
- SGD Accuracy:99.86%





## Author
Mariam yaser
