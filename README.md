# SDN-Based Multipath Data Offloading Using Link Quality Prediction

This repository implements the **LSTM-based channel quality prediction** methodology described in the paper: [SDN-Based Multipath Data Offloading Scheme Using Link Quality Prediction for LTE and WiFi Networks](https://ieeexplore.ieee.org/document/10767139). The implementation focuses on predicting channel quality using machine learning models (LSTM and BLSTM) to aid in decision-making for data offloading in heterogeneous LTE-WiFi networks.

---

## Key Highlights

- **Link Quality Prediction:** Uses LSTM and BLSTM models for classifying channel quality into Good, Intermediate, and Bad categories.
- **Metrics Used:**
  - Hardware-based: Received Signal Strength Indicator (RSSI).
  - Software-based: Packet Delivery Ratio (PDR).
- **Application Context:** This prediction is intended to assist SDN-based traffic offloading decisions between LTE and WiFi.

---

## Motivation

The rapid growth of mobile data traffic demands efficient utilization of network resources. This project:
- Implements link quality prediction using deep learning to classify and forecast channel conditions.
- Enables smarter decision-making for multipath data offloading schemes in SDN-enabled LTE-WiFi networks.

---

## Methodology

### 1. **Link Quality Prediction**
- **Models Implemented:**
  - Long Short-Term Memory (LSTM).
  - Bidirectional LSTM (BLSTM).
- **Input Metrics:**
  - RSSI (hardware-based).
  - PDR (software-based).
- **Classes:**
  - Good, Intermediate, Bad.

### 2. **Data Preprocessing**
- Dataset is derived from IoT-LAB, with features such as RSSI and PDR.
- Preprocessing includes:
  - Removing outliers and redundancies.
  - Standardizing features using `StandardScaler` from `scikit-learn`.

### 3. **Training and Prediction**
- LSTM and BLSTM models are trained on an 80-20 train-test split.
- Prediction performance is evaluated using metrics like accuracy and confusion matrices.

---

## Results

- **Prediction Accuracy:**
  - LSTM: 99.73%.
  - BLSTM: 99.94%.
  - Combined use of RSSI and PDR outperforms individual metrics.

---

## Requirements

- Python 3.9+
- Libraries: `tensorflow`, `scikit-learn`, `matplotlib`

## Citation 📝

If you use the code in this repository, please cite the following paper:
```
@article{kamath2024sdn,
  title={SDN-Based Multipath Data Offloading Scheme Using Link Quality Prediction for LTE and WiFi Networks},
  author={Kamath, Santhosha and Raman, J. Aravinda and Kumar, Pankaj and Singh, Sanjay and Kumar, M. Sathish},
  journal={IEEE Access},
  volume={12},
  pages={176554--176568},
  year={2024},
  publisher={IEEE}
}
```
