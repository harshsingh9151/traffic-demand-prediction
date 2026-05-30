# Traffic Demand Prediction

## Overview

This project predicts traffic demand using machine learning techniques and feature engineering.

## Dataset

Features include:

- geohash
- day
- timestamp
- RoadType
- NumberofLanes
- LargeVehicles
- Landmarks
- Temperature
- Weather

Target:

- demand

## Feature Engineering

- Hour and minute extraction
- Cyclical encoding
- Peak-hour indicators
- Target encoding for geohash
- Interaction features
- Statistical aggregation features

## Models

- Random Forest Regressor
- Extra Trees Regressor

## Ensemble

75% Random Forest + 25% Extra Trees

## Result

Best leaderboard score: **90.58**

## Tools

- Python
- Pandas
- NumPy
- Scikit-Learn
- Jupyter Notebook
