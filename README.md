# 🛒 E-Commerce Customer Satisfaction Score Prediction (Deep Learning Model)

## Project Summary
This project aims to predict Customer Satisfaction (CSAT) scores using Deep Learning techniques, specifically Artificial Neural Networks (ANN). In the e-commerce domain, accurately understanding customer satisfaction from interaction data and feedback is essential for enhancing service quality, strengthening customer retention, and supporting long-term business growth. By applying a neural network–based model, this project enables reliable CSAT score predictions from customer interaction data, providing actionable, real-time insights that organizations can use to identify service gaps and improve overall customer experience.

---

## Project Background
Customer satisfaction is a critical indicator of **loyalty, repeat purchasing behavior, and customer referrals**. Traditionally, satisfaction has been measured through surveys; however, these approaches are often time-consuming and capture only a limited view of the overall customer experience. With the adoption of deep learning techniques, organizations can now **predict satisfaction scores in real time**, enabling faster identification of service gaps and more effective optimization of service delivery.

---

## Dataset Overview
The dataset contains customer interaction records from an e-commerce platform called Shopzilla (1 month).

---

## Project Goal
The goal of this project is to **develop a Deep Learning–based Artificial Neural Network (ANN) model** that can **predict Customer Satisfaction (CSAT) scores** based on customer interaction data from the e-commerce platform Shopzilla.

---

## Tech Stack
- Programming Language: Python 🐍
- Deep Learning Framework: TensorFlow / Keras
- Data Handling & Analysis: Pandas, NumPy, Scikit-learn
- Model Saving/Loading: Joblib, H5 Format
- Frontend: Streamlit
- Visualization: Matplotlib, Seaborn
- Version Control: Git & GitHub

---

## Model Architecture
The model is built as a **multi-layer Artificial Neural Network (ANN)**:

**Input Layer:** Takes in all selected features after preprocessing

**Hidden Layers:**
- Dense layers with ReLU activation
- Batch Normalization for stable training
- Dropout layers to prevent overfitting

**Output Layer:**
Dense layer with Softmax activation for predicting CSAT scores (0–4)

The model is trained with **categorical crossentropy loss**, optimized using the **Adam optimizer**.

---

## Model Performance
From evaluation on the test dataset:

**Overall Accuracy:** ~67%

**Per-Class Performance:**
- CSAT=0 → Precision 0.74, Recall 0.49
- CSAT=1 → Precision 0.87, Recall 0.74
- CSAT=2 → Precision 0.82, Recall 0.59
- CSAT=3 → Precision 0.40, Recall 0.74
- CSAT=4 → Precision 0.67, Recall 0.62

**Insight:** The model performs well overall, especially in distinguishing satisfied (1, 2, 4) customers. Some classes like 3 (neutral) are harder to classify due to overlapping feedback patterns.

---

## Streamlit Frontend
The Streamlit application offers an interactive interface for CSAT prediction through two flexible modes:

- **Manual Input (Sidebar)** → Users can enter individual customer interaction details and receive an instant CSAT score along with prediction probabilities.
- **CSV Upload (Batch Prediction)** → Users can upload a CSV file containing multiple interaction records to generate CSAT predictions in bulk, with the option to download the results for further analysis.

This setup enables both real-time individual predictions and scalable batch processing for business use cases.

---



