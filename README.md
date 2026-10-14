# Real-Time Driver Drowsiness Detection System 🚗

A computer-vision-based project developed as part of our **Engineering Design and Innovation (EDI-I)** coursework to explore real-time driver drowsiness detection and road safety.

## 📌 Project Overview

Driver fatigue and drowsiness can reduce a driver's attention and reaction time, increasing the risk of road accidents. This project explores a vision-based approach to identifying signs of driver drowsiness using a camera, image processing, and machine-learning components.

The repository includes source code for model training, feature extraction, model evaluation, calibration, and graphical user interfaces.

## ✨ Project Components

- **Feature Extraction:** Code for extracting features used by the detection pipeline.
- **Model Training:** Scripts for training the project's detection model.
- **Model Evaluation:** Utilities for evaluating model performance.
- **Calibration:** A separate module for model calibration.
- **User Interface:** Multiple Python UI and dashboard implementations.
- **Session Reports:** A module for generating session reports.
- **Alert Assets:** Sound files included in the project repository.

*The exact detection criteria and supported features should be confirmed against the implementation before making performance claims.*

## 🛠️ Technology Stack

- **Programming Language:** Python
- **Machine Learning:** Model training and evaluation components
- **Computer Vision:** Vision-based driver monitoring
- **User Interface:** Python-based UI and dashboard modules

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
│   ├── ui_embedded.py
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

- Python installed on your system
- The dependencies listed in `requirements.txt`
- A webcam, if required by the selected application entry point

### Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/pavanmundhe/Realtime-driver-drowsiness-detection.git
   cd Realtime-driver-drowsiness-detection
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   ```

   On Windows PowerShell:

   ```powershell
   .venv\Scripts\Activate.ps1
   ```

3. Install the project dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

### Running the Project

The repository contains multiple application entry points. Review the corresponding source files and dependencies to identify the intended entry point before launching the application.

## 🎓 Academic Context

**Project:** Engineering Design and Innovation – I (EDI-I)  
**Domain:** Computer Vision and Machine Learning  
**Application Area:** Driver Safety and Drowsiness Monitoring

## 👥 Contributors and Attribution

This repository is a fork of the original group project:

**Original repository:** [Tanmaygt1/Realtime-driver-drowsiness-detection](https://github.com/Tanmaygt1/Realtime-driver-drowsiness-detection)

The project originated as collaborative academic work. Please refer to the original repository and commit history for project provenance and contributions.

## ⚠️ Disclaimer

This project is intended for educational and demonstration purposes. It is not a certified driver-safety system and should not replace proper rest, safe driving practices, or validated vehicle safety equipment.
