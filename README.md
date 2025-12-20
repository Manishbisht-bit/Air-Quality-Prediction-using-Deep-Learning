* 🌫️ Multi-Station Air Quality Prediction using Deep Learning
* **Project Overview**

This project focuses on hourly air quality prediction using deep learning and hybrid optimization techniques across multiple monitoring stations.

To ensure a fair and scientific evaluation, existing state-of-the-art models from prior research were first reproduced and tested. Based on their limitations, an improved Hybrid AOAOA-Optimized Bi-LSTM model with advanced feature extraction was proposed.

* **📚 Baseline Methods (From Literature)**

Before proposing our model, we implemented and evaluated the methods reported in prior research, following their original architectures and training strategies.

**Methods Reproduced from Literature:**

Bi-LSTM

CNN + LSTM

Attention-based LSTM

GRU

Transformer Encoder

These methods were directly inspired by and adapted from the following reference paper:

[[1] Author(s), “Efficient multi-station air quality prediction in Delhi with wavelet and optimization-based models,” plosone, 2025.](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0330465)

📌 The architectures and training procedures of these models were implemented according to the methodology described in the above paper to ensure reproducibility and fair comparison.

* **🧪 Models Implemented**

The following models were implemented and compared:

Bi-LSTM (Baseline from Literature)

CNN + LSTM (Literature-Inspired)

Attention-Based LSTM

GRU

Transformer Encoder

* **Proposed Model: Hybrid AOAOA-Optimized Bi-LSTM**

🧠 Proposed Model (Final)
Hybrid AOAOA-Optimized Bi-LSTM

The final model improves upon the literature methods by integrating:

Time-frequency analysis

Dimensionality reduction

Meta-heuristic feature selection

Processing Pipeline:

Min–Max Normalization

Wavelet Transform (DB4)

Principal Component Analysis (PCA)

Feature Selection using Hybrid Aquila–Arithmetic Optimization (AOAOA)

Bi-Directional LSTM Prediction

* **🏗️ Model Architecture**

Input: Selected Wavelet–PCA features

Layers:

Bidirectional LSTM (50 units, return sequences)

Bidirectional LSTM (50 units)

Dense output layer

Optimizer: Adam

Loss Function: Mean Squared Error (MSE)

* **📊 Monitoring Stations**

The model is evaluated using hourly air quality data from the following stations:

AshokVihar

DCStadium

DwarkaSec8

NehruNagar

Najafgarh

Okhla

Each station is processed independently to avoid data leakage.

* **📁 Dataset**

The dataset contains hourly air quality measurements including pollutant concentrations and meteorological parameters.

Dataset Source:

🔗 [[Dataset Link Here](https://data.mendeley.com/datasets/bzhzr9b64v/1)]

Dataset Format:
feature_1, feature_2, ..., feature_n, target


Features: PM2.5, PM10, NO₂, SO₂, CO, O₃, etc.

Target: Air quality concentration or AQI

Time Resolution: Hourly

* **📈 Evaluation Metrics**

All models are evaluated using:

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² Score

* **🔬 Experimental Findings**

Literature models perform well but struggle with feature redundancy and noise

Transformer requires large datasets for stable performance

GRU is efficient but slightly less accurate

Proposed AOAOA-Bi-LSTM consistently achieves the best accuracy across stations

* **🚀 Key Contributions**

Reproduction of state-of-the-art air quality prediction models

Hybrid optimization-based feature selection

Wavelet-driven temporal analysis

Robust multi-station forecasting framework

* **🧩 Applications**

Smart city air monitoring systems

Environmental decision support

Public health risk analysis

Pollution control policy planning


* **⚙️ How to Run**
pip install numpy pandas scikit-learn tensorflow pywavelets
python main.py
