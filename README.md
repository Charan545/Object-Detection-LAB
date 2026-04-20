# 🌍 Disaster Image Analysis using Computer Vision

### (Feature Extraction + Feature Matching + Object Detection)

---

## 📌 Overview

This project implements a complete **Computer Vision pipeline** for analyzing disaster images such as floods, earthquakes, and fires.

It is divided into two main parts:

### 🔹 Part I: Image Processing & Feature Engineering

* Preprocessing noisy disaster images
* Feature extraction using keypoint detectors
* Feature matching between images

### 🔹 Part II: Object Detection & Analysis

* Object detection using YOLO / RetinaNet
* Performance evaluation using IoU and detection metrics
* Robustness analysis under extreme conditions

---

## 🧠 Concepts Used

* Image Denoising (Gaussian, Median, Bilateral Filtering)
* Feature Detection & Description
* SIFT (Scale & rotation invariant features)
* Feature Matching using Brute-Force Matcher
* Deep Learning-based Object Detection using YOLO / RetinaNet
* Evaluation using Intersection over Union

---

## ⚙️ Technologies Used

* Python
* OpenCV
* PyTorch / Torchvision
* NumPy
* Matplotlib
* Google Colab

---

# 🔹 Part I: Image Processing Pipeline

## 1️⃣ Preprocessing Noisy Images

Disaster images often contain noise due to poor lighting, weather conditions, or sensor limitations.

### Techniques Used:

* **Gaussian Filter** → Smooths general noise
* **Median Filter** → Removes salt-and-pepper noise
* **Bilateral Filter** → Preserves edges while denoising

### Outcome:

* Improved image quality
* Better feature detection accuracy

---

## 2️⃣ Feature Extraction

Feature extraction identifies important regions like edges, corners, and textures.

### Method Used:

* **SIFT (Scale-Invariant Feature Transform)**

### Key Advantages:

* Invariant to scale and rotation
* Robust to illumination changes
* Effective for real-world disaster scenes

### Output:

* Keypoints (important locations)
* Descriptors (numerical representation of features)

---

## 3️⃣ Feature Matching

Feature matching finds correspondences between two images.

### Method Used:

* **Brute-Force Matcher** with Lowe’s Ratio Test

### Steps:

1. Compare descriptors from two images
2. Find nearest neighbors
3. Apply ratio test to remove false matches

### Applications:

* Change detection (before vs after disaster)
* Image alignment
* Damage assessment

---

# 🔹 Part II: Object Detection Pipeline

## 1️⃣ Object Detection (YOLO / RetinaNet)

This project uses deep learning-based object detection to identify objects in disaster scenes.

### Models:

* **YOLO (You Only Look Once)** → Fast, real-time detection
* **RetinaNet** → High accuracy with Focal Loss

### Working:

* Input image → Neural Network
* Output → Bounding boxes + confidence scores

### Use Cases:

* Detect damaged buildings
* Identify fire, debris, vehicles
* Assist rescue operations

---

## 2️⃣ Evaluation Metrics

### 📊 Intersection over Union (IoU)

IoU measures overlap between predicted and ground truth boxes.

$$
IoU = \frac{Area\ of\ Overlap}{Area\ of\ Union}
$$

### Other Metrics:

* Precision
* Recall
* mAP (mean Average Precision)

### Interpretation:

* High IoU → Accurate detection
* Low IoU → Poor localization

---

## 3️⃣ Robustness Analysis

To test model reliability, images are modified under extreme conditions:

### Conditions Tested:

* Noise (Gaussian noise)
* Blur (Gaussian blur)
* Low-light (darkened images)

### Observations:

* Noise → Increases false detections
* Blur → Misses fine features
* Low-light → Reduces confidence scores

### Conclusion:

* Models perform well in normal conditions
* Performance degrades in extreme environments

---

## 📁 Project Structure

```
disaster-image-analysis/
│── part1_feature_pipeline.py
│── part2_detection.py
│── README.md
│── requirements.txt
│── images/
│   ├── input/
│   ├── output/
```

---

## ▶️ How to Run

### Step 1: Install Dependencies

```
pip install -r requirements.txt
```

### Step 2: Run Part I

```
python part1_feature_pipeline.py
```

### Step 3: Run Part II

```
python part2_detection.py
```

---

## 📊 Results

* Clear noise reduction using filters
* Accurate feature matching between images
* Successful object detection using YOLO/RetinaNet
* Noticeable performance drop in extreme conditions

---

## 🚀 Applications

* Disaster damage assessment
* Satellite image comparison
* Rescue and emergency planning
* Smart surveillance systems

---

## 💡 Future Improvements

* Use custom-trained datasets for disaster detection
* Improve robustness using data augmentation
* Deploy as a web application
* Integrate real-time drone footage analysis

---

## 👨‍💻 Author

**Allagadda Charan**
B.Tech – AI & Data Science

---

## 📜 License

This project is for academic and educational purposes.
