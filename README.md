# AI-SOC-Guardian
┌─────────────────────────┐
│  Network Traffic / PCAP │
└─────────────┬──────────┘
              │
              ▼
┌─────────────────────────┐
│  Packet Collector       │
│  (PyShark / Scapy)      │
└─────────────┬──────────┘
              │
              ▼
┌─────────────────────────┐
│ Preprocessing Layer     │
│ - Handle Missing Data   │
│ - OneHot / Label Encode │
│ - MinMax / StandardScale│
└─────────────┬──────────┘
              │
              ▼
┌─────────────────────────┐
│ IDS-MTran AI Model      │
│ - Predict Attack / Normal│
└─────────────┬──────────┘
              │
              ▼
┌─────────────────────────┐
│ Alert & Log Manager     │
│ - Save to DB            │
│ - Send Email / API      │
└─────────────┬──────────┘
              │
              ▼
┌─────────────────────────┐
│ Dashboard / Visualization│
│ - Live Attack Feed       │
│ - Statistics & Metrics   │
│ - Network Overview       │
│ - Optional Heatmaps      │
└─────────────────────────┘

IDS-MTran: AI-Based Intrusion Detection System (SOC Layer 1)
📄 Project Overview

IDS-MTran is an advanced AI-powered Intrusion Detection System designed for SOC (Security Operation Center) Layer 1. It leverages deep learning and transformer architectures to detect network attacks in real-time using the NSL-KDD dataset. The system includes a preprocessing pipeline, multi-scale feature extraction, and cross-feature attention to achieve high accuracy in detecting both binary and multi-class attacks.

⚡ Key Features

Multi-Scale Feature Extraction: Extracts low, mid, and high-level features from network traffic.

Transformer-Based Detection: Uses independent transformer encoders for each feature scale.

Cross-Feature Attention (CFE): Enhances feature fusion across multiple scales.

Dynamic Focal Loss: Handles imbalanced classes effectively.

Early Stopping: Prevents overfitting and saves the best model.

Dashboard-Ready: Outputs can be integrated into a real-time monitoring dashboard.

Preprocessing Included: Encodes, scales, handles outliers, and reshapes data for the model.

🧩 Project Components

Data Preprocessor: Cleans, encodes, scales, and reshapes network traffic data.

IDS-MTran Model: Multi-scale patching + transformer backbone + cross-feature attention.

Training & Evaluation:

Focal loss with dynamic alpha for class imbalance

AdamW optimizer with OneCycleLR scheduler

Accuracy, F1-score, precision, recall metrics

Saved Model & Preprocessor: Ready to load for inference or deployment
