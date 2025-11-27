🚗🔐 VANET Malicious Node Detection using Message-Backtracking
A Security Framework for Detecting Message Tampering in Vehicular Networks (C-ITS / VANETs)

This repository contains an end-to-end implementation of a malicious-node detection framework for Vehicular Ad-Hoc Networks (VANETs), focusing on detecting message tampering attacks using a Python-based backtracking algorithm.

The project includes attack analysis, feature engineering, path reconstruction, and performance evaluation under varying adversarial densities.

📌 Project Overview

Vehicular networks are vulnerable to multiple security threats due to their high mobility and decentralized architecture.
This project develops a forensic detection pipeline that traces message propagation paths and identifies the exact node where a legitimate message was modified into a malicious one.

🚀 Key Features
🔹 1. Attack Modeling

Analyzed multiple VANET security threats including:

Message Tampering

Sybil Attacks

Replay Attacks

Routing Attacks

Denial-of-Service (DoS)

This helped establish a strong understanding of adversarial behavior in C-ITS environments.

🔹 2. Feature Engineering

Performed extensive feature extraction from:

Mobility data (speed, location, trajectory)

Temporal data (timestamps, delays)

Beacon-level data (sender IDs, hop information)

Designed high-impact indicators such as:

Timestamp skew

Hop-count deviations

Message-content deviation metrics

Plausibility checks based on mobility constraints

Applied correlation, variance-based selection, and mutual information ranking.

🔹 3. Message-Backtracking Detection Algorithm

Implemented a Python-based forensic algorithm using Pandas and NumPy to:

Reconstruct message propagation paths

Compare message versions at each hop

Detect content inconsistencies

Localize the exact node where the tampering occurred

This approach ensures high interpretability and reliable identification of the attacker node.

🔹 4. Performance Evaluation

Evaluated system robustness under varying proportions of malicious nodes:

0–20% malicious nodes → Stable precision & accuracy

>25% malicious nodes → Recall & F1-score degrade sharply

This demonstrates the increasing difficulty of detection in dense adversarial environments and highlights realistic system limitations.

📊 Results Summary

High accuracy in detecting message tampering

Strong interpretability of attacker identification

Reduced false positives due to precise feature selection

Clear degradation trend under high adversarial density

Applicable to real-world C-ITS, ITS-G5, and autonomous vehicle communication scenarios

🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib / Seaborn (for visualization)

Jupyter Notebook

📁 Repository Structure
│── data/                     # Raw + cleaned VANET datasets  
│── src/
│     ├── feature_engineering.py
│     ├── backtracking_algorithm.py
│     ├── utils.py
│── notebooks/
│     ├── analysis.ipynb
│     ├── detection_demo.ipynb
│── results/
│     ├── performance_metrics.csv
│     ├── plots/
│── README.md

📌 How to Run

Clone the repository

git clone https://github.com/yourusername/vanet-malicious-node-detection.git
cd vanet-malicious-node-detection


Install dependencies

pip install -r requirements.txt


Run the Jupyter Notebook

jupyter notebook


Open notebooks/detection_demo.ipynb to see the full detection pipeline.

🧠 Future Work

Integrating ML models (GNNs, LSTMs) for enhanced detection

Adding GPS-spoofing and multi-vector attack detection

Real-time simulation using SUMO/OMNeT++

Integrating blockchain for non-repudiation

✨ Author

Anju Yadav
Security Research Intern — C-ITS, VANET, Federated Learning
IIT Guwahati (Mathematical Sciences)
