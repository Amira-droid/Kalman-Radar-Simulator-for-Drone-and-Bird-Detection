# Kalman-Radar-Simulator-for-Drone-and-Bird-Detection
Built a radar-style simulator that tracks drones and birds, predicts future paths, shows a live heatmap, and alerts when drones enter a no-fly zon
Radar Airspace Monitor
Real-Time Multi-Target Tracking • Kalman Filter Prediction • Synthetic Heatmap Radar
A simulation demonstrating airspace safety monitoring using tracking, prediction, and visualization techniques.

# Overview
This project simulates a radar-style airspace monitoring system that tracks multiple moving targets (drones and birds), predicts their future paths, and displays a synthetic heatmap representing radar energy intensity across the airspace. It combines motion modeling, Kalman filtering, radar-like visualization, and safety logic to mimic how real surveillance systems manage air traffic in restricted zones.
This is an excellent demonstration of applied concepts in:
•	Estimation & Tracking (Kalman Filters)
•	Motion Prediction
•	Synthetic Radar Modeling
•	Real-time Web Visualization (Flask + HTML Canvas)
•	Safety-Critical Monitoring

 # Features
# 1. Real-Time Multi-Target Simulation
•	3 simulated drones (red)
•	3 simulated birds (blue)
•	Targets move across a 100×100 virtual airspace and bounce off boundaries.


 # 2. Kalman Filter Tracking
Each target uses a constant-velocity 2D Kalman Filter to estimate:
•	Smoothed position (x, y)
•	Future predicted trajectory
The UI displays:
•	Filtered path (actual position)
•	Future prediction for the leading drone (green dotted line + green markers)

# 3. Radar-Style Heatmap
A synthetic heatmap is generated every 500 ms representing “energy return” from targets:
•	Red/yellow = high concentration of targets
•	Green = medium
•	Blue = minimal activity
Interpreting this:
•	Horizontal axis ≈ X position
•	Vertical axis ≈ Y position
•	Brighter colors indicate regions where objects are clustered

# 4. Restricted Zone Detection + Alerts
•	A rectangular no-fly zone (red box) is enforced
•	If a drone enters, the system triggers:
o	On-screen alert (red text)
o	Audio alarm (alert.wav)


 # 5. Web Interface (Flask + HTML Canvas)
•	Real-time rendering at 2 updates/sec
•	Smooth circles for targets
•	Clean, interactive UI
•	No external dependencies beyond Flask and NumPy

