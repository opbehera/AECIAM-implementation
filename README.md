🔐 AE-CIAM
Hybrid AI-Enabled Framework for Low-Rate DDoS Attack Detection
This project is an academic implementation and experimental extension of the research paper:
“AE-CIAM: A Hybrid AI-enabled Framework for Low-rate DDoS Attack Detection in Cloud Computing”
Authors: Ashfaq Ahmad Najar & S. Manohar Naik
The implementation focuses on validating and comparing the proposed framework using the CICIDS2017 dataset under both binary and multiclass intrusion detection settings.
---
📚 Research Reference
The conceptual foundation of this project is based on the following research work:
AE-CIAM: A Hybrid AI-enabled Framework for Low-rate DDoS Attack Detection in Cloud Computing
Available at:
https://www.researchgate.net/publication/386143198_AE-CIAM_a_hybrid_AI-enabled_framework_for_low-rate_DDoS_attack_detection_in_cloud_computing
⚠️ This project is intended for academic and educational purposes and does not claim to be an official reproduction of the referenced research work.
---
📊 Dataset
CICIDS2017
The dataset was obtained from Kaggle due to temporary unavailability of the official CIC website.
🔗 https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset
Note: This Kaggle dataset is a redistributed version of the original CICIDS2017 dataset by the Canadian Institute for Cybersecurity (CIC).
---
🧠 Model Architecture (as per Research Paper)
Feature Extraction:
Autoencoder with Attention Mechanism (79 → 32 features)
Classification:
CNN Inception Network with Attention Mechanism
Trainable Parameters:
15,624
Reported Performance (Paper):
Binary Accuracy: 99.99%
Multiclass Accuracy: 99.44%
---
🧪 Experimental Setup
Dataset: CICIDS2017 (multi-CSV)
Feature preprocessing: numeric filtering, scaling, NaN & infinity handling
Classification modes:
Binary (Benign vs Attack)
Multiclass (Attack categories)
Evaluation metrics:
Accuracy
Precision
Recall
F1-Score
MCC
Test Loss
Inference Time
---
📈 Results Comparison
Paper vs Our Implementation
🔹 Multiclass Classification
Metric	Paper	Our Model
Accuracy (%)	99.44	95.86
Precision (%)	99.08	96.10
Recall (%)	99.44	95.76
F1-Score (%)	99.26	95.36
MCC	0.9872	0.862
Test Loss	0.0197	0.1157
Inference Time (s/sample)	0.000411	2 × 10⁻⁶
🔹 Binary Classification
Metric	Paper	Our Model
Accuracy (%)	99.99	96.94
Precision (%)	99.99	96.94
Recall (%)	99.99	96.94
F1-Score (%)	99.99	96.96
MCC	–	0.893
Test Loss	0.0246	0.0672
Inference Time (s/sample)	0.000209	2 × 10⁻⁶
---
🎯 Conclusion
This project demonstrates a practical implementation of the AE-CIAM framework using CICIDS2017 and provides a transparent comparison between published research results and experimental implementation outcomes under binary and multiclass settings.
