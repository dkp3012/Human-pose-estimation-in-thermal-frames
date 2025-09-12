# 🤖 Human Pose Estimation in Thermal Frames using Deep Learning Techniques

![Thermal Pose](images/examples/indoor_sitting.png)

Detect humans and estimate their poses in **thermal images** using **YOLOPose**. Thermal imaging is challenging due to lack of color and texture, but crucial in environments where RGB cameras fail—🌙 night surveillance, 🏥 healthcare monitoring, 🌪️ disaster response.  

This project focuses on:

- 🧍 Human detection  
- 🔑 Estimation of 17 keypoints per person  
- 🎯 Classification into **9 predefined action classes**

The **Thermal-IM dataset** of 9,414 annotated frames from 53 videos supports model training and evaluation. The study highlights **dataset construction, keypoint annotation, and model performance** on thermal human activities.

---

# 📚 Published Paper

**Dhananjay Kumar Prasad. (2024). Human Action Recognition in Thermal Images Using Pose Estimation.**  
*International Journal of Intelligent Systems and Applications in Engineering, 12(23s), 3713–.*  
[🔗 View Article](https://ijisae.org/index.php/IJISAE/article/view/7845)

---

## 📂 Thermal-IM Dataset

**Thermal-IM contains 9,414 thermal images extracted from 53 videos**, annotated with 17 COCO-style keypoints across 9 human action classes, ready for YOLOv8-Pose training and evaluation.  

[📥 Download Dataset](YOUR_GOOGLE_DRIVE_LINK)

**Dataset Summary:**

| 📌 Feature             | ℹ️ Details |
|-----------------------|------------|
| 🎥 Videos             | 53         |
| 🖼️ Resolution         | 288×384 px |
| ⏱️ Frame rate          | 15 FPS     |
| 🔑 Keypoints           | 17 COCO-style |
| 🏷️ Action Classes      | Abnormal, Leg_stretching, Lying, Push-ups, Sit-ups, Sitting, Sitting_crosslegs, Standing, Walking |
| 🖼️ Total Frames        | 9,414      |

---

## 🏃 Sample Action

### Indoor Single-Person Activity
![Indoor action example](images/examples/indoor_sitting.png)

---

## 📄 Citation

If you use this project in your work, please cite:

**Dhananjay Kumar Prasad (2024).** *Human Pose Estimation in Thermal Frames using Deep Learning Techniques*.  
International Journal of Intelligent Systems and Applications in Engineering, 12(23s), 3713–.  
[🔗 https://ijisae.org/index.php/IJISAE/article/view/7845](https://ijisae.org/index.php/IJISAE/article/view/7845)

---

## 🚀 Quick Start

```bash
# Install dependencies
pip install ultralytics torch torchvision opencv-python
