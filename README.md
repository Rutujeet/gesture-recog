## Static Gesture Recognition

Gesture recognition enables computers to interpret human movements, essential for applications like Sign Language Translation where hand gestures are converted into spoken words.

### Dataset

- **Source**: [Sign Language MNIST dataset](https://www.kaggle.com/datasets/datamunge/sign-language-mnist)
- **Labels**: 0-25, representing A-Z (excluding J and Z).
- **Training Set**: 27,455 images
- **Test Set**: 7,172 images
- **Image Format**: Each image is 28x28 pixels, represented by 784 grayscale values (0-255).

### Data Preprocessing

- **Loading Data**: CSV files are loaded into pandas DataFrames.
- **Dataset Class**: `SignLanguageDataset` is defined to handle data conversion:
  - Images are reshaped to 28x28 with one channel and normalized to [0, 1].
  - Labels are one-hot encoded.
- **Data Loaders**: `DataLoader` instances are created for both training and test datasets with a batch size of 100.

### Model

- **Framework**: PyTorch
- **Architecture**: The Convolutional Neural Network (CNN) includes:
  - Convolutional Layer with 8 filters
  - Max Pooling
  - Convolutional Layer with 16 filters
  - Max Pooling
  - Flattening
  - Fully Connected Layer
  - Output Layer
- **Loss Function**: `BCEWithLogitsLoss`, which combines `Sigmoid` and `Binary Cross Entropy Loss`.
- **Optimizer**: Adam with learning rate 0.001

### Training and Evaluation

- **Training**: The model is trained for 100 epochs. Training loss and accuracy are printed for each epoch.
- **Evaluation**:
  - **Training Accuracy**: Calculated after each epoch.
  - **Test Accuracy**: Calculated after the final epoch.

### Results

- **Training Accuracy**: 98.47%
- **Test Accuracy**: 88.24%
