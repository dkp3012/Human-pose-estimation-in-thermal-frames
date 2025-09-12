# 🤖 Human Pose Estimation in Thermal Frames using Deep Learning Techniques

This project focuses on detecting humans and estimating their poses in thermal images using deep learning models like YOLOPose. Thermal images are challenging due to lack of color and texture, but essential in environments where standard RGB cameras fail—like night surveillance, healthcare monitoring, and disaster response.

---

## 📄 Citation

If you use this project in your work, please cite:

**Dhananjay Kumar Prasad (2024).** *Human Pose Estimation in Thermal Frames using Deep Learning Techniques*.  
International Journal of Intelligent Systems and Applications in Engineering, 12(23s), 3713–.  
[https://ijisae.org/index.php/IJISAE/article/view/7845](https://ijisae.org/index.php/IJISAE/article/view/7845)

---

## 🚀 Project Goals

✔ Detect humans in thermal frames  
✔ Extract pose keypoints in COCO format  
✔ Handle noisy and low-contrast data  
✔ Apply data augmentation tailored for thermal imagery  
✔ Convert annotations to YOLO format  
✔ Train models with custom hyperparameters  
✔ Visualize keypoints, metrics, and action classification  
✔ Store results in structured formats for easy analysis

---

## 📂 Dataset Overview

### 🔢 Action Classes  
The dataset consists of thermal images organized by human actions:

- 🟥 **Abnormal**  
- 🟠 **Leg_stretching**  
- 🟡 **Lying**  
- 🟢 **Push-ups**  
- 🔵 **Sitting**  
- 🟣 **Sitting_crosslegs**  
- 🟤 **Sit-ups**  
- ⚪ **Standing**  
- ⚫ **Walking**

### 📁 Folder Structure

data/
├── images/
│ ├── train/
│ ├── val/
│ └── test/
└── json_labels/
├── train/
├── val/
└── test/



### 📋 Annotation Format

Each JSON file contains:

- ✅ `class`: action label  
- ✅ `bbox`: normalized coordinates `[x_center, y_center, width, height]`  
- ✅ `keypoints`: 17 points, each `[x, y, confidence]`, normalized between 0 and 1  

This structure ensures compatibility with YOLOPose and downstream applications.

---

## 🔧 Dataset Processing Pipeline

### 1️⃣ Annotation Conversion  
JSON annotations are transformed into YOLO format `.txt` files containing bounding boxes and keypoints.

### 2️⃣ Data Augmentation  
Augmentations help the model learn from noisy and diverse samples:

- 🔄 Horizontal flip  
- ➕ Gaussian noise  
- 📏 Resize transformations  

### 3️⃣ Dataset Splitting  
Automatically split into:

- 📂 70% training  
- 📂 20% validation  
- 📂 10% testing  

### 4️⃣ Data Cleaning  
Images without detectable humans are removed to ensure meaningful training.

### 5️⃣ CSV Generation  
All annotations are exported to a CSV file for inspection and analysis.

---

## ⚙ Installation

### 📦 Requirements

- Python 3.8+
- PyTorch 1.12 or newer
- OpenCV, NumPy, pandas, matplotlib
- Optional: wandb for experiment tracking

### 💻 Install Dependencies

```bash
pip install -r requirements.txt
