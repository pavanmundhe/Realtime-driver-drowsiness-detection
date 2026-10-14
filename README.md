# Real-Time Driver Drowsiness Detection System 🚗

A computer-vision-based driver monitoring system developed as part of our **Engineering Design and Innovation (EDI-I)** project at Vishwakarma Institute of Technology, Pune.

The project combines **MediaPipe Face Mesh, facial feature engineering, and a Random Forest classifier** to detect signs of driver drowsiness from a live camera feed.

## 📌 Overview

Driver drowsiness can impair attention and reaction time, increasing the risk of road accidents. This project explores a non-intrusive, vision-based approach to monitoring driver alertness using facial landmarks and machine learning.

The system extracts facial landmarks, calculates eye and mouth measurements, and uses a trained classifier to distinguish between alert and drowsy states. It also provides a graphical interface for monitoring detection indicators and displaying alerts.

## ✨ Key Features

- **Real-Time Face Landmark Detection:** Uses MediaPipe Face Mesh to extract 468 facial landmarks.
- **Eye Aspect Ratio (EAR):** Measures changes in eye geometry to identify signs of eye closure.
- **Mouth Aspect Ratio (MAR):** Helps identify mouth-opening patterns associated with yawning.
- **Machine Learning Classification:** Uses a Random Forest classifier to classify extracted facial features.
- **Temporal Analysis:** Uses measurements across multiple frames to reduce decisions based on isolated frames.
- **Drowsiness Alerts:** Applies consecutive-prediction logic to determine when to trigger an alert.
- **Graphical User Interface:** Displays camera output and monitoring indicators.
- **Session Reports:** Includes functionality for generating session summaries.

## 🧠 Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core implementation |
| MediaPipe Face Mesh | Facial landmark extraction |
| OpenCV | Computer-vision and camera processing |
| NumPy | Numerical computations |
| scikit-learn | Random Forest classification |
| PyQt | Graphical user interface components |

*The listed technologies reflect the project's described approach; verify the repository's dependency file for the exact installed packages and versions.*

## ⚙️ How It Works

The detection pipeline follows these stages:

1. **Video Capture:** Receives frames from a camera.
2. **Facial Landmark Extraction:** Detects facial landmarks using MediaPipe Face Mesh.
3. **Feature Engineering:** Calculates EAR, MAR, and temporal features from facial measurements.
4. **Classification:** Feeds the extracted features into the trained Random Forest model.
5. **Temporal Smoothing:** Uses consecutive predictions to reduce isolated false alerts.
6. **Alert and Reporting:** Displays the detection state and supports session summaries.

## 📊 Reported Experimental Results

The accompanying research paper reports the following results from experiments using self-recorded videos under controlled, indoor driving-simulation conditions.

| Metric | Hybrid Random Forest | Threshold Baseline |
|---|---:|---:|
| Accuracy | 91% | 78% |
| F1-score | 0.91 | 0.78 |

The paper reports an average processing rate of approximately **28 FPS on an Intel i5 processor**.

These are results reported in the project paper, not independently reproduced benchmarks. Performance may vary with hardware, lighting, camera placement, and the person being monitored.

## 📂 Repository Structure

```text
Realtime-driver-drowsiness-detection/
├── src/
│   ├── calibrate.py
│   ├── eval_model.py
│   ├── extract_features.py
│   ├── generate_session_report.py
│   ├── main_mvp.py
│   ├── pyqt_dashboard.py
│   ├── record_label.py
│   ├── shared_state.py
│   ├── train_model.py
│   ├── ui.py
│   ├── ui_dashboard.py
│   └── ...
├── models/
├── sounds/
├── logs/
├── requirements.txt
├── README.md
└── ...
```

## 🚀 Getting Started

### Prerequisites

- Python
- A webcam, if required by the selected application entry point
- The dependencies listed in `requirements.txt`
- Any model files required by the selected application

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/pavanmundhe/Realtime-driver-drowsiness-detection.git
cd Realtime-driver-drowsiness-detection
```

**2. Create a virtual environment**

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

**3. Install the dependencies**

```bash
python -m pip install -r requirements.txt
```

### Running the Application

The repository contains multiple Python application entry points. The correct entry point and any model-file requirements should be confirmed from the source code before running the application.

## 🔬 Research Paper

The accompanying research paper is titled:

**“Real-Time Driver Drowsiness Detection Using MediaPipe Face Mesh Landmarks and a Hybrid Machine-Learning Classifier.”**

It describes the system methodology, feature engineering, Random Forest classifier, experimental evaluation, and limitations.

## ⚠️ Limitations

- The reported evaluation used a small, self-recorded dataset collected under controlled indoor conditions.
- Performance under extreme lighting, facial occlusion, and other real-world conditions requires further evaluation.
- Glasses and variations in facial geometry may affect landmark detection.
- The system is an academic prototype and is not a certified driver-safety system.

**Important:** Do not use this project as a substitute for adequate rest, safe driving practices, or validated vehicle safety systems.

## 👥 Contributors and Attribution

This project originated as collaborative academic work.

**Original repository:** [Tanmaygt1/Realtime-driver-drowsiness-detection](https://github.com/Tanmaygt1/Realtime-driver-drowsiness-detection)

The work was conducted by a student team from the Department of Computer Science and Engineering (AI & ML), Vishwakarma Institute of Technology, Pune, India.

This repository is a fork of the original group project. Please refer to the original repository and commit history for project provenance and individual contributions.

## 🎓 Project Information

- **Course:** Engineering Design and Innovation – I (EDI-I)
- **Domain:** Computer Vision and Machine Learning
- **Application:** Driver Drowsiness Detection
- **Institution:** Vishwakarma Institute of Technology, Pune, India
