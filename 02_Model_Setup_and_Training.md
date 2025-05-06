# AI Model Setup and Training (L02)

## Development Environment Setup

Conceptual Setup of Development Environment
Part 1: Research and Documentation
Python Installation
I downloaded Python from, installed it, and ensured “Add Python to PATH” was checked. I verified the installation with:
python --version
To manage dependencies, I created a virtual environment:
TensorFlow and TensorFlow Lite Installation
I used pip to install TensorFlow and TensorFlow Lite:
I verified the installation in Python by checking TensorFlow’s version.
Jupyter Notebook Installation
I installed Jupyter Notebook with:
This opened an interactive environment for running Python code.
Part 2: Conceptual AI Model Design
Neural Network for MNIST
I designed a neural network using Keras for the MNIST dataset:
Input Shape: (28, 28)
Layers: Flatten → Dense(128, ReLU) → Dense(10, Softmax)
Loss Function: Sparse categorical cross-entropy
Optimizer: Adam
Data Loading and Preprocessing
I loaded the MNIST dataset and normalized pixel values to [0, 1]:
Model Training
I compiled the model with accuracy as the metric and trained it for 10 epochs:
Part 3: Model Conversion and Saving
TensorFlow Lite Conversion
I converted the trained Keras model to TensorFlow Lite using:
I saved the converted model as model.tflite.
Part 4: Model Deployment
Deployment and Testing
I loaded the TensorFlow Lite model and allocated tensors:
I tested it with sample input and retrieved the output. This process simulates running AI on edge devices.
Reflective Journal
Challenges I Faced
Understanding TensorFlow Lite conversion and managing Python environments was tricky at first.
What I Learned
I gained practical knowledge of installing tools, creating neural networks, and deploying models on edge devices.
Application
I can now build AI-powered mobile apps and IoT projects using TensorFlow Lite for real-world applications.

---

# Model Training, Deployment, and Reflections (L03)

Step 1: Set Up the Environment
Install Python:
I downloaded and installed Python from Python's official website.
Install VS Code:
I downloaded and installed Visual Studio Code from VS Code's official website.
Install TensorFlow:
I opened a terminal in VS Code and ran:
Install Edge Impulse CLI:
I installed Node.js and npm from Node.js' official website. Then, I ran the following command in the terminal:
Step 2: Prepare the Dataset
Load and Preprocess the Data:
I created a new Python file in VS Code and wrote the following code to load and preprocess the MNIST dataset:
Step 3: Train a Simple AI Model
Define the Model:
model = tf.keras.Sequential([
    tf.keras.layers.Conv2D(32, (3, 3), activation='relu', input_shape=(28, 28, 1)),
    tf.keras.layers.MaxPooling2D((2, 2)),
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(128, activation='relu'),
    tf.keras.layers.Dense(10, activation='softmax')
])
Compile the Model:
Train the Model:
model.fit(x_train, y_train, epochs=5, validation_data=(x_test, y_test))
Step 4: Convert and Deploy the Model
Convert the Model to TFLite:
Simulate the Edge Device:
I followed the instructions provided by Edge Impulse to simulate the edge device environment and tested the deployed model.
Step 5: Test and Validate the Model
Run Inference on the Simulated Edge Device:
I used the Edge Impulse platform to run inference and validate the model performance.
I analyzed the results and made necessary adjustments.
Personal Reflections:
This exercise was a valuable learning experience for me. Setting up the environment and installing the necessary tools was straightforward, but I encountered some minor challenges while installing dependencies due to compatibility issues. 
Training the AI model helped me reinforce my understanding of neural networks and how they process data. Converting the model to TFLite and deploying it to a simulated edge device was particularly interesting, as it highlighted the differences between running AI models in cloud environments versus edge devices.
Through this process, I realized the importance of optimizing AI models for performance and efficiency, especially when deploying on resource-constrained devices. I also found debugging to be an essential skill, as I had to troubleshoot errors while uploading the model to Edge Impulse. 
Overall, this project gave me a deeper appreciation for edge computing and its potential applications in real-world scenarios.
