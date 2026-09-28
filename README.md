# 🛡️ NetGuard AI: Passive Network Threat Detection System

**NetGuard AI** is an advanced, lightweight network traffic monitoring and passive intrusion detection system engineered to analyze unidirectional IP traffic in real-time. Designed for modern cybersecurity environments, it bridges the gap between raw network telemetry and actionable machine learning intelligence, providing security analysts with a robust tool to identify network anomalies, unauthorized access attempts, and cyber threats without disrupting operational workflows.

---

## 🚀 Key Features

* **Passive Traffic Analysis:** Safely inspects packet captures (`.pcap`) and live network interfaces in a strictly read-only manner, ensuring zero packet loss or network latency disruption.
* **Automated Feature Extraction:** Automatically parses raw IP packet flows to distill high-dimensional network behaviors into precise statistical and behavioral metrics.
* **ML-Powered Threat Classification:** Employs optimized machine learning classifiers trained to recognize signature patterns of malicious traffic, port scans, and volumetric abnormalities.
* **Real-Time Monitoring Dashboard:** Integrates a responsive, interactive web interface built with Streamlit to visualize traffic flows, alert logs, and system health metrics at a glance.

---

## 🏛️ System Architecture & Workflow

The pipeline is structured into three decoupled layers to maximize scalability and modularity:
1. **Ingestion Layer:** Captures raw network packets or loads offline `.pcap` files using robust packet-parsing libraries.
2. **Processing & Feature Engineering:** Extracts critical flow attributes—such as packet inter-arrival times, payload sizes, and protocol flags—into structured tabular features.
3. **Inference & Visualization:** Passes engineered features through serialized machine learning models, instantly flagging anomalies and streaming alerts directly to the dashboard.

---

## 📂 Repository Structure

```text
NetGuard-AI/
├── data/               # Raw and processed packet captures (.pcap)
├── models/             # Serialized machine learning models and scalers
├── src/                # Core pipeline logic
│   ├── extractor.py    # Network traffic feature extraction module
│   ├── predict.py      # Real-time threat inference engine
│   └── utils.py        # Configuration and helper utilities
├── dashboard/          # Interactive Streamlit monitoring application
├── requirements.txt    # Project dependencies and environment specs
└── README.md           # Comprehensive project documentation
