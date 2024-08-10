# Static Gesture Recognition

Gesture recognition helps computers interpret human movements, crucial for Sign Language Translation, where hand gestures turn into spoken words.

## Dataset:
- Similar to MNIST, with labels (0-25) for A-Z (excluding J and Z).
- Training set: 27,455 cases. Test set: 7,172 cases.
- Each 28x28 pixel image is represented by 784 grayscale values (0-255).

## Data Preprocessing:
- Split features (pixels) from labels.
- Reshape features to match image format.
- Apply One Hot Encoding to labels.

## Model:
- Built using Keras with a simple CNN (Convolutional Neural Network).
- The CNN consists of 7 layers:
  1. Convolutional Layer with ReLU
  2. Max Pooling
  3. Convolutional Layer with ReLU
  4. Max Pooling
  5. Flattening
  6. Fully Connected Layer with ReLU
  7. Output Layer with Sigmoid

## Results:
- Training Set Accuracy: 96.06%
- Test Set Accuracy: 87.77%

Suggestions are always welcome!
