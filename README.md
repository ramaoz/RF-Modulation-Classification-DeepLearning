RF Modulation Classification using Deep Learning

This project implements a Convolutional Neural Network (CNN) to classify wireless RF modulation types from raw I/Q signal samples.
The model is trained using the RadioML 2016 dataset and learns to recognize different digital and analog modulation schemes.

Project Overview

Modern wireless systems use many modulation techniques such as:
- BPSK
- QPSK
- 8PSK
- QAM16
- QAM64
- AM-DSB
- AM-SSB
- GFSK
- PAM4

Automatically identifying modulation types is important in many telecommunications applications such as:
- Cognitive Radio
- Spectrum Monitoring
- Signal Intelligence
- Wireless Security
- 5G / 6G Research

Dataset

Dataset used: RadioML 2016

The dataset contains I/Q signal samples for multiple modulation types under different Signal-to-Noise Ratio (SNR) levels.

Each signal sample contains:
- 2 channels (I and Q)
- 128 time samples

Dataset structure:
(modulation type, SNR) → signal samples

To improve model performance, signals with very low SNR values were filtered:
SNR ≥ 0

Machine Learning Pipeline

RF Dataset
↓
Signal Extraction (I/Q samples)
↓
SNR Filtering
↓
Dataset Preparation
↓
CNN Model
↓
Training
↓
Evaluation
↓
Confusion Matrix Analysis

Model Architecture

Conv2D
MaxPooling
Conv2D
MaxPooling
Flatten
Dense
Dropout
Dense (Softmax)

Results

Final Test Accuracy:
~77%

The project includes:
- Training accuracy plots
- Confusion matrix visualization
- Saved trained model (RF_modulation_classifier.h5)

Project Structure

rf_modulation_classification
│
├── notebook
│     rf_modulation_classification.ipynb
│
├── model
│     RF_modulation_classifier.h5
│
├── figures
│     training_accuracy.png
│     confusion_matrix.png
│
├── RML2016.10a_dict.dat
│
└── README.md

Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

Author

Rama AlSakkar
MSc Telecommunications Engineering
Machine Learning & RF Signal Processing
