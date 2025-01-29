# ASL Recognition using Multi-Modal Deep Learning

## 📌 Project Overview
This project implements an **American Sign Language (ASL) recognition system** using **deep learning**. It includes three approaches:

1. **Baseline Model:** Image-based CNN for ASL recognition.
2. **Skeletal Model:** Uses **Mediapipe Hands** to extract hand landmarks and classify ASL gestures.
3. **Multi-Modal Model:** Combines both image and skeletal data for enhanced recognition accuracy.

The models are trained on the **ASL Alphabet Dataset** from **Kaggle**:  
[ASL Alphabet Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)  

---

📦 Project Name
├── 📂 Final_Codes/                  # Final scripts for running the models
│   ├── 📜 baseline_do_not_touch.py      # Baseline model execution
│   ├── 📜 skeletal_do_not_touch.py      # Skeletal model execution
│   ├── 📜 multi_modal_do_not_touch.py   # Multi-modal model execution
│   ├── 📜 final3_combined.py            # Final integrated model
│
├── 📂 keypoints_csv_files/          # Extracted skeletal data
│   ├── 📜 skeletal_keypoints.csv         # CSV with extracted keypoints
│
├── 📂 model_files/                  # Training scripts for each model
│   ├── 📂 Baseline/                      # Baseline model training
│   │   ├── 📜 preprocess_asl.py            # Data augmentation & preprocessing
│   │   ├── 📜 splitting.py                  # Dataset splitting
│   │   ├── 📜 model_training.py             # CNN Model training
│   │
│   ├── 📂 Multi_Modal/                  # Multi-modal model training
│   │   ├── 📜 multi_modal_preprocessing.py  # Feature extraction
│   │   ├── 📜 multi_modal_training.py       # Multi-modal model training
│   │
│   ├── 📂 Skeletal/                      # Skeletal model training
│       ├── 📜 skeletal_extraction.py        # Extracts skeletal keypoints
│       ├── 📜 skeletal_training.py          # Skeletal model training
│
├── 📂 Models/                        # Trained models
│   ├── 📜 baseline_model.h5                # CNN model
│   ├── 📜 multimodal_model_large_non_augmented.h5  # Multi-modal model
│   ├── 📜 skeletal_model_large_non_augmented.h5    # Skeletal model
│
├── 📂 asl_dataset/                   # ASL dataset (from Kaggle)
│
└── 📜 README.md                      # Project description


## 📦 Installation

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/ASL-Recognition.git
cd ASL-Recognition
2️⃣ Install Dependencies
Ensure you have Python installed. Install required libraries:

pip install -r requirements.txt
Required Libraries:
TensorFlow
OpenCV
Mediapipe
NumPy
Pandas
Scikit-learn
Pyttsx3

🚀 Usage
1️⃣ Running the Baseline Model
python "Final Codes/baseline do not touch.py"
Uses a CNN model trained on the ASL dataset.
Predicts sign language based on image input.
2️⃣ Running the Skeletal Model
python "Final Codes/skaletal do not touch.py"
Uses Mediapipe to detect hand landmarks.
Predicts sign language based on skeletal features.
3️⃣ Running the Multi-Modal Model
python "Final Codes/multi modal do not touch.py"
Combines image and skeletal data for better accuracy.
4️⃣ Running the Final Model
python "Final Codes/final3_combined.py"
Automatically selects the best prediction from all three models.
🧠 Model Details
Model	Input Type	Architecture	Accuracy
Baseline	Image (224x224)	CNN (MobileNetV2)	~90%
Skeletal	Hand Landmarks	MLP (Dense Layers)	~85%
Multi-Modal	Image + Landmarks	CNN + MLP (Fusion)	~94%
The Multi-Modal Model outperforms individual models by combining hand landmarks with image features.

📊 Results & Performance
Baseline Model: Performs well for clear images but struggles with low-light conditions.
Skeletal Model: Robust to lighting but less accurate for similar hand poses.
Multi-Modal Model: Best overall performance, leveraging both modalities.
📢 Acknowledgements
Dataset: ASL Alphabet Dataset on Kaggle
Libraries Used: TensorFlow, OpenCV, Mediapipe, Scikit-learn, Pyttsx3
Developers: Your Name(s)
📜 License
This project is licensed under the MIT License.
Feel free to use and modify.

⭐ Contributing
Want to contribute?
Fork the repo and submit a pull request. Any improvements are welcome!

🔗 References
ASL Dataset on Kaggle
Mediapipe Hands

---
