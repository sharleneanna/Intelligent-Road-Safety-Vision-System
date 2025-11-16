# 🚗 AutoSafeDrive ADAS

### **Intelligent Road Safety Vision System using YOLOv8 + Risk Estimation**

AutoSafeDrive ADAS is an AI-powered visual perception system that analyzes real-world road scenes and estimates driving risk using object detection and an intelligent risk scoring engine.
This project is built as part of the **AICTE × Shell × Edunet Foundation – AI/ML in Automotive Internship**.

🔥 **This repository contains the final submission version with:**

* YOLOv8-based object detection
* Risk scoring engine
* Vulnerable road-user emphasis
* Automatic dataset loading (Kaggle Hub)
* Batch evaluation & analytics
* Clean annotated outputs
* Interactive Gradio web app
* End-to-end Colab-ready script

---

## 📌 Project Overview

Modern Advanced Driver Assistance Systems (ADAS) rely on computer vision to understand the environment around a vehicle.
**AutoSafeDrive ADAS** simulates such perception using deep learning—detecting road users (cars, trucks, pedestrians, cyclists, etc.) and estimating scene-level risk.

The system is built for real-time insights and research use-cases, focusing on:

* Threat recognition
* Collision-risk evaluation
* Road safety analysis
* Visual decision support

---

# 🧠 Features

| Feature                               | Description                                                                               |
| ------------------------------------- | ----------------------------------------------------------------------------------------- |
| **🚘 Object Detection (YOLOv8)**      | Detects cars, bikes, buses, pedestrians, trucks, and traffic lights.                      |
| **⚠️ Dynamic Risk Estimation**        | Computes risk based on object size (proximity), vulnerability, and bounding box position. |
| **🟥 Visual Annotations**             | Color-coded bounding boxes: Green (Safe), Yellow (Caution), Red (Danger).                 |
| **📊 Batch Evaluation & Analytics**   | Generates annotated dataset, CSV logs, and risk histogram.                                |
| **📦 Automatic IDD Dataset Download** | Fetches the Indian Driving Dataset using KaggleHub.                                       |
| **🖥️ Gradio Web App**                | User-friendly UI for interactive image analysis.                                          |
| **🔧 Lightweight Tracking**           | Maintains detection consistency using simple IoU tracking.                                |
| **🎯 One-Cell Colab Execution**       | Fully runnable in a single notebook cell.                                                 |

---

# 📂 Project Structure

```
AutoSafeDrive/
│
├── autosafedrive_outputs/
│   ├── annot_*           # Annotated images
│   ├── eval_*.csv        # Risk scoring log
│   └── risk_hist.png     # Risk distribution plot
│
├── data/
│   └── idd/              # Downloaded IDD dataset (via KaggleHub)
│
└── AutoSafeDrive_Final.ipynb  # Full one-cell script
```

---

# 🛠️ How It Works

### 1. **Dataset Handling**

The script automatically downloads the **Indian Driving Dataset (IDD)** using KaggleHub.
A small subset (20 images) is prepared for evaluation.

### 2. **YOLOv8 Object Detection**

Using `yolov8n.pt`, the system detects:

* Cars
* Trucks
* Buses
* Motorcycles
* Bicycles
* Pedestrians
* Traffic lights

### 3. **Risk Engine**

Risk = f(proximity, vulnerability)

* **Close objects → higher risk**
* **Pedestrians, bicycles, motorcycles → extra risk +15**
* Risk scale:

  * **0–35:** SAFE
  * **36–65:** CAUTION
  * **66–100:** DANGER

### 4. **Annotation System**

The pipeline draws:

* Bounding boxes
* Class + confidence
* Per-object risk
* Overall risk banner on the image

### 5. **Batch Evaluation**

Generates:

* Annotated images
* eval.csv
* Histogram for risk distribution

### 6. **Gradio Demo**

Interactive web interface to upload images and see real-time ADAS annotations.

---

# 📸 Example Output

> *(You can upload sample annotated outputs from autosafedrive_outputs/ once you run the script.)*

---

# ▶️ Run Locally or on Colab

### **Google Colab (Recommended)**

1. Open a new notebook
2. Paste the full one-cell script from this repo
3. Run
4. Gradio demo auto-launches

### Requirements

```
ultralytics
opencv-python-headless
pandas
matplotlib
tqdm
gradio
kagglehub
```

---

# 🧪 Risk Formula (Simplified)

```
proximity = (bbox_height / image_height) * 100
vulnerable_bonus = 15 if class in ["person","bicycle","motorcycle"]
risk = prox*0.6 + vulnerable_bonus
risk = clipped to [0,100]
```

This produces realistic near-collision indicators for ADAS-like systems.

---

# 🚀 Results

### ✔ 100% automated pipeline

### ✔ Strong ADAS logic

### ✔ Professional annotated outputs

### ✔ Accurate risk distribution

### ✔ Easy to demonstrate in viva/interview

---

# 📘 Future Improvements

* Driver drowsiness detection
* Lane segmentation using deep models
* Distance estimation through monocular depth
* Video-based temporal risk prediction
* Multi-frame collision prediction (TTC-based)
* On-device optimization (TensorRT/ONNX)

---

# 🙋‍♀️ Author

**Sharlene Anna Pereira**
AI/ML in Automotive (AICTE × Shell × Edunet Foundation)
B.Tech CSE (AIML)

---
