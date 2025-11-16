
# AutoSafeDrive AI – Intelligent Road Safety Vision System

AICTE × Shell × Edunet Foundation Internship (AI/ML in Automotive)
Developed by: **Sharlene Anna Pereira**

---

## Overview

AutoSafeDrive AI is a complete computer-vision–based Advanced Driver Assistance System (ADAS) prototype.
It analyzes road scenes using deep learning and classical computer vision to detect objects, track vehicle movement, detect lanes, estimate risk, and predict potential collision danger.

Built using YOLOv8, OpenCV, object tracking, lane detection, and a multi-factor ADAS risk engine, this system demonstrates how modern autonomous vehicles perceive and understand their surroundings.

This project represents an extended and enhanced version of the Week 2 milestone of the AICTE × Shell × Edunet Foundation Internship (AI/ML in Automotive).

---

## Key Features

### 1. Zero-Shot Object Detection (YOLOv8)

Detects:

* Cars, trucks, buses
* Motorcycles and bicycles
* Pedestrians
* Traffic lights
* Autorickshaws (via COCO motorcycle class)

No training required; uses pretrained YOLOv8n.

### 2. Multi-Factor ADAS Risk Engine

A custom risk engine computes a score based on:

* Object proximity
* Estimated distance
* Vulnerable road users (pedestrians, cyclists, motorcyclists)
* Object tracking and relative approach speed
* Time-To-Collision (TTC) estimation
* Lane deviation
* Overall scene context

Final risk output is categorized as:

* SAFE
* CAUTION
* DANGER

### 3. Lane Detection and Lane Offset

Performs detection of:

* Lane lines
* Road boundaries
* Vehicle’s displacement from lane center

Uses Canny edge detection and Hough line transform.

### 4. Object Tracking

Implements a lightweight Intersection-over-Union (IoU) tracker:

* Assigns unique IDs to detected objects
* Tracks movement across frames
* Estimates approach or retreat speed

### 5. Batch Evaluation and Analytics

Automatically processes dataset images and generates:

* Annotated output frames
* CSV file containing risk values
* Risk distribution histogram
* Status (SAFE/CAUTION/DANGER) distribution chart

### 6. Gradio ADAS Demo Interface

A real-time interactive dashboard allowing users to:

* Upload custom road images
* Analyze IDD samples
* View detection, tracking, lane results, and risk metrics
* Interact without running any additional code

### 7. Automatic End-to-End Execution

The submission script:

* Downloads the dataset
* Prepares subsets
* Runs detection
* Generates analytics
* Saves all files
* Launches the ADAS dashboard
* Writes a submission-ready README automatically

---

## System Workflow

1. Dataset Collection
   Uses the Indian Driving Dataset (IDD) hosted on Kaggle. Contains complex, real-world Indian traffic scenarios.

2. Object Detection
   YOLOv8 identifies road entities such as vehicles, pedestrians, and traffic signals.

3. Lane Detection
   Classical computer vision methods detect lane boundaries and compute vehicle drift.

4. Object Tracking
   Moving objects are tracked across frames and assigned consistent IDs.

5. Risk Scoring
   Computes an overall risk score for each frame using proximity, speed, distance, TTC, lane offset, and vulnerable road user prioritization.

6. Logging and Visualization
   Saves CSV logs, plots, and annotated frames for analysis.

7. Gradio ADAS Interface
   Provides an interactive way to test images and view the system’s predictions.

---

## Dataset Used: Indian Driving Dataset (IDD)

Contains real images of Indian road scenarios with:

* Dense traffic
* Autorickshaws
* Pedestrians
* Variable lighting
* Complex road conditions

Dataset Source:
[https://www.kaggle.com/datasets/mitanshuchakrawarty/new-idd-dataset](https://www.kaggle.com/datasets/mitanshuchakrawarty/new-idd-dataset)

---

## Technology Stack

* Python
* Ultralytics YOLOv8
* OpenCV
* NumPy
* Pandas
* Matplotlib
* Gradio
* KaggleHub

---

## How to Run (Google Colab)

1. Open Google Colab
2. Paste the complete AutoSafeDrive ADAS script into a single cell
3. Run the cell

The script will automatically:

* Download the dataset
* Prepare data
* Run evaluations
* Launch the ADAS demo
* Save analytics in `/content/autosafedrive_outputs/`

No manual steps required.

---

## Output Files Generated

* Annotated road scene images
* Detailed risk CSV file
* Risk histogram
* Safety status bar chart
* Submission README

---

## Applications

* Driver-assistance prototypes
* Autonomous vehicle perception research
* Collision prediction systems
* Lane-keeping support
* Academic and industry demonstrations

---

## Future Scope

* Bird’s Eye View (BEV) transformation
* Depth estimation using MiDaS or DPT
* Trajectory prediction
* Driver drowsiness and distraction detection
* Steering angle estimation
* Real-time video inference
* YOLOv8 fine-tuning on IDD

---

## Acknowledgements

* Ultralytics YOLOv8 team
* IDD dataset contributors
* OpenCV community
* KaggleHub
* AICTE × Edunet × Shell Internship Program

---

## End of README
---
