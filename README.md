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

### SIH 2026 | SIH26168

**AI-ML Based Intelligent Dead Reckoning System for Seamless Navigation**

