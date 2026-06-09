# MNIST Digit Classification: Perceptron vs. Artificial Neural Network vs. Convolutional Neural Network

This repository presents a comparative study of three increasingly powerful Deep Learning architectures — a **Single-Layer Perceptron**, a **Multi-Layer Artificial Neural Network (ANN)**, and a **Convolutional Neural Network (CNN)** — on the widely used MNIST handwritten digit dataset.

The objective is to evaluate how model complexity influences classification performance when recognizing handwritten digits from grayscale images.

---

## 🚀 Project Workflow

### 1. Data Acquisition

* Loaded the MNIST training and testing datasets.
* Dataset consists of grayscale handwritten digit images of size **28 × 28 pixels**.
* Each image belongs to one of **10 classes (0–9)**.

### 2. Data Preprocessing

* Separated pixel values and target labels.
* Normalized pixel intensities from **0–255** to **0–1** for faster and more stable training.
* Reshaped image data into:

  * **28 × 28** format for visualization and ANN models.
  * **28 × 28 × 1** format for CNN models.
* Applied one-hot encoding to target labels using categorical representation.

### 3. Data Visualization

* Displayed sample handwritten digit images from the training dataset.
* Verified image-label consistency after preprocessing.

---

## 🧠 Model Development

### Model 1: Single-Layer Perceptron

* Implemented using TensorFlow/Keras Sequential API.
* Architecture:

  * Flatten Layer
  * Dense Output Layer (10 neurons, Softmax activation)
* Optimizer: SGD
* Loss Function: Categorical Crossentropy

### Model 2: Artificial Neural Network (ANN)

* Implemented using TensorFlow/Keras Sequential API.
* Architecture:

  * Flatten Layer
  * Dense Layer (128 neurons, ReLU)
  * Dense Layer (64 neurons, ReLU)
  * Dense Output Layer (10 neurons, Softmax)
* Optimizer: Adam
* Loss Function: Categorical Crossentropy

### Model 3: Convolutional Neural Network (CNN)

* Implemented using TensorFlow/Keras Sequential API.
* Architecture:

  * Conv2D Layer (32 filters)
  * MaxPooling Layer
  * Conv2D Layer (64 filters)
  * MaxPooling Layer
  * Flatten Layer
  * Dense Layer (128 neurons)
  * Dropout Layer (0.5)
  * Dense Output Layer (10 neurons, Softmax)
* Optimizer: Adam
* Loss Function: Categorical Crossentropy

---

## 📊 Results

### Single-Layer Perceptron

The Perceptron establishes a baseline performance by learning a linear mapping between image pixels and digit classes.

**Test Accuracy:** **90.97%**

Key Observations:

* Learns basic digit patterns effectively.
* Limited ability to capture complex spatial relationships.
* Serves as a strong baseline classifier.

---

### Artificial Neural Network (ANN)

The ANN introduces hidden layers that enable the model to learn non-linear decision boundaries.

**Test Accuracy:** **97.78%**

Key Observations:

* Significant improvement over the Perceptron.
* Better feature abstraction through hidden layers.
* Improved generalization on unseen handwritten digits.

---

### Convolutional Neural Network (CNN)

The CNN leverages convolutional filters to automatically learn spatial features such as edges, strokes, and shapes.

**Test Accuracy:** **99.29%**

Key Observations:

* Highest accuracy among all models.
* Captures local image patterns efficiently.
* Most robust architecture for image classification tasks.

---

## 📈 Performance Comparison

| Metric                    | Perceptron | ANN        | CNN                      |
| ------------------------- | ---------- | ---------- | ------------------------ |
| Test Accuracy             | 90.97%     | 97.78%     | 99.29%                   |
| Learning Type             | Linear     | Non-Linear | Spatial Feature Learning |
| Complexity                | Low        | Moderate   | High                     |
| Feature Extraction        | Manual     | Learned    | Automatic                |
| Performance on Image Data | Moderate   | Excellent  | Outstanding              |

---

## 📉 Visualizations Included

The project includes:

* Sample MNIST digit visualization.
* Training vs Validation Accuracy curves.
* Training vs Validation Loss curves.
* Validation Accuracy comparison across all models.
* Side-by-side prediction comparison.
* CNN Confusion Matrix.
* Final Accuracy Comparison Bar Chart.

These visualizations provide insight into model learning behavior and comparative performance.

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn
* TensorFlow
* Keras

---

## 📂 Dataset

The project uses the MNIST Handwritten Digit Dataset containing:

* 70,000 grayscale images
* Image Size: 28 × 28 pixels
* 10 digit classes (0–9)

Target Classes:

```text
0, 1, 2, 3, 4, 5, 6, 7, 8, 9
```

Dataset Files:

* `mnist_train.csv.zip`
* `mnist_test.csv.zip`

---

## 🎯 Conclusion

This comparative study clearly demonstrates how increasing model complexity improves image classification performance.

* The **Perceptron** provides a simple baseline with respectable accuracy.
* The **ANN** significantly improves performance by learning non-linear representations.
* The **CNN** achieves near-human-level accuracy by automatically extracting meaningful spatial features from images.

The results highlight why Convolutional Neural Networks have become the standard architecture for computer vision and image recognition tasks.
