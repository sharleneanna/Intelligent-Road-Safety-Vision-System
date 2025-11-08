# 🚗 AutoSafeDrive AI – Intelligent Road Safety Vision System  
**AICTE × Shell × Edunet Foundation Internship (AI/ML in Automotive)**  
Developed by **Sharlene Anna Pereira**

---

## 📘 Overview  
**AutoSafeDrive AI** is an intelligent vision-based assistant that analyzes real road environments and estimates driving risk levels using deep learning.  
Powered by **YOLOv8 (Ultralytics)**, it detects vehicles, pedestrians, and road hazards, computes risk levels, and displays visual safety alerts — forming a prototype for an AI-powered Advanced Driver Assistance System (ADAS).

This project is part of the **AICTE Edunet Internship (AI/ML in Automotive)** initiative and represents the **Week 2 milestone (90% completion)**.

---

## 🧠 Features (Week 2 PRO Build)

| Feature | Description | Why It’s Impressive |
|----------|--------------|--------------------|
| 🚘 **Zero-Shot Object Detection** | Pretrained YOLOv8n detects cars, buses, trucks, bikes, pedestrians, and traffic lights. | Fast & transferable — no extra labeling required. |
| 📦 **Indian Driving Dataset (IDD)** | Uses real Indian traffic data from Kaggle’s *New IDD Dataset*. | Localized data → realistic Indian road conditions. |
| ⚠️ **Dynamic Risk Estimation** | Calculates proximity-based risk for each object and overall scene. | Converts perception → analytics → safety logic. |
| 🟥 **Visual Risk Overlay** | Color-coded safety zones: Green (Safe), Yellow (Caution), Red (Danger). | Easy to understand for drivers & evaluators. |
| 📊 **Risk Analytics Dashboard** | Auto-generates histograms & CSV logs for analysis. | Demonstrates applied data-driven decision making. |
| 🧩 **Gradio Web App** | Interactive interface for live demos & image uploads. | User-friendly and deployable for real-world use. |
| 🖼️ **Pre-Annotated Samples** | Automatically generates annotated IDD frames. | Instant visual proof-of-concept. |
| 🔗 **Full ML Workflow** | Dataset → Inference → Risk Metrics → Visualization → UI. | End-to-end AI engineering pipeline. |

---

## 🧩 System Workflow  

```mermaid
graph TD
    A[📦 IDD Dataset (KaggleHub)] --> B[🚘 YOLOv8n Inference]
    B --> C[⚙️ Risk Scoring Engine]
    C --> D[📊 CSV + Plots Generation]
    C --> E[🧩 Gradio Dashboard Interface]
    E --> F[👀 User Visualization & Interaction]

