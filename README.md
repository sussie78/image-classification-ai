This dataset contains images of circles and squares for training an image classification model.  

---

## 📂 Dataset Structure  
The dataset is available as a ZIP file. After extracting, it follows this structure:  

dataset/ ├── circles/ # Images of circles ├── squares/ # Images of squares

---

## 📥 How to Use the Dataset  

### **1️⃣ Download & Extract the ZIP File**  
1. Click on the ZIP file in this repository and **download it**.  
2. Extract the ZIP file to get the `dataset/` folder.  
3. Use the dataset for training your AI model.  

### **2️⃣ Load the Dataset in Python**  
You can check the dataset structure using this Python code:  
```python
import os

dataset_path = "path_to_extracted_folder/dataset"

# List available classes
print("Classes:", os.listdir(dataset_path))

1️⃣ Dataset Size & Image Details
How many images are in each category?
What is the resolution of the images?
Are the images synthetic or real-world?

## 📊 Dataset Details  
- Total Images: 100 (50 Circles, 50 Squares)  
- Image Format: PNG  
- Resolution: 128x128 pixels  
- Type: Synthetic (Generated for training purposes)  

## 🏆 Model Performance  
After training a simple CNN model for 10 epochs, the results were:  
- **Training Accuracy:** 95%  
- **Validation Accuracy:** 92%  
- **Loss:** 0.08  

📌 *Your results may vary depending on training parameters.*  

## 🔍 Making Predictions with the Trained Model  
Once the model is trained, you can test it on new images:  

```python
import tensorflow as tf
from tensorflow.keras.preprocessing import image
import numpy as np

# Load the trained model
model = tf.keras.models.load_model("shape_classifier_model.h5")

# Load and preprocess a test image
img_path = "test_images/sample.png"  # Replace with an actual test image path
img = image.load_img(img_path, target_size=(128, 128))
img_array = image.img_to_array(img) / 255.0
img_array = np.expand_dims(img_array, axis=0)

# Make a prediction
prediction = model.predict(img_array)
print("Prediction:", "Circle" if prediction[0][0] < 0.5 else "Square")






















