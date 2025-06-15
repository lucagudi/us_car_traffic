# Traffic Delay Severity Classification using Machine Learning

This project investigates how machine learning can be used to classify the severity of traffic delays caused by road accidents, based on real-time features available at the time of the incident. The goal is to improve early detection of severe disruptions, aiding routing and traffic control systems.

## 🚗 Problem Statement

Roadway accidents account for a significant portion of urban traffic congestion. Timely identification of high-severity accidents can enable smarter traffic management and help prevent widespread delays. This project focuses on reducing false negatives in severe cases, favoring models with high recall.

## 📊 Dataset

The analysis is based on the [US Accidents Dataset (2016–2023)](https://doi.org/10.48550/arXiv.1906.05409), which includes:
- 7.7M+ accident records across the U.S.
- Features: temporal data, weather, location, infrastructure.

## 🛠️ Methodology

### Preprocessing
- Cleaning, outlier removal, class binarization (1–2 → non-severe, 3–4 → severe).
- Feature engineering (e.g., extracting time-based features, one-hot encoding).

### Modeling
Four classification models were trained and evaluated:
- **Logistic Regression** (baseline)
- **Random Forest**
- **Histogram-Based Gradient Boosting (HGBoost)** ⭐
- **Multilayer Perceptron (MLP)**

### Evaluation Metrics
- Primary: **Recall**
- Secondary: F1-score, Accuracy, ROC AUC

## 🏆 Results

| Model                   | Recall | F1-Score | Accuracy | ROC AUC |
|------------------------|--------|----------|----------|---------|
| Logistic Regression    | 0.69   | 0.71     | 0.68     | 0.74    |
| Random Forest          | 0.77   | 0.52     | 0.71     | 0.81    |
| **HGBoost**            | **0.79** | 0.54   | 0.73     | 0.82    |
| MLP                    | 0.63   | 0.54     | **0.78** | 0.82    |

**HGBoost** provided the best balance of recall and computational efficiency.

## 🧠 Future Work

- Incorporate visual datasets (e.g., street-level imagery like *StreetSurfaceVis*) via CNNs.
- Explore Graph Neural Networks for capturing spatial traffic patterns.
- Address data limitations (feature richness, class imbalance) and fairness concerns.

## 👥 Authors

Eduard Aguado, Luca Giovanni Gudi, Marco Sburlino, David Yoshio Uraji  
MSc in Business Administration and Data Science  
Copenhagen Business School, 2025

## 📄 License

This project is for educational and research purposes.
