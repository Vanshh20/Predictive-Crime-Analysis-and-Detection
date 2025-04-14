# Predictive Crime Analysis and Detection


---

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Modules](#modules)
  - [Crime Hotspot Detection](#crime-hotspot-detection)
  - [Repeat Offender Prediction](#repeat-offender-prediction)
  - [Patrol Route Optimization](#patrol-route-optimization)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [Screenshots](#screenshots)
- [References](#references)
- [License](#license)

---

## Project Overview
The **Predictive Crime Analysis and Detection** system is an integrated platform designed to assist law enforcement agencies by leveraging machine learning and optimization techniques. It addresses three critical aspects of crime management:
1. **Crime Hotspot Detection**: Identifies high-risk crime areas across India using clustering techniques.
2. **Repeat Offender Prediction**: Predicts the likelihood of offenders reoffending using advanced classification models.
3. **Patrol Route Optimization**: Generates efficient patrol routes prioritizing high-risk areas to minimize travel distance.

The system is implemented as a Flask-based web application with an interactive dashboard, providing actionable insights through visualizations and reports. It achieves scalability, robustness, and practical applicability, reducing patrol distances by approximately 20% and offering over 80% accuracy in offender predictions.

---

## Features
- **Interactive Crime Hotspot Maps**: Visualizes Low, Medium, and High-risk zones across Indian states using Folium.
- **Repeat Offender Classification**: Classifies offenders into Low, Medium, and High risk with an XGBoost model.
- **Optimized Patrol Routes**: Generates risk-prioritized routes for police stations using Ant Colony Optimization (ACO).
- **User-Friendly Dashboard**: Flask-based interface for accessing predictions, maps, and reports.
- **Scalable Data Processing**: Handles large datasets efficiently with Dask and Parquet caching.
- **Custom Visualizations**: Includes color-coded maps, feature importance plots, and route overlays.

---

## System Architecture
The system follows a modular architecture:

![System Architecture](media/system_architecture.png)

- **Input Layer**: Crime data (CSV), GeoJSON boundaries, inmate records (TSV), and simulated police station data.
- **Processing Layer**:
  - Hotspot Detection: K-Means clustering and Folium visualization.
  - Repeat Offender Prediction: XGBoost with Dask for scalability.
  - Patrol Route Optimization: Random Forest and ACO.
- **Output Layer**: Interactive maps (HTML), prediction reports (CSV), and a Flask-based dashboard.
- **Storage Layer**: Parquet files for caching and Pickle for model serialization.

---

## Technology Stack
- **Programming Language**: Python 3.11
- **Data Processing**:
  - Pandas: Data manipulation
  - NumPy: Numerical computations
  - Dask: Large dataset handling
- **Machine Learning**:
  - Scikit-Learn: K-Means, Random Forest
  - XGBoost: Gradient boosting for predictions
- **Optimization**:
  - Custom Ant Colony Optimization (ACO) implementation
- **Geospatial Analysis**:
  - GeoPandas: GeoJSON processing
  - Folium: Interactive maps
- **Web Development**:
  - Flask: Web framework
  - HTML/CSS/JavaScript: Frontend visualizations
- **Visualization**:
  - Matplotlib: Plotting and color mapping
- **Storage**:
  - Parquet: Efficient data storage
  - Pickle: Model serialization
- **IDE**: VS Code

---

## Installation
To set up the project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/predictive-crime-analysis.git
   cd predictive-crime-analysis
