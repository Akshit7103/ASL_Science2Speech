ASL Recognition using Multi-Modal Deep Learning

📌 Project Overview

This project implements an American Sign Language (ASL) recognition system using deep learning. It includes three approaches:

Baseline Model: Image-based CNN for ASL recognition.

Skeletal Model: Uses Mediapipe Hands to extract hand landmarks and classify ASL gestures.

Multi-Modal Model: Combines both image and skeletal data for enhanced recognition accuracy.

The models are trained on the ASL Alphabet Dataset from Kaggle:ASL Alphabet Dataset

📂 Project Structure

├── Final Codes/                  # Main scripts for execution
│   ├── baseline_do_not_touch.py  # Baseline model testing script
│   ├── skaletal_do_not_touch.py  # Skeletal model testing script
│   ├── multi_modal_do_not_touch.py # Multi-modal model testing script
│   ├── final3_combined.py        # Final combined model for ASL recognition
│
|── keypoints_csv_files/      # Skeletal data extracted from Mediapipe
│   ├── skeletal_keypoints.csv    # CSV file containing extracted hand keypoints
│
├── model_files/                  # Scripts for training models
│   ├── Baseline/
│   │   ├── dataset_files_augmentation/
│   │   ├── preprocess_asl.py     # Data augmentation & preprocessing
│   │   ├── splitting.py          # Splitting dataset into train/val/test
│   │   ├── model_training.py     # Training CNN model for ASL recognition
│   │
│   ├── Multi_Modal/
│   │   ├── multi_modal_preprocessing.py  # Extracts skeletal & image features
│   │   ├── multi_modal_training.py      # Multi-modal deep learning model
│   │
│   ├── Skeletal/
│   │   ├── skeletal_extraction.py  # Extracts skeletal features using Mediapipe
│   │   ├── skeletal_training.py    # MLP model for skeletal-based classification
│
├── Models/                        # Pretrained models
│   ├── baseline/
│   │   ├── baseline_model.h5       # Image-based CNN model
│   ├── multi_modal/
│   │   ├── multimodal_model_large_non_augmented.h5 # Multi-modal model
│   ├── skeletal/
│   │   ├── skeletal_model_large_non_augmented.h5  # Skeletal model
│
├── asl_dataset/                    # ASL dataset (from Kaggle)
└── README.md                        # Documentation

📦 Installation

1️⃣ Clone the Repository

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

python "Final Codes/baseline_do_not_touch.py"

Uses a CNN model trained on the ASL dataset.

Predicts sign language based on image input.

2️⃣ Running the Skeletal Model

python "Final Codes/skaletal_do_not_touch.py"

Uses Mediapipe to detect hand landmarks.

Predicts sign language based on skeletal features.

3️⃣ Running the Multi-Modal Model

python "Final Codes/multi_modal_do_not_touch.py"

Combines image and skeletal data for better accuracy.

4️⃣ Running the Final Model

python "Final Codes/final3_combined.py"

Automatically selects the best prediction from all three models.

🧠 Model Details

Model

Input Type

Architecture

Accuracy

Baseline

Image (224x224)

CNN (MobileNetV2)

~90%

Skeletal

Hand Landmarks

MLP (Dense Layers)

~85%

Multi-Modal

Image + Landmarks

CNN + MLP (Fusion)

~94%

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

This project is licensed under the MIT License. Feel free to use and modify.

⭐ Contributing

Want to contribute? Fork the repo and submit a pull request. Any improvements are welcome!

🔗 References

ASL Dataset: Kaggle - ASL Alphabet

Mediapipe Hands: Google Mediapipe
