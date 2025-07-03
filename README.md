# Dynamic-Pricing-for-Urban-Parking-Lots

**Capstone Project – Summer Analytics 2025**  
Hosted by the Consulting & Analytics Club × Pathway

---

## 📌 Project Overview

Urban parking lots are a limited yet high-demand resource. Fixed pricing often leads to inefficiencies — overcrowding during peak hours or underutilization during low-demand periods. This project implements a **real-time dynamic pricing engine** to improve utilization and revenue efficiency across 14 simulated urban parking spaces.

The engine adjusts prices based on:
- Historical occupancy trends
- Vehicle queue lengths
- Nearby traffic congestion
- Special events or holidays
- Vehicle types (car, bike, truck)
- Competitor prices based on geographic proximity

---

## 🎯 Objective

To build a real-time pricing system using only:
- `Python`
- `pandas`, `numpy`
- `Pathway` (for real-time simulation)
- `Bokeh` (for visualization)

The goal is to model and simulate price changes throughout the day and improve lot-level efficiency using economic principles and intelligent data processing.

---

## ⚙️ Features

- 📈 Demand-based dynamic pricing with configurable weights
- 🧠 Linear baseline and advanced pricing models
- 📍 Competitive price adjustment using geospatial distance
- 🔄 Real-time price updates simulated using Pathway
- 📊 Interactive real-time pricing visualization with Bokeh

---

## 🧪 Data Description

- **14 Parking Lots**
- **73 Days**, **18 time points per day (8:00 AM to 4:30 PM)**
- **Features**:
  - `Latitude`, `Longitude`
  - `Capacity`, `Occupancy`
  - `QueueLength`, `TrafficConditionNearby`
  - `IsSpecialDay`, `VehicleType`

---

## 🛠 Technologies Used

| Tool            | Purpose                                    |
|-----------------|--------------------------------------------|
| Python          | Programming Language                       |
| pandas, numpy   | Data processing and feature calculations   |
| geopy           | Distance calculations for competitive logic|
| Bokeh           | Real-time plotting and visualization       |
| Pathway         | Real-time data stream simulation           |
| Google Colab    | Development environment                    |

---

## 📁 Project Structure

📦 urban-parking-pricing/

├── dataset.csv # Input dataset

├── parking_project.ipynb # Main Colab notebook with all models

├── pricing_output.csv # Output prices (optional)

├── README.md # Project documentation




## 🧠 Pricing Models

### ✅ Model 1: Baseline Linear Model
 ```python
Price(t+1) = Price(t) + α × (Occupancy / Capacity)
 ```

### ✅ Model 2: Demand-Based Dynamic Pricing
 ```
Weighted demand function:

Normalized occupancy

Queue length

Traffic level

Special day indicator

Vehicle type weight
 ```

### ✅ Model 3: Competitive Pricing (Optional)
 ```
Calculates distance to nearby lots

Adjusts pricing based on competitor pricing strategy

Suggests rerouting if overcapacity
 ```


📊 Real-Time Visualization
Interactive real-time pricing for selected lots is displayed using Bokeh, simulating live pricing updates with data streaming.


▶️ How to Run
1. Clone the Repository
 ```
git clone https://github.com/yourusername/urban-parking-pricing.git
cd urban-parking-pricing
 ```
2. Install Required Libraries
 ```
pip install pandas numpy bokeh geopy pathway
 ```
3. Open the Notebook in Google Colab or Jupyter
 ```
# In Colab:
Upload `parking_project.ipynb` and run all cells
 ```
# In Jupyter:
jupyter notebook parking_project.ipynb
 ```
📌 Notes
All models are implemented from scratch

No external ML libraries like scikit-learn or TensorFlow were used

Real-time simulation is done using Pathway's streaming framework

Prices are constrained between $5 and $20 to remain practical


