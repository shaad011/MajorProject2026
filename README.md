# Network Intrusion Detection Using Deep Learning with Anomaly Thresholding

This repository contains a specialized implementation for detecting network intrusions using a custom Deep Learning architecture powered by the TensorFlow framework. The model is trained on the TON_IoT Network dataset to identify cyber attacks and differentiate them from normal network traffic.

---

# Project Overview

The goal of this project is to provide a high-accuracy automated intrusion detection solution for network security. By leveraging deep learning and reconstruction error thresholding (designed for a Federated Learning framework), the model achieves strong detection rates for critical network threats.

## Key Performance Metrics (Overall Best)

- **Target Classification:** Normal vs. Attack
- **Evaluation Method:** Reconstruction error thresholding (`errs > th`)
- **Dataset Shape:** 211,043 instances × 44 features
- **Environment:** Kaggle GPU (Single GPU Setup)

---

# Tech Stack & Requirements

## Frameworks & Libraries

- TensorFlow 2.19.0
- Keras
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Environment

- Kaggle Notebook (GPU Enabled)

## Installation Requirements

```bash
tensorflow==2.19.0
scikit-learn
pandas
numpy
matplotlib
seaborn
````

---

# Dataset

The model is trained using the **TON_IoT Network Dataset** (`Train_Test_Network.csv`).

## Dataset Classes

| Traffic Type | Instances |
| ------------ | --------- |
| Normal       | 50,000    |
| Attack       | 161,043   |

---

# Model Architecture

A custom Deep Learning configuration was developed specifically for intrusion detection.

## Features

* **Input Features:** 44 network telemetry features

  * Core Network Features
  * DNS Features
  * SSL Features
  * HTTP Features
  * Weird Traffic Indicators

* **Classification Head:**

  * Threshold-based anomaly detection
  * Reconstruction error classification

* **Callbacks Used:**

  * `EarlyStopping`
  * `ReduceLROnPlateau`

---

# Training Results

The model was evaluated using extensive exploratory data analysis (EDA) and testing on dataset splits.

## Classification Summary

| Class  | Instances | Description                             |
| ------ | --------- | --------------------------------------- |
| All    | 211,043   | Evaluated using `classification_report` |
| Normal | 50,000    | Baseline network traffic                |
| Attack | 161,043   | Malicious network traffic               |

---

# Installation

Clone the repository:

```bash
git clone https://github.com/your-username/network-intrusion-detection.git
```

Move into the project directory:

```bash
cd network-intrusion-detection
```

Install required dependencies:

```bash
pip install tensorflow scikit-learn pandas numpy matplotlib seaborn
```

---

# Usage

## Run the Notebook

Open the notebook:

```bash
MajorFinal.ipynb
```

The notebook includes:

* Data preprocessing
* Deep exploratory data analysis (EDA)
* Model training
* Threshold optimization
* Model evaluation
* Classification reporting

## Dataset Setup

1. Download the TON_IoT Network dataset.
2. Place `Train_Test_Network.csv` in the project directory.
3. Update dataset paths if required.

---

# Project Structure

```text
network-intrusion-detection/
│
├── MajorFinal.ipynb
├── Train_Test_Network.csv
├── README.md
│
└── requirements.txt
```

## File Descriptions

| File                     | Description                                                      |
| ------------------------ | ---------------------------------------------------------------- |
| `MajorFinal.ipynb`       | Main notebook containing preprocessing, training, and evaluation |
| `Train_Test_Network.csv` | Source dataset file                                              |
| `README.md`              | Project documentation                                            |
| `requirements.txt`       | Python dependencies                                              |

---

# Model Highlights

* Deep Learning-based intrusion detection
* Reconstruction error thresholding
* Binary classification (Normal vs Attack)
* Optimized for Federated Learning integration
* GPU-accelerated training support
* High detection accuracy for malicious traffic

---

# Future Improvements

* Federated Learning integration
* Real-time intrusion monitoring
* Multi-class attack classification
* Model deployment using TensorFlow Serving
* Explainable AI (XAI) support
* Hyperparameter optimization

---

# Credits

* TensorFlow for the deep learning backend
* UNSW for the TON_IoT Network dataset
* Kaggle for GPU-enabled training environment

---

# License

This project is intended for academic and research purposes.

---

