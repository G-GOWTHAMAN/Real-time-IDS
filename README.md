# Real-Time Intrusion Detection System (IDS) using Machine Learning and Explainable AI

This project implements a real-time Intrusion Detection System (IDS) that leverages machine learning techniques and Explainable AI (XAI) to detect and explain malicious activity in live network traffic. It integrates both public and custom intrusion datasets to improve detection accuracy and reduce false positives.

## Project Overview

- Real-time detection of multiple types of network intrusions.
- Uses ensemble learning with Random Forest and XGBoost.
- Captures live packet data using Scapy.
- Provides a Streamlit-based dashboard for monitoring.
- Integrates Explainable AI to provide insights behind detection.
- Sends alerts and logs activity for future retraining.
- Continuously improves model performance using stored data.

## Project Novelty: Explainable AI

Traditional IDS systems suffer from high false positive rates due to lack of transparency in classification. This project incorporates Explainable AI to:

- Provide detailed reasoning for each flagged packet.
- Help administrators understand the root cause of alerts.
- Improve trust in detection decisions.
- Reduce unnecessary responses to false alerts.

Explainability is implemented using feature attribution tools such as SHAP or rule-based systems, which highlight the most important factors leading to the classification.

## System Architecture

1. **Packet Capture** – Live packet capture using Scapy.
2. **Preprocessing and Feature Extraction** – Data cleaning and transformation.
3. **Model Training and Prediction** – Ensemble of Random Forest and XGBoost.
4. **Prediction Output** – Classification into normal or various attack categories.
5. **Dashboard** – Real-time display using Streamlit.
6. **Explainable AI and Alert System** – Provides reasoning and notifies administrators.
7. **Logs Database** – Stores all processed network traffic.
8. **Model Retraining** – Uses stored logs to improve model accuracy over time.

## Datasets Used

The project uses a combination of public datasets and custom attack datasets for training:

- CIC-IDS2017
- CIC-DoS2017
- CSE-CIC-IDS2018
- UNSW-NB15
- NF-ToN-IoT-v2
- NF-UQ-NIDS-v2
- CIC-MalMem2022
- IoT Intrusion Detection Dataset
- Network Intrusion Detection (2024)
- Sniffer AI Dataset

Custom attack traffic is generated using simulated attacks in virtual machines and captured using network sniffing tools.

## Tools and Technologies

- Python 3
- Scikit-learn
- XGBoost
- SHAP (for explainability)
- Pandas, NumPy
- Scapy (for packet capture)
- Streamlit (for dashboard)
- SMTP (for email alerting)
