
# CIFAR-10 Image Classification using Bidirectional LSTM

This project demonstrates how to perform image classification on the **CIFAR-10 dataset** using a **Bidirectional LSTM (Long Short-Term Memory)** network built with **TensorFlow and Keras**.

Although CNNs are more common for image tasks, this project explores a sequence-based approach by reshaping image data and feeding it into a Bidirectional LSTM model.

---

## Dataset: CIFAR-10
The CIFAR-10 dataset consists of:
- 60,000 color images (32×32)
- 10 classes:
  - Airplane
  - Automobile
  - Bird
  - Cat
  - Deer
  - Dog
  - Frog
  - Horse
  - Ship
  - Truck

Split:
- Training samples: 50,000  
- Testing samples: 10,000  

---

## Project Workflow

1. Load CIFAR-10 dataset
2. Normalize image pixel values
3. Reshape images for LSTM input
4. One-hot encode class labels
5. Build a Bidirectional LSTM model
6. Train and validate the model
7. Evaluate model performance
8. Visualize accuracy and loss
9. Generate predictions

---

## Model Architecture

- Input Layer: (32, 32, 3)
- Reshape Layer: Converts image into sequences
- Forward LSTM: 128 units
- Backward LSTM: 128 units (go_backwards=True)
- Concatenation Layer
- Dense Output Layer: 10 units with Softmax activation

Loss Function:
- Categorical Crossentropy

Optimizer:
- Adam

Evaluation Metric:
- Accuracy

---

## Training Details

- Epochs: 10
- Batch Size: 64
- Validation Data: CIFAR-10 test set

---

## Results

- Training and validation accuracy are plotted across epochs
- Training and validation loss curves help detect overfitting
- Final predictions are generated using the trained model

---

## Libraries Used

- Python 3
- TensorFlow
- Keras
- NumPy
- Matplotlib

---

## How to Run

1. Install dependencies:
   ```bash
   pip install tensorflow numpy matplotlib
   ```

2. Run the Python script containing the model code.

---

## Notes

- This approach treats images as sequences, which is computationally heavier than CNNs.
- Performance may be lower compared to convolution-based architectures.
- Useful for educational and experimental purposes.

---

## Author

Created for academic and learning purposes.
