# SIH-2026-AI-ML-ENABLED-SEAMLESS-NAVIGATION
# SIH26168 — Task A: Dataset Preprocessing

## 📌 Overview

This repository contains **Task A** of SIH26168 — *AI-ML Based Intelligent Dead Reckoning System for Seamless Navigation*.

Task A focuses on preparing the **IO-VNBD dataset** for the ML and INS/EKF modules.

## 🎯 What We Do

* 🔍 Inspect and understand the raw dataset
* 🧹 Clean missing, duplicate, and invalid data
* ⏱️ Analyze and synchronize sensor timestamps
* 📊 Visualize IMU and GNSS data
* 🪟 Generate sliding windows
* 🔀 Create session-based Train/Validation/Test splits
* 🚫 Prevent data leakage
* 📦 Export processed data for downstream models

## 🔄 Pipeline

```text
Raw Dataset
     ↓
Inspection
     ↓
Cleaning
     ↓
Synchronization
     ↓
Visualization
     ↓
Sliding Windows
     ↓
Session-Based Split
     ↓
Processed Dataset
     ↓
ML / INS / EKF
```

## 📂 Repository Structure

```text
SIH26168-Task-A/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── dataset_inspection.ipynb
│   ├── preprocessing.ipynb
│   └── visualization.ipynb
│
├── src/
├── outputs/
├── requirements.txt
└── README.md
```

## 🛠️ Tech Stack

**Python · Pandas · NumPy · Matplotlib · Jupyter/Colab**

## 🚧 Status

**In Progress**

> Goal: Deliver a clean, synchronized, windowed and leakage-free dataset ready for the navigation pipeline.

---
# Task A — IO-VNBD Dataset Processing

Part of **SIH26168 — AI-ML Based Intelligent Dead Reckoning System for
Seamless Navigation**.

This folder contains the work for understanding, cleaning, visualizing,
and preparing the IO-VNBD dataset for the navigation/ML pipeline.

## 📂 Files

| File | Description |
|---|---|
| `MERGED SVW10-VW10.csv` | Original merged dataset used for analysis |
| `cleaned_MERGED SVW10-VW10.csv` | Cleaned version of the merged dataset |
| `vw10_imu_traces.png` | IMU accelerometer and gyroscope visualization |
| `vw10_imu_traces (1).png` | IMU, vehicle-speed and GPS-satellite anomaly visualization |
| `vw10_windows.npz` | Windowed dataset: 5 s windows, 10 Hz, 2.5 s stride |
| `vw10_windows_split.npz` | Windowed dataset with train/validation/test labels |

## 🔄 Processing Pipeline

```text
Raw CSV
   ↓
Cleaning
   ↓
Sensor & Timestamp Analysis
   ↓
Visualization / Anomaly Inspection
   ↓
5-second Sliding Windows
   ↓
Train / Validation / Test Split

### SIH 2026 | SIH26168

**AI-ML Based Intelligent Dead Reckoning System for Seamless Navigation**

