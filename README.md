# ASL_Science2Speech 🤟🔊

A real-time deep learning project that converts American Sign Language (ASL) hand gestures into audible speech. It integrates image-based, skeletal-based, and multi-modal models for accurate recognition and uses Text-to-Speech (TTS) to speak predictions.

---

## 📌 Features

- 🎥 Real-time webcam input
- 🧠 Deep learning models (image, skeletal, multi-modal)
- 🖐️ Hand tracking using [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands)
- 🔊 Instant speech output using `pyttsx3`
- 🧪 Fully functional training + preprocessing pipeline
- 🗂️ Modular architecture for experimentation

---

## 🗂️ Project Structure

```
ASL_Science2Speech/
├── Final codes/                    # Real-time model execution scripts
│   ├── baseline do not touch.py
│   ├── skeletal do not touch.py
│   ├── multi modal do not touch.py
│   └── final3_combined.py
│
├── model files/                    # Model training & preprocessing
│   ├── Baseline/
│   │   ├── model training.py
│   │   ├── preprocess_asl.py
│   │   └── splitting.py
│   ├── skeletal/
│   │   ├── skeletal_extraction.py
│   │   └── skeletal_training.py
│   └── multi modal/
│       ├── multi_modal_preprocessing.py
│       └── multi_modal_training.py
│
├── keypoints_csv files/            # Precomputed skeletal keypoints
│   └── skeletal_keypoints.csv
│
├── Models/                         # Trained models (.h5)
│   ├── baseline/
│   ├── skeletal/
│   └── multi modal/
│
└── asl_dataset.zip                 # Raw or augmented dataset archive (optional)
```

---

## 🚀 How to Run (Real-Time Inference)

Make sure your webcam is connected.

### 🔁 All Models Combined (Skeletal + Image + Multi-Modal)

```bash
python "Final codes/final3_combined.py"
```

### 🧠 Run Individually

```bash
# Baseline image model
python "Final codes/baseline do not touch.py"

# Skeletal keypoints model
python "Final codes/skeletal do not touch.py"

# Multi-modal model (image + keypoints)
python "Final codes/multi modal do not touch.py"
```

---

## 🧪 Model Training Pipeline

You can train your own models from scratch.

### 🔧 1. Preprocess + Augment Dataset

```bash
python model files/Baseline/preprocess_asl.py
```

### ✂️ 2. Split into Train/Val/Test

```bash
python model files/Baseline/splitting.py
```

### 🏋️ 3. Train Models

```bash
# Baseline (MobileNetV2)
python model files/Baseline/model training.py

# Skeletal
python model files/skeletal/skeletal_extraction.py
python model files/skeletal/skeletal_training.py

# Multi-Modal
python model files/multi modal/multi_modal_preprocessing.py
python model files/multi modal/multi_modal_training.py
```

---

## 🧰 Dependencies

Install them with:

```bash
pip install -r requirements.txt
```

### Key Libraries:

- `tensorflow`
- `opencv-python`
- `mediapipe`
- `pyttsx3`
- `numpy`, `pandas`, `scikit-learn`

---

## 📊 Models Used

| Model Type | Input | Description |
|------------|-------|-------------|
| Baseline | Image only (224×224) | MobileNetV2-based classifier |
| Skeletal | 2D keypoints (x, y only) | MLP trained on hand landmarks |
| Multi-Modal | Image + Keypoints | CNN + Dense hybrid fusion architecture |

---

## 🎓 Acknowledgements

- ASL Alphabet Dataset
- MediaPipe Hands
- TensorFlow, OpenCV, and Pyttsx3 teams

---

## 📣 Author

**Akshit Mahajan**  
🔗 GitHub: [Akshit7103](https://github.com/Akshit7103)

**Vedant Passi**  
🔗 GitHub: [VedantPassi](https://github.com/VedantPassi)

---

## 📝 License

This project is for educational and research purposes only. 
