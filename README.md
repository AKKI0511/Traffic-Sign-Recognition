# Model Accuracy

![Screenshot 2024-05-03 173319](https://github.com/AKKI0511/Traffic-Sign-Recognition/assets/120317569/0f3f74b6-75c1-4a20-9636-35c7cf0b24ea)

## Experimentation Steps

1. **Base Model:**
   - I started with a basic convolutional neural network (CNN) architecture consisting of three convolutional layers with max-pooling, followed by a densely connected layer and an output layer.
   - The model was compiled using the Adam optimizer and categorical crossentropy loss.

2. **Filter Sizes and Pooling:**
   - I experimented with different filter sizes in convolutional layers (e.g., (3, 3), (5, 5)) to capture various image features.
   - Adjusted max-pooling sizes to control downsampling.

3. **Hidden Layers and Dropout:**
   - Introduced a dense hidden layer with 512 units and experimented with dropout (0.5) to prevent overfitting.
   - Tried different sizes and numbers of hidden layers for feature extraction.

4. **Activation Functions:**
   - Experimented with activation functions, starting with ReLU for convolutional layers and softmax for the output layer.
   - Tried alternatives like Leaky ReLU and tanh for hidden layers.

5. **Optimizers and Learning Rates:**
   - Explored different optimizers (e.g., Adam, SGD) and learning rates to observe convergence speed and final accuracy.

## Observations

- **What Worked Well:**
  - The base model with a simple CNN architecture provided a reasonable starting point.
  - Increasing model complexity with additional hidden layers improved the model's ability to capture intricate features.

- **What Didn't Work Well:**
  - Extremely deep architectures led to overfitting, highlighting the importance of dropout for regularization.
  - Larger filter sizes resulted in longer training times without significant accuracy improvement.

- **General Notes:**
  - Adam optimizer consistently performed well in terms of convergence speed and final accuracy.
  - Experimenting with various hyperparameters is crucial, but it requires careful monitoring of training and validation performance.

## Conclusion

The experimentation process was insightful, emphasizing the importance of balancing model complexity and overfitting. The final model employs a moderately deep architecture with suitable dropout, filter sizes, and pooling, achieving satisfactory accuracy on the traffic sign recognition task.
