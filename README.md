# Dynamic-Pricing-for-Urban-Parking-Lots

**Capstone Project – Summer Analytics 2025**  
Hosted by: Consulting & Analytics Club × Pathway


📌 Project Overview
Urban parking spaces are a limited and highly demanded resource. Traditional static pricing leads to inefficiencies — overcrowding during peak hours or underutilization during low-demand periods. This project implements a real-time, intelligent, and demand-sensitive pricing system to optimize parking space utilization and maximize revenue.

Using simulated data for 14 parking lots over 73 days (with time-series steps every 30 minutes), this system adjusts parking prices in real-time based on factors like:

Occupancy rates
Queue length
Traffic congestion
Special event indicators
Vehicle types
Competitor pricing (geolocation-based)

🧰 Tech Stack Used
Technology
Purpose
Python
Core programming language
pandas
Data manipulation and processing
numpy
Numerical operations
geopy
Distance calculation for competition
Bokeh
Real-time visualization of price trends
Pathway
Real-time data ingestion & simulation
Google Colab
Development and execution environment

🏗️ Architecture Diagram (Mermaid)
graph TD
A[Input CSV Dataset (Parking Logs)] --> B[Preprocessing with pandas]
B --> C[Model 1: Baseline Linear Pricing]
B --> D[Model 2: Demand-Based Pricing]
B --> E[Model 3: Competitive Adjustment]
C --> F[Real-Time Pricing Output]
D --> F
E --> F
F --> G[Pathway Streaming Engine]
G --> H[Bokeh Visualization (Live Plot)]
G --> I[Final Output CSV]


⚙️ System Architecture & Workflow
Data Loading & Preprocessing

Input data includes latitude, longitude, capacity, occupancy, queue_length, traffic, special_day, and vehicle_type.

Cleaned and sorted by Time and SystemCodeNumber.

Model 1 – Baseline Linear Model

Simple linear increase in price based on occupancy ratio.

Model 2 – Demand-Based Dynamic Model

Price is influenced by:

Normalized occupancy

Queue length

Traffic level

Special event indicator

Vehicle type weight

Model 3 – Competitive Pricing Model

Uses geopy to calculate distances between lots.

Adjusts price if nearby competitors are cheaper or overburdened.

Real-Time Simulation

Pathway streams data time-step-wise (30 min intervals).

Prices are updated and visualized dynamically.

Visualization

Bokeh renders real-time pricing updates on an interactive plot.

📁 Folder Structure

📦 urban-parking-pricing/
├── dataset.csv # Input dataset (simulated)
├── parking_project.ipynb # Main Google Colab notebook
├── pricing_output.csv # Output file with updated prices (optional)
├── README.md # Project documentation (this file)
├── report.pdf # (Optional) Additional report


🧠 Key Features
✅ Three dynamic pricing models with increasing complexity

✅ Real-time data stream handling using Pathway

✅ Proximity-aware pricing strategy

✅ Interactive real-time plotting via Bokeh

✅ Pure Python implementation — no external ML libraries

📈 How to Run the Project
Clone the Repository
```
(https://github.com/guptakeshav12/Dynamic-Pricing-for-Urban-Parking-Lots.git)
cd Dynamic-Pricing-for-Urban-Parking-Lots
```
Install Required Dependencies
```
pip install pandas numpy geopy bokeh pathway
```
Run the Notebook in Google Colab
```
Open Dynamic Pricing for Urban Parking Lots.ipynb in Google Colab
```
Execute cells sequentially to:

Load data

Generate pricing predictions

Visualize in real time

📎 Documentation
📄 README.md – This file

🧠 Model documentation – Inline comments in parking_project.ipynb

📉 Architecture & logic – Mermaid diagram + explanation

📊 Visualization – Bokeh embedded in notebook

📝 report.pdf (Optional) – Deeper insights, evaluation, and rationale

🔓 Repository Access
🔹 This repository is public

🔹 All scripts and notebooks run without error

🔹 All documentation is self-contained and easy to follow

🔹 No external services are required beyond Colab and GitHub

🙌 Acknowledgements
Consulting & Analytics Club, IITG

Pathway Team

Summer Analytics 2025 Mentors & Organizers

📬 Contact
👤 Author: Keshav Gupta
📧 Email: your.email@example.com
🔗 GitHub: github.com/yourusername
