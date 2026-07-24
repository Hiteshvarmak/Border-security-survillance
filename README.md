# 🛡️ MobileNet–ConvLSTM Based Low-Power Spatio-Temporal Surveillance for Border Security

> An AI-powered border surveillance system that combines **MobileNet** and **ConvLSTM** to detect infiltration activities by learning both spatial and temporal features from surveillance videos. Designed for deployment on low-power edge devices, the system enables real-time monitoring and alert generation.

---

## 📖 Overview

Traditional border surveillance systems primarily rely on spatial information extracted from individual video frames, making them less effective in recognizing motion-based infiltration activities. This project addresses that limitation by integrating **MobileNet** for spatial feature extraction with **ConvLSTM** for temporal sequence learning.

The trained model processes continuous surveillance video streams, identifies suspicious activities, and sends alerts to a central monitoring server. The lightweight architecture enables deployment on edge devices such as Raspberry Pi or NVIDIA Jetson, making it suitable for remote border areas with limited computational resources.

---

## ✨ Features

- 🎥 Real-time surveillance video processing
- 🧠 MobileNet-based spatial feature extraction
- ⏳ ConvLSTM-based temporal feature learning
- 🚨 Automatic intrusion detection and alert generation
- 📡 Edge AI deployment for low-power devices
- 🗄️ Server integration for storing detected events
- 📈 Lightweight architecture with high computational efficiency
- 🔍 Robust against motion-based infiltration scenarios

---

## 🏗️ Architecture

```
                 Surveillance Camera
                         │
                         ▼
                 Video Frame Extraction
                         │
                         ▼
              Image Preprocessing
        (Resize → Normalize → Frame Sequence)
                         │
                         ▼
                MobileNet Feature Extractor
             (Spatial Feature Extraction)
                         │
                         ▼
              Sequence of Feature Maps
                         │
                         ▼
                   ConvLSTM Network
          (Temporal Feature Learning)
                         │
                         ▼
              Fully Connected Layer
                         │
                         ▼
              Infiltration Classification
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
        Alert Generation      Database Storage
```

---

## 📂 Dataset

This project is trained using publicly available surveillance datasets.

### UCF Crime Dataset

Used for abnormal activity recognition including:

- Abuse
- Arrest
- Assault
- Burglary
- Fighting
- Robbery
- Shooting
- Explosion
- Normal Activities

### VisDrone VID Dataset

Used for learning spatial features from aerial surveillance scenes including:

- Humans
- Vehicles
- Outdoor environments
- Aerial object detection

> **Note:** The datasets are not included in this repository due to their large size.

Dataset Links:

- https://www.crcv.ucf.edu/projects/real-world/
- https://github.com/VisDrone/VisDrone-Dataset

---

## ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Border-Surveillance-MobileNet-ConvLSTM.git
```

Navigate to the project

```bash
cd Border-Surveillance-MobileNet-ConvLSTM
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## 📁 Project Structure

```
Border-Surveillance-MobileNet-ConvLSTM/
│
├── dataset/
├── demo/
├── docs/
├── images/
├── models/
├── notebooks/
├── outputs/
├── src/
│   ├── dataset.py
│   ├── mobilenet.py
│   ├── convlstm.py
│   ├── train.py
│   ├── test.py
│   ├── inference.py
│   └── utils.py
│
├── README.md
├── LICENSE
├── requirements.txt
└── .gitignore
```

---

## 🚀 Training

### 1. Prepare the datasets

Download:

- UCF Crime Dataset
- VisDrone VID Dataset

Organize them into the following directory:

```
dataset/
    train/
    validation/
    test/
```

### 2. Preprocess

- Extract video frames
- Resize images to **160 × 160**
- Normalize pixel values
- Create frame sequences
- Generate labels

### 3. Train the model

```bash
python train.py
```

Training includes:

- MobileNet feature extraction
- ConvLSTM temporal learning
- Classification using fully connected layers

---

## 🧪 Testing

Run inference using:

```bash
python test.py
```

For real-time surveillance:

```bash
python inference.py
```

The system will:

- Capture live video
- Predict infiltration activities
- Display prediction
- Save suspicious frames
- Generate alerts

---

## 📊 Results

### Model Performance

| Metric | Value |
|---------|--------|
| Training Accuracy | **92.80%** |
| Architecture | MobileNet + ConvLSTM |
| Input Size | 160 × 160 |
| Deployment | Edge AI Device |
| Application | Border Surveillance |

### Outputs

- Confusion Matrix
- Accuracy Graph
- Loss Graph
- Sample Predictions
- Detected Intrusion Frames

---

## 🔮 Future Work

- Drone-based surveillance integration
- Thermal and infrared camera support
- Multi-camera surveillance system
- Night-time intrusion detection
- GPS-based intruder tracking
- Weapon detection integration
- Face recognition module
- Cloud-based monitoring dashboard
- Edge optimization using TensorRT
- Integration with Large Language Models (LLMs) for intelligent alert summaries

---

## 👨‍💻 Authors

- **K. Hitesh Varma**
- **A. Anshul**
- **K. Vishweshwar Reddy**
- **M. Ganesh**

**Guide**

Dr. A. Pramod Kumar

Department of CSE (CyS, DS) and AI&DS

VNR Vignana Jyothi Institute of Engineering & Technology

---

## 📚 Citation

If you use this project in your research, please cite:

```bibtex
@misc{BorderSurveillance2026,
  title={MobileNet–ConvLSTM Based Low-Power Spatio-Temporal Surveillance for Border Security},
  author={A. Anshul and K. Vishweshwar Reddy and K. Hitesh Varma and M. Ganesh},
  year={2026},
  institution={VNR Vignana Jyothi Institute of Engineering and Technology}
}
```

---

## ⭐ Support

If you found this project helpful:

⭐ Star this repository

🍴 Fork this repository

📩 Open an issue for suggestions or improvements

---

## 📄 License

This project is developed for academic and research purposes. Please cite the authors if you use or extend this work.
