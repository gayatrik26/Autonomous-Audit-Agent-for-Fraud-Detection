# Autonomous Audit Agent for Fraud Detection

## Overview
This project implements an **Autonomous Audit Agent** that monitors a stream of financial transactions and detects anomalies using **unsupervised anomaly detection**. The agent continuously processes incoming transactions and flags potential fraudulent activities.

## Features
- **Synthetic Data Generation**: Simulates realistic financial transaction data.
- **Unsupervised Anomaly Detection**: Uses **Isolation Forest** to identify unusual transactions.
- **Streaming Transaction Processing**: Continuously processes new transactions in real-time.
- **Batch Processing**: Analyzes a batch of transactions to detect anomalies efficiently.

## Tech Stack
- **Python**
- **Scikit-Learn** (Isolation Forest for anomaly detection)
- **NumPy & Pandas** (Data manipulation)
- **Matplotlib & Seaborn** (Visualization)

---

## Project Flow
1. **Generate Synthetic Transaction Data**
2. **Simulate Streaming Transactions**
3. **Train the Anomaly Detection Model (Isolation Forest)**
4. **Score and Label Transactions**
5. **Display Anomaly Detection Results**
6. **Process Transactions in Batches**

---

## Installation
### Clone the Repository
```sh
git clone https://github.com/your-username/fraud-detection.git
cd fraud-detection
```

### Set Up Virtual Environment
```sh
python -m venv env
source env/bin/activate  # On Windows use: env\Scripts\activate
```

### Install Dependencies
```sh
pip install -r requirements.txt
```

---

## Usage
### 1️⃣ Train the Model
Run the training script to train the **Isolation Forest model**:
```sh
python scripts/train_model.py
```
This will save the trained model as a **Pickle (.pkl) file** inside the `model/` directory.

### 2️⃣ Start Streaming Transactions
Run the following script to simulate **real-time transaction monitoring**:
```sh
python scripts/stream_transactions.py
```
The agent will process transactions, detect anomalies, and print results in real-time.

---

## File Structure
```
fraud-detection/
│── model/                   # Trained model stored here
│   ├── isolation_forest.pkl
│── scripts/                 # Python scripts
│   ├── train_model.py        # Model training script
│   ├── stream_transactions.py # Streaming transaction processing
│── .gitignore                # Ignore unnecessary files
│── README.md                 # Project documentation
│── requirements.txt          # Python dependencies
```

---

## Example Output
```
[2025-02-09 16:05:13] Transaction: {'Amount': 1027.77, 'Merchant': 'PayPal', 'Location': 'New York', 'Transaction Type': 'Wire Transfer'}, Prediction: ✅ Legit
[2025-02-09 16:06:10] Transaction: {'Amount': 5000.00, 'Merchant': 'Unknown', 'Location': 'Russia', 'Transaction Type': 'Cryptocurrency'}, Prediction: 🛑 Fraud
```

---

## Author
👩‍💻 **Gayatri Kadam**  
[GitHub](https://github.com/gayatrik26) | [LinkedIn](https://www.linkedin.com/in/gayatri-kadam/)
