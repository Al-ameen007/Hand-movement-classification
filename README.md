# EEG Motor Imagery Classification Project

## Overview

This project aims to classify **EEG (electroencephalography)** signals from the **BCI Competition IV** dataset, where subjects performed motor imagery tasks involving their left and right hands. The goal is to preprocess the raw EEG data, extract meaningful features, and use machine learning models to distinguish between these two motor imagery tasks.

## Dataset

The dataset (`BCICIV_calib_ds1e.mat`) contains EEG signals, recorded at a specific sampling rate, along with event markers indicating the timing of motor imagery tasks. The key focus is on classifying signals related to right-hand and left-hand motor imagery tasks.

## Workflow

### 1. Data Preprocessing and Feature Extraction
- EEG data is segmented into trials corresponding to the motor imagery events, and baseline correction is applied to remove unwanted drifts.
- A **Discrete Fourier Transform (DFT)** is used to convert the EEG signals from the time domain to the frequency domain, allowing for spectral analysis. Band-pass filtering is then applied to focus on relevant frequency components.

### 2. Classification
Two machine learning models are used to classify the motor imagery tasks:
- **Neural Network**: A simple neural network is trained using **KFold cross-validation** to distinguish between the right-hand and left-hand motor imagery tasks.
- **Random Forest Classifier**: A traditional machine learning model is also applied for comparison, with cross-validation to evaluate its performance.

### 3. Evaluation
Both models are evaluated using accuracy metrics, and the results show how well each model can classify the EEG signals into the two motor imagery categories.

## Results

The project demonstrates the effectiveness of using Fourier Transforms and machine learning techniques to classify EEG signals. Both models show reasonable accuracy in distinguishing between right-hand and left-hand motor imagery tasks.


