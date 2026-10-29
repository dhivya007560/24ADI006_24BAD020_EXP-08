# 24ADI006_24BAD020_EXP-08

# Experiment No. 8: Train a Simple Autoencoder for Dimensionality Reduction and Feature Learning

##  Aim
To implement and train a simple autoencoder using the MNIST handwritten digit dataset, learn a lower-dimensional representation of input images, and evaluate the model by reconstructing the original images.

##  Dataset
The MNIST dataset contains handwritten digit images from 0 to 9.

- Training images: 60,000
- Testing images: 10,000
- Image size: 28 × 28 pixels
- Original input features: 784
- Latent features: 32

Dataset source: https://www.tensorflow.org/datasets/catalog/mnist

##  Methodology

### Part A: Dataset Preparation and Preprocessing
1. Load the MNIST dataset using TensorFlow/Keras.
2. Display sample handwritten digit images.
3. Normalize pixel values to the range 0 to 1.
4. Flatten each 28 × 28 image into a 784-dimensional vector.
5. Use the input images as both input and target output.

### Part B: Encoder and Decoder Implementation
1. Define an input layer with 784 features.
2. Create the encoder using Dense layers with ReLU activation.
3. Reduce the input to a latent representation of 32 features.
4. Create the decoder using Dense layers.
5. Use sigmoid activation in the output layer to reconstruct 784 pixel values.
6. Combine the encoder and decoder into an autoencoder model.

### Part C: Model Compilation and Training
1. Compile the model using the Adam optimizer.
2. Use binary cross-entropy as the reconstruction loss.
3. Train the model for 10 epochs with a batch size of 256.
4. Validate the model using the test dataset.
5. Plot the training and validation loss curves.

### Part D: Dimensionality Reduction and Reconstruction
1. Pass test images through the trained encoder.
2. Extract 32-dimensional latent feature vectors.
3. Pass the latent vectors through the decoder.
4. Compare original and reconstructed images.
5. Evaluate reconstruction performance using loss values and visual inspection.
6. Save the trained autoencoder model.

##  Model Architecture

**Input (784 features) → Dense (128, ReLU) → Latent Layer (32, ReLU) → Dense (128, ReLU) → Output (784, Sigmoid)**

The encoder reduces the number of features from 784 to 32, while the decoder reconstructs the image from the compressed representation.

##  Technologies Used
- Python for programming
- TensorFlow/Keras for building and training the autoencoder
- NumPy for numerical operations
- Matplotlib for visualizing images and loss curves
- MNIST for handwritten digit images

##  Expected Output
- Display sample MNIST images.
- Print training and testing dataset dimensions.
- Display encoder, decoder, and autoencoder model summaries.
- Show training and validation loss for each epoch.
- Plot training and validation loss curves.
- Display original and reconstructed images side by side.
- Print the original dimension (784) and latent dimension (32).
- Save the trained model as `autoencoder_mnist.keras`.

##  Result
A simple autoencoder is implemented and trained using the MNIST dataset. The encoder learns a compressed 32-dimensional representation from the original 784-dimensional input, and the decoder reconstructs the handwritten digit images. The reconstruction loss and visual comparison are used to evaluate the model's performance.

##  Conclusion
The experiment demonstrates how an autoencoder performs dimensionality reduction and feature learning. It shows how important information can be represented in a smaller latent space and used to reconstruct the original input images.


