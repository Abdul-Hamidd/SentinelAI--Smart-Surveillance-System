# 🚀 Smart Surveillance and action System (AI-Based)

An intelligent **AI-powered smart surveillance and action system** that detects **weapons, fire/smoke, and violent activities (fight detection)** in real-time using deep learning models. The system can also send **automated email alerts with video evidence** using LLM-generated messages.

---

## 🧠 Project Overview

This project integrates multiple AI models into a single pipeline to enhance security monitoring:

* 🔫 **Weapon Detection** (Gun, Knife)
* 🔥 **Fire & Smoke Detection**
* 👊 **Fight Detection (Violence Recognition)**
* 🤖 **LLM-based Alert Generation (Ollama)**
* 📧 **Automated Email Alerts with Video Clips**

The system works on **live camera feed** and triggers alerts when suspicious activity is detected.

---

## ⚙️ Technologies Used

* **Python**
* **PyTorch**
* **YOLOv8 (Ultralytics)**
* **SlowFast (PyTorchVideo)**
* **OpenCV**
* **Ollama (LLM Integration)**
* **Gmail API**

---

## 🧩 Models Used

### 🔹 1. Weapon Detection Model

* Model: YOLOv8s
* Classes: Gun, Knife
* Trained on custom dataset using Ultralytics

---

### 🔹 2. FireSmoke Detection Model

* Model: YOLOv8n
* Classes: FireSmoke
* Optimized for small datasets

---

### 🔹 3. Fight Detection Model

* Model: SlowFast R50
* Type: Video Classification
* Classes:

  * 0 → Non-Fight
  * 1 → Fight

---

## 🏗️ System Architecture

```
Live Camera Feed
        ↓
Frame Processing (OpenCV)
        ↓
-------------------------------
| YOLO Models (Frame-based)   |
| - Weapon Detection          |
| - Fire Detection            |
-------------------------------
        ↓
-------------------------------
| SlowFast Model              |
| - Fight Detection (Video)   |
-------------------------------
        ↓
Event Detection
        ↓
LLM (Ollama) → Alert Message
        ↓
📧 Email Alert + Video Clip
```

---

## 🚀 Features

* ✅ Real-time surveillance monitoring
* ✅ Multi-model AI integration
* ✅ Detects multiple threats simultaneously
* ✅ Automatic alert generation using LLM
* ✅ Sends email with **attached video evidence**
* ✅ Optimized for performance using frame skipping

---



---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/Abdul-Hamidd/SentinelAI--Smart-Surveillance-System.git
cd SentinelAI--Smart-Surveillance-System
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### 🔹 Run Live Camera Detection

```bash
python inference.py
```

### 🔹 Run Video Analysis

---

## 📧 Email Alert Setup

1. Enable Gmail API
2. Download `credentials.json`
3. Place it in root directory
4. First run will generate `token.pickle`

---

## 🤖 LLM Integration (Ollama)

* Used to generate **human-like emergency alert messages**
* Model: `gpt-oss:120b-cloud`

---

## 🎥 Output

* Real-time bounding boxes:

  * 🔴 Weapon
  * 🟠 Fire
  * ⚠ Fight Warning
* Email alert with:

  * Event description
  * Attached video clip

---

## 🧪 Training Details

### YOLO Models

* Optimizer: AdamW
* Epochs: 300
* Augmentation: Enabled

### SlowFast Model

* Transfer Learning
* Dropout for regularization
* Early stopping applied

---

## ⚠️ Notes

* Model files (`.pt`) are not included due to size

---

## 🌟 Future Improvements

* Web dashboard for monitoring
* Multi-camera support
* Mobile notifications
* Cloud deployment

---

## 👨‍💻 Author

**ABDUL HAMID**

---

## ⭐ If you like this project

Give it a star ⭐ on GitHub!
