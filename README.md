# 🎯 Detecting Facial Features

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![YOLOv8](https://img.shields.io/badge/model-YOLOv8-success.svg)](https://github.com/ultralytics/ultralytics)

A computer vision project that detects key facial and clothing attributes from an image of a person. The model can identify:
- 👓 Whether the person is **wearing glasses**
- 🧑 The **gender** of the person
- 👕 The **color of the shirt** worn

Built using **YOLOv8**, this project performs detection on uploaded images, identifying key facial features and clothing attributes. It is designed for applications in user analytics, visual understanding, and human-centered AI systems.

---

## 📌 Features

- Detects **gender**, **shirt color**, and **glasses** in images.
- Uses **YOLOv8**, a state-of-the-art object detection model.
- Automatically scrapes a **diverse dataset** using the **Pexels API**.
- Image annotation and dataset curation via **Roboflow**.
- Beginner-friendly and easy to run locally.

---

## 📂 Dataset Collection

- Images were scraped from the [Pexels](https://www.pexels.com/) website using their **official API key**.
- The dataset was curated to be **unbiased** with respect to **race and gender**.
- Over **1000+ high-quality images** were collected representing diverse individuals in various environments.

---

## 🖍️ Data Annotation

- Image annotation was performed using [**Roboflow**](https://roboflow.com/).
- Each image was labeled with:
  - `gender` (male/female),
  - `glasses` (wearing glasses/not wearing glasses),
  - `shirt_color` (color name or class).

Roboflow was also used to export data in YOLOv8-compatible format.

---

## 🧠 Model & Training

- The model used is **[YOLOv8](https://github.com/ultralytics/ultralytics)** from Ultralytics.
- Trained on a custom annotated dataset.
- Fine-tuning was performed using Roboflow’s YOLO export and Ultralytics’ training pipeline.

Example training command:
```bash
yolo detect train data=data.yaml model=yolov8n.pt epochs=100 imgsz=640
