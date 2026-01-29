# 🔐 AE-CIAM

**Hybrid AI-Enabled Framework for Low-Rate DDoS Attack Detection**

This project is an academic implementation and experimental extension of the research paper:  
“AE-CIAM: a hybrid AI-enabled framework for low-rate DDoS attack detection in cloud computing.” [web:39]  
**Authors:** Ashfaq Ahmad Najar & S. Manohar Naik [web:39]  

The implementation focuses on validating and comparing the proposed framework using the CICIDS2017 dataset under both binary and multiclass intrusion detection settings. [web:49]

---

## 📚 Research Reference

The conceptual foundation of this project is based on the following research work:

> Najar, A. A., & Naik, S. M., “AE-CIAM: a hybrid AI-enabled framework for low-rate DDoS attack detection in cloud computing,” *Cluster Computing*, 2025. [web:39]

Available at:  
https://www.researchgate.net/publication/386143198_AE-CIAM_a_hybrid_AI-enabled_framework_for_low-rate_DDoS_attack_detection_in_cloud_computing [web:39]

⚠️ This project is intended for academic and educational purposes and does not claim to be an official reproduction of the referenced research work. [web:39]

---

## 📊 Dataset

### CICIDS2017

The dataset used for experiments is **CICIDS2017**, which contains real-world benign and attack traffic with around 80 flow-based features. [web:49]  
Due to temporary unavailability or access issues with the official CIC website, the data was obtained from a Kaggle mirror:

🔗 https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset [web:46]

Note: This Kaggle dataset is a redistributed version of the original CICIDS2017 dataset by the Canadian Institute for Cybersecurity (CIC). [web:49][web:46]

---

## 🧠 Model Architecture (as per Research Paper)

**Feature Extraction**  
- Autoencoder with attention mechanism (input features ≈79 → compressed to 32-dimensional latent representation). [web:39][web:49]

**Classification**  
- CNN Inception-style network with attention mechanism for final attack classification. [web:39]

**Trainable Parameters**  
- Reported trainable parameters: **15,624**. [web:39]

**Reported Performance (Paper)**  
- **Binary accuracy:** 99.99% [web:39]  
- **Multiclass accuracy:** 99.44% [web:39]

---

## 🧪 Experimental Setup (This Implementation)

- **Dataset:** CICIDS2017 (multi-CSV, flow-based features). [web:49]  
- **Preprocessing:** numeric feature selection, scaling, handling NaN and infinite values.  
- **Classification modes:**
  - Binary (Benign vs Attack)
  - Multiclass (Attack categories)
- **Evaluation metrics:**
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - Matthews Correlation Coefficient (MCC)
  - Test loss
  - Inference time per sample

---

## 📈 Results Comparison

### Multiclass Classification

| Metric                     | Paper (AE-CIAM) | Our Model |
|---------------------------|-----------------|-----------|
| Accuracy (%)              | 99.44           | 95.86     |
| Precision (%)             | 99.08           | 96.10     |
| Recall (%)                | 99.44           | 95.76     |
| F1-Score (%)              | 99.26           | 95.36     |
| MCC                       | 0.9872          | 0.862     |
| Test Loss                 | 0.0197          | 0.1157    |
| Inference Time (s/sample) | 0.000411        | 2 × 10⁻⁶  |

### Binary Classification

| Metric                     | Paper (AE-CIAM) | Our Model |
|---------------------------|-----------------|-----------|
| Accuracy (%)              | 99.99           | 96.94     |
| Precision (%)             | 99.99           | 96.94     |
| Recall (%)                | 99.99           | 96.94     |
| F1-Score (%)              | 99.99           | 96.96     |
| MCC                       | –               | 0.893     |
| Test Loss                 | 0.0246          | 0.0672    |
| Inference Time (s/sample) | 0.000209        | 2 × 10⁻⁶  |

---

## 🎯 Conclusion

This project demonstrates a practical implementation of the AE-CIAM framework on the CICIDS2017 dataset and provides a transparent comparison between the published research results and experimental outcomes for both binary and multiclass intrusion detection. [web:39][web:49]  
The gaps between reported and reproduced performance highlight the impact of implementation choices, dataset variants, and experimental conditions, and can guide future optimization and extension work. [web:39][web:44]
