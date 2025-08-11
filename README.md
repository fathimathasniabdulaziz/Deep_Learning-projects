# Deep_Learning-projects
Deep learning projects
Flower Classification with TensorFlow
📌 Project Overview
This project is a deep learning image classification model built with TensorFlow that can classify images of flowers into five categories:

Daisy 🌼

Dandelion 🌻

Rose 🌹

Sunflower 🌞

Tulip 🌷

It uses a Convolutional Neural Network (CNN) to automatically learn patterns and features from images without manual feature engineering.

📂 Dataset
The dataset is the TensorFlow Flowers Dataset which contains thousands of labeled flower images.

Total Classes: 5

Image Size: 180×180 pixels

Color Mode: RGB

Split: 80% training, 20% validation

🛠 Tech Stack
Python 3

TensorFlow / Keras

Matplotlib

NumPy

🚀 How It Works
Data Loading – Downloads the dataset and splits it into training & validation sets.

Preprocessing – Resizes images, normalizes pixel values to 0–1.

Model Building – Creates a CNN with convolution, pooling, flatten, and dense layers.

Training – Uses the Adam optimizer and Sparse Categorical Crossentropy loss.

Evaluation – Measures accuracy on unseen validation data.

Prediction – Model predicts the class of any given flower image.

📜 Code Example
python
Copy
Edit
model = tf.keras.Sequential([
    tf.keras.layers.Rescaling(1./255),
    tf.keras.layers.Conv2D(16, 3, activation='relu'),
    tf.keras.layers.MaxPooling2D(),
    tf.keras.layers.Conv2D(32, 3, activation='relu'),
    tf.keras.layers.MaxPooling2D(),
    tf.keras.layers.Conv2D(64, 3, activation='relu'),
    tf.keras.layers.MaxPooling2D(),
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(128, activation='relu'),
    tf.keras.layers.Dense(5, activation='softmax')
])
📊 Results
After 5 epochs, the model achieves:

Training Accuracy: ~87%

Validation Accuracy: ~78%

Example prediction:

makefile
Copy
Edit
Predicted: sunflower
Actual: sunflower
