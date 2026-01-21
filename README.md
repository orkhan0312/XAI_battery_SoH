# 🔍 Step-by-Step Model Explainability with SHAP

This repository contains the code, data structure, and example results supporting the publication:

Detecting Battery Degradation Factors using Explainable AI
O. Gahramanov, H. N. Hokmabad, E. Ginzburg-Ganz, Y. Levron, J. Belikov
Presented at ISGT Europe 2025 Conference

---

## 📘 Overview

Accurate prediction of battery **State-of-Health (SoH)** is essential for ensuring safe, reliable, and efficient battery operation. While deep learning models such as Convolutional Neural Networks (CNNs) provide strong predictive performance, their lack of transparency limits trust and real-world adoption.

This project combines **CNN-based SoH prediction** with **explainable artificial intelligence (XAI)** techniques. A CNN is used to model temporal dependencies in battery time-series data (current, voltage, temperature), and **SHAP** is applied post hoc to explain model predictions. In addition to local explanations, a temporally-aware **Global SHAP** aggregation highlights consistent degradation patterns across the battery lifecycle, enabling transparent identification of key degradation factors.

---

## 🧠 Methodology Summary

The workflow consists of the following steps:

1. **Data Preparation**  
   Battery time-series data are downsampled, normalized, and structured using a sliding window of consecutive charge–discharge cycles to capture temporal dependencies.

2. **CNN-Based SoH Prediction**  
   A one-dimensional CNN is trained to predict battery SoH from sequences of current, voltage, and temperature.

3. **Local SHAP Analysis**  
   SHAP is applied to explain individual predictions by quantifying feature contributions at the cycle level.

4. **Global SHAP Aggregation**  
   Local SHAP values are aggregated across overlapping temporal windows to preserve time dependencies and reveal lifecycle-level degradation patterns.

This approach combines the accuracy of deep learning with interpretable insights into battery degradation drivers.

---

## 📄 Citation

@inproceedings{Gahramanov2025XAI,
  title     = {Detecting Battery Degradation Factors using Explainable AI},
  author    = {Gahramanov, Orkhan and Hokmabad, H. N. and Ginzburg-Ganz, Elinor and Levron, Yoash and Belikov, Juri},
  booktitle = {ISGT Europe Conference Proceedings},
  year      = {2025}
}

---

## 📬 Contact
For questions, feedback, or collaboration:

Orkhan Gahramanov
Tallinn University of Technology
📧 orkhan.gahramanov@taltech.ee
