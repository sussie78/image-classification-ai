

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

