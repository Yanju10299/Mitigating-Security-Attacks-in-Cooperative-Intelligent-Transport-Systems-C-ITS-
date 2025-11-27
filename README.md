🚗 VANET Malicious Node Detection (Message Tampering)

This project focuses on detecting message tampering attacks in Vehicular Ad-Hoc Networks (VANETs).
It uses a Python-based backtracking approach to trace how a message travels through the network and identify the node where it was modified.

📌 Overview

In VANET communication, attackers can change a legitimate message into a malicious one.
This project builds a detection system that:

Tracks message flow between vehicles

Compares message content at each hop

Detects where the message was altered

Identifies the malicious node responsible

🔧 Key Components
1. Attack Analysis

Studied common VANET attacks such as:

Message tampering

Sybil

Replay

Routing attacks

DoS

To understand how attackers behave in vehicular networks.

2. Feature Engineering

Extracted useful features from:

Mobility data

Timestamp data

Beacon / communication logs

Selected the most important features for detecting abnormal behavior.

3. Backtracking Algorithm

Implemented using Pandas and NumPy:

Reconstructs the message path

Checks for content inconsistencies

Detects the exact node where the message changed

This makes the detection process simple and interpretable.

4. Performance Evaluation

Tested the system with different proportions of malicious nodes:

Up to 20% malicious nodes → system performs well

Beyond 25% → recall and F1-score drop

This shows how detection becomes harder as attacks increase.

🛠 Tech Used

Python

Pandas

NumPy

Jupyter Notebook

▶️ How to Run
git clone <repo-url>
cd vanet-malicious-node-detection
pip install -r requirements.txt
jupyter notebook


Open detection_demo.ipynb to see the full workflow.

📁 Structure
src/            # Algorithms and utilities
notebooks/      # Analysis and demo notebooks
data/           # Datasets
results/        # Metrics and plots


✨ Author

Anju Yadav
VANET Security | C-ITS | Python
