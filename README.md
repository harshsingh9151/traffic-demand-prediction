# 🚦 Traffic Demand Prediction

## 📌 Overview

This project focuses on predicting traffic demand using machine learning and feature engineering techniques. The objective is to accurately estimate traffic demand based on road characteristics, location information, weather conditions, and temporal features.

The solution combines extensive feature engineering with ensemble learning to improve prediction performance on a competitive leaderboard.

---

## 🎯 Problem Statement

Predict traffic demand using various traffic, road, weather, and location-related features.

Target Variable:

- **Demand** (continuous regression target)

---

## 📊 Dataset Features

The dataset contains information related to:

- Geographical location (Geohash)
- Day
- Timestamp
- Road Type
- Number of Lanes
- Large Vehicles
- Nearby Landmarks
- Temperature
- Weather Conditions

---

## 🛠 Feature Engineering

### ⏰ Time-Based Features

Extracted information from timestamps:

- Hour
- Minute
- Peak Hour Indicator
- Night Indicator
- Hour Bins

### 🔄 Cyclical Encoding

Since time is cyclical, sine and cosine transformations were applied:

- hour_sin
- hour_cos
- minute_sin
- minute_cos

### 🔗 Interaction Features

Created interaction features to capture relationships between variables:

- lane_pressure
- vehicle_lane_interaction
- temp_hour_interaction
- day_hour_interaction
- weather_hour_interaction

### 📍 Location-Based Features

Implemented target encoding and statistical aggregation:

- geohash_te
- geo_mean
- road_mean
- road_lane_mean
- time_mean

---

## 🤖 Models Used

### Random Forest Regressor

Used for capturing non-linear relationships between features and demand.

### Extra Trees Regressor

Added model diversity and reduced variance.

---

## 🎯 Ensemble Strategy

Final predictions were generated using weighted averaging:

```python
final_prediction = (
    0.75 * RandomForest +
    0.25 * ExtraTrees
)
```

This ensemble consistently outperformed individual models.

---

## 📈 Results

| Model | Score |
|---------|---------|
| CatBoost Baseline | 86.75 |
| Feature Engineered Ensemble | **90.58** |

### Improvement Achieved

```text
86.75 → 90.58
```

Total improvement:

**+3.83 leaderboard points**

---

## 🔍 Key Insights

During experimentation:

- RoadType was found to be one of the most influential features.
- Geohash-based target encoding significantly improved performance.
- Statistical aggregation features provided additional gains.
- Weather had relatively low impact compared to road and location features.
- Ensemble learning outperformed individual models.

---

## 🧰 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-Learn
- Jupyter Notebook

---

## 📂 Repository Structure

```text
traffic-demand-prediction/
│
├── traffic_demand.ipynb
├── README.md
├── requirements.txt
├── approach.txt
└── submission_geo_stats.csv
```

---

## 🚀 Future Improvements

Potential future enhancements:

- Gradient Boosting Ensembles
- Advanced Target Encoding Techniques
- Spatial Feature Engineering
- Hyperparameter Optimization
- Model Stacking

---

## 📜 Conclusion

This project demonstrates a complete machine learning workflow involving:

- Data Exploration
- Feature Engineering
- Target Encoding
- Ensemble Learning
- Model Evaluation
- Leaderboard Optimization

The final solution achieved a leaderboard score of **90.58** through systematic experimentation and iterative model improvements.

---

## 👤 Author

**Harsh Singh**

GitHub: https://github.com/harshsingh9151
